# Optional LaTeX example

`example.tex` adapts the original career tracker's two-column layout: dates and section labels on the left, career content on the right. It retains the typography, spacing, and reusable layout commands while replacing all personal content with placeholders. It needs no photo, icons, or external image assets. Its text corresponds to the placeholder master Markdown CV.

This is a presentation example, not candidate evidence and not an automatic Markdown converter. You can use your own LaTeX, Word, HTML, or other template instead. Record that preference in `career/profile.md`.

## Use for an application

1. Finish and review `applications/<company>/<role>/cv.md`.
2. Copy `cv-tex/example.tex` to that application's `cv.tex`.
3. Ask the agent to synchronise the reviewed Markdown into that source while preserving the layout. Escape LaTeX special characters, including `%`, `&`, `_`, `#`, and `$`.
4. Compile with XeLaTeX or LuaLaTeX. PDFLaTeX does not support this example's `fontspec` setup.
5. Inspect the PDF visually and check extracted text and links against the Markdown. Long role blocks use minipages and may need to be split for page breaks. Replace every placeholder before sending.

The example tries the full Roboto font family when available and otherwise falls back to Latin Modern fonts. It uses standard packages: `babel`, `calc`, `enumitem`, `fontspec`, `geometry`, `microtype`, and `hyperref`. Use a TeX installation that provides them, or upload the source to a LaTeX editor and select XeLaTeX.

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
