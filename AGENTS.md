# Repository conventions

This repository holds reusable skills, plugins, and scripts.

- Put each skill in `skills/<skill-name>/` with a `SKILL.md` entrypoint. Keep its references, assets, metadata, and exclusive helpers within that folder.
- Put authored or customized plugins in `plugins/<plugin-name>/`, following the plugin platform's required manifest and structure.
- Put independent or shared utilities in `scripts/`. Prefer existing platform features and standard libraries; add dependencies only when needed.
- Keep `plugins/` and `scripts/` tracked with `.gitkeep` until their first resources are added. Remove each placeholder when adding content. Create other directories only as needed.
- Update the README catalog and installation instructions when resources are added, moved, or removed.
- Keep personal evidence, secrets, generated artifacts, and installed dependencies out of commits. Use synthetic examples when needed.
- Preserve relative links within skills so each skill remains portable.
- Validate changed skills with an available skill validator, and check references and metadata. For executable utilities, run an appropriate focused check and document required dependencies and usage.
- Preserve unrelated local changes and keep changes scoped to the requested resource.
