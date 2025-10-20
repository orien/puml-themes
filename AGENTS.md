# Repository Guidelines

## Project Structure & Module Organization
Themes live in `themes/` as paired `.puml` sources and `.md` documentation (e.g., `puml-theme-solarized-light.*`). The gallery tool under `tools/gallery-generation/` holds the Ruby CLI in `bin/`, YAML configuration in `config/`, and sample diagrams in `puml/`. Temporary exports or scratch assets belong in `tools/tmp/`. Refer to `README.md` for user-facing instructions before adding new folders.

## Build, Test, and Development Commands
- `tools/gallery-generation/bin/gallery` updates each theme’s gallery section based on `config/gallery.yaml`; run after adjusting samples or URLs.
- `ruby tools/gallery-generation/bin/gallery` is interchangeable when you prefer explicit invocation (ensure Ruby 3.x is available).
- `plantuml -tsvg examples/diagram.puml` renders a local preview; duplicate an existing sample in `tools/gallery-generation/puml/sequence/`, include your theme, then run this command to sanity-check colors.

## Coding Style & Naming Conventions
PlantUML themes use two-space indentation and `$UPPER_SNAKE_CASE` variables for palettes and font settings. Keep comments in PlantUML files prefixed with `'` and wrap reusable logic in `!procedure` blocks. Follow the naming convention `puml-theme-<theme-name>.(puml|md)` and avoid spaces or uppercase letters in filenames. Ruby utilities follow idiomatic Ruby style: `snake_case` method names, double-quoted strings when interpolation is anticipated, and early returns for guard clauses.

## Testing Guidelines
There is no automated test suite; rely on rendering checks. For every theme change, render at least the sequence diagrams listed in `config/gallery.yaml` and confirm contrast, stroke widths, and font sizing. Update or add `.puml` samples when introducing new diagram scenarios so the gallery reflects the change. If PlantUML reports syntax issues, resolve them before opening a pull request.

## Commit & Pull Request Guidelines
Review history favors concise, imperative commit messages (e.g., “Enhance README with comprehensive project documentation”). Write descriptive bodies when context is non-obvious. Pull requests should link any relevant issues, summarize visual changes, and attach before/after renders or PlantUML URLs when modifying theme aesthetics. Ensure the gallery output is refreshed in the same branch whenever theme visuals change.

## Gallery Maintenance
Keep `config/gallery.yaml` authoritative: list every theme slug and diagram category you expect to showcase. When adding a theme, include it in `themes:` and supply the necessary `.puml` samples; the gallery command will then populate the corresponding Markdown block automatically.
