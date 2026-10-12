# Optional LaTeX example

`example.tex` adapts the original career tracker's two-column layout: dates and section labels on the left, career content on the right. It retains the typography, spacing, and reusable layout commands while replacing all personal content with placeholders. The header includes a 36 mm example photo and the original location, phone, email, and LinkedIn icons. `image-example.png` is the supplied placeholder image in a LaTeX-compatible format. It is not a personal photo. A rendered preview is included as `example.pdf`. Its text corresponds to the placeholder master Markdown CV.

This is a presentation example, not candidate evidence and not an automatic Markdown converter. You can use your own LaTeX, Word, HTML, or other template instead. Record that preference in `career/profile.md`.

## Use for an application

1. Finish and review `applications/<company>/<role>/cv.md`.
2. Copy `cv-tex/example.tex` to that application's `cv.tex`. Keep the shared photo and icon assets in `cv-tex/`; the source searches there when compiled from the repository root. For an online editor, upload the source and the five supporting assets (the PNG photo and the four icon PDFs) together.
3. Ask the agent to synchronise the reviewed Markdown into that source while preserving the layout. Escape LaTeX special characters, including `%`, `&`, `_`, `#`, and `$`.
4. Compile with XeLaTeX or LuaLaTeX. PDFLaTeX does not support this example's `fontspec` setup.
5. Inspect the PDF visually and check extracted text and links against the Markdown. Long role blocks use minipages and may need to be split for page breaks. Replace every placeholder before sending.

The example tries the full Roboto font family when available and otherwise falls back to Latin Modern fonts. It uses standard packages: `babel`, `calc`, `enumitem`, `fontspec`, `geometry`, `microtype`, `graphicx`, and `hyperref`. Use a TeX installation that provides them, or upload the source to a LaTeX editor and select XeLaTeX.

From the repository root, to compile the placeholder example:

```sh
mkdir -p exports
xelatex -interaction=nonstopmode -halt-on-error -output-directory=exports cv-tex/example.tex
```

For a real application, substitute your actual company and role folder:

```sh
xelatex -interaction=nonstopmode -halt-on-error -jobname=company-role-cv -output-directory=exports applications/company/role/cv.tex
```

Use `lualatex` in place of `xelatex` if preferred. Run again if the compiler requests it. Keep the source in Git and generated PDFs in `exports/`. A failed or unavailable compiler must be reported, with the source retained for later rendering.

## Replace the example photo

Replace `image-example.png` with your own PNG photo, or update the image reference to a local photo path if you do not want to commit it. Keep the original 36 mm height for the same header proportions. The four supplied icon PDFs can remain shared across applications.

`example.pdf` is the rendered placeholder preview, not an application deliverable. Regenerate it after changing the template source or assets. The `exports/` folder is for personal application exports and remains ignored by Git.

## Cover-letter example

`cover-letter-example.tex` uses the original cover-letter layout: A4, 15 mm margins, a 44.5 mm left column, a 3.5 mm column gap, black section rules, and letter paragraphs in the right column. The name sits on the left and contact details on the right. It uses Roboto when installed and a Latin Modern fallback otherwise. Unlike the CV header, this letter layout has no photo or icons.

Its content matches `templates/application/cover-letter.md`. Both contain placeholders only. Draft and review the application's `cover-letter.md` first, then copy this source to `applications/<company>/<role>/cover-letter.tex` and synchronise the content. Preserve the exact headings required by an application when provided. This example is optional; omit the letter if it is not needed.

Compile the example from the repository root:

```sh
xelatex -interaction=nonstopmode -halt-on-error -output-directory=exports cv-tex/cover-letter-example.tex
```

The included `cover-letter-example.pdf` and `cover-letter-example-preview.png` show the placeholder layout. Personal application exports belong in `exports/`. Each body block is a minipage, so keep it short enough to fit a page or split it deliberately when expanding the letter. Check the rendered result against the Markdown before sending.
