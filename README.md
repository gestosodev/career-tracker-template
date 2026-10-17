# Ines Kringler's career tracker

A personal workspace for Ines Kringler's career in dentistry and dental technology. It keeps her factual career history, master CV, work stories, and future job applications together.

Initialised on 17 October 2026 from the supplied two-page English CV, `cv-ines-english.pdf`. Both pages were visually checked and their text extracted. The career records contain imported CV claims; credentials and employment have not been independently verified.

## Current status

- All four career records have been populated from the CV.
- The master Markdown CV is an imported baseline awaiting Ines's review.
- The source lists a dentist role at Dr. Borrmann Dental Clinic from January 2026 to Present. The user confirmed on 17 October 2026 that she still works there.
- Clinical scope and independent treatment at Dr. Borrmann are recorded, alongside university treatment experience. Specific patient cases, case volumes, and outcomes remain not yet documented.
- Current goal: find a dentist job in Madrid. The generic June letter is saved under `career/source-materials/`, with its destination updated at the user’s request. It is not tied to an actual open position.
- Future CVs should use English for now and the repository layout in `cv-tex/example.tex`, as confirmed on 17 October 2026. Output format and page length remain undecided.
- No application has been started. The job tracker is empty.

## File map

| Path | Purpose |
| --- | --- |
| [Career profile](career/profile.md) | Identity, contact details, languages, preferences, sources, and open questions |
| [Detailed experience](career/experience.md) | Roles, education, licence entry, and clinical observerships |
| [Work summaries](career/work-summaries.md) | Partial first-person STAR records with verbatim CV passages |
| [Master CV](career/cv.md) | General Markdown CV for review and later tailoring |
| [Job tracker](applications/job-tracker.md) | Opportunity status, deadlines, and next actions |
| `applications/<company>/<role>/` | Separate workspace for each future application |
| [Application templates](templates/application/) | Starting files for research, role analysis, questions, CV support, and answers |
| [Agent instructions](AGENTS.md) | Operating rules for the AI agent |
| `sources/` | Local source PDF and extracted text, ignored by Git |
| `exports/` | Future rendered documents, ignored by Git |
| [Optional LaTeX layouts](cv-tex/README.md) | Template examples containing placeholders, not Ines's career evidence |

The original PDF is retained as `sources/cv-ines-english.pdf`; the checked extraction is `sources/cv-ines-english-extracted.txt`. The source was supplied from `/Users/luis/Documents/personal/CV-ines/cv-ines-english.pdf`.

## Next review

Review the [open questions](career/profile.md#open-questions), starting with contact details, output format and page length, and intended next roles. English and the repository CV template layout are confirmed. Confirm the observership dates printed as December 2025 and October 2011. Exact qualification and licence details can be added from supporting documents.

To develop a work story, describe one role, patient-care situation, decision, or challenge in Ines's own words. Useful details include the situation, her responsibility, what she personally did, collaborators, and the observed result. The CV provides role descriptions but little of this context.

## Start an application

Start a new conversation for each opportunity and supply the job posting, company, deadline, and any form questions. A useful starting request is:

> Read AGENTS.md and the career records. Prepare an application for this opportunity. Create a separate application folder from templates/application/, investigate the role, map its requirements to documented experience, and ask about gaps. Tailor the master CV into the application folder and prepare the requested drafts for review.

Review the Markdown before rendering. Use the English language and CV template layout selected in `career/profile.md`; confirm output format and page length when rendering. Keep rendering sources with the application and final files in `exports/`. Populate a copy of `cv-tex/example.tex` with reviewed content; its placeholder content remains an example.

## Maintain the record

Keep detailed facts in `career/experience.md`, reusable stories and original wording in `career/work-summaries.md`, and a general CV in `career/cv.md`. Application-specific wording belongs in its application folder. Review imported facts with Ines before using them in an application.

The Markdown records contain personal information. Original documents and generated exports stay local by default; inspect any proposed commit before sharing or committing.
