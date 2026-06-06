# Agent Rules

## Repository Shape

- This repo is a general creative studio for small art projects and experiments.
- Keep project directories under `projects/`.
- Use lowercase dash-case for directory names.
- Keep project-specific data inside that project's directory, usually under `data/`.
- Keep project-specific render artifacts inside that project's directory, usually under `renders/`.
- `projects/toxes/` is the shared TouchDesigner component/library area.

## TouchDesigner Assets

- Preserve `.toe` and `.tox` files as TouchDesigner assets.
- Do not casually rewrite binary `.toe` or `.tox` files by hand.
- When asked to edit TouchDesigner assets, prefer one of these paths:
  - edit external text assets that the project references, such as Python, GLSL, CSV, JSON, or media files;
  - if TouchDesigner command-line tools are available, use `toeexpand`/`toecollapse` for inspectable edits;
  - otherwise, explain the limitation and propose the smallest safe manual workflow.
- Keep reusable components in `.tox` form when they are meant to be shared across projects.

## Data And Generated Files

- Checked-in CSV, JSON, and render artifact files are acceptable, including generated project data.
- Do not regenerate project data unless the user asks or the requested change clearly requires it.
- Some historical data scripts depend on local absolute paths into `/Users/alex/worlds/basis/basis-language/`; treat those scripts as user-local workflows.

## Verification

- There is no standard automated check loop for this repo.
- For organization or text edits, verify with `git status`, `find`, and `rg`.
- Do not try to launch TouchDesigner projects unless the user explicitly asks.
