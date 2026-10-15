# Consulting Kings Q&A Manager

Shared decision log for Consulting Kings: the team answers open questions, admins set results, and every question moves from Open to In Discussion to Solved. Organised by project and meeting, with AI-assisted bulk add, transcript import and result suggestions, plus Markdown, CSV and JSON export.

`index.html` is a single file written as a Claude Artifact. It is not meant to be opened as a plain web page, because it relies on the Artifact runtime.

## Runtime capabilities

Declared when publishing the Artifact:

- `db`: one document per record in the collections `users`, `projects`, `meetings`, `sections`, `questions`, `answers`. Live updates through `onSnapshot`.
- `sample`: AI features (bulk sorting, transcript analysis, result suggestions).
- `downloads`: export as `.md`, `.csv` and `.json`.

## Roles (inside the app)

- **Contributor** (default): answers questions, adds questions, sections and meetings.
- **Viewer**: read-only.
- **Admin / Super admin**: set results, manage users, projects and access.

These roles are enforced in the page only. Who may write to the database at all is decided by the Artifact's Share menu: people need at least Contributor there to save anything.

## Publishing

Publish `index.html` with the capabilities above. The starter content (questions and sample answers) is written into an empty database on first open.
