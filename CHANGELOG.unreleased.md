# Unreleased changes

Add here any changes made in a PR that are relevant to end users. Allowed sections:

- Added - for new features.
- Changed - for changes in existing functionality.
- Deprecated - for soon-to-be removed features.
- Removed - for now removed features.
- Fixed - for any bug fixes.
- Security - in case of vulnerabilities.

Section headings should be at level 3 (e.g. `### Added`).

## Unreleased

### Added

- The `reinit` setting can be set to `"default"` (@timoffex in https://github.com/wandb/wandb/pull/9569)

### Changed

- Boolean values for the `reinit` setting are deprecated; use "return_previous" and "finish_previous" instead (@timoffex in https://github.com/wandb/wandb/pull/9557)
- The "wandb" logger is configured with `propagate=False` at import time, whereas it previously happened when starting a run. This may change the messages observed by the root logger in some workflows (@timoffex in https://github.com/wandb/wandb/pull/9540)

### Fixed

- Calling `wandb.init()` in a notebook finishes previous runs as previously documented (@timoffex in https://github.com/wandb/wandb/pull/9569)
    - Bug introduced in 0.19.0
- Fixed an error being thrown when logging `jpg`/`jpeg` images containing transparency data (@jacobromero in https://github.com/wandb/wandb/pull/9527)
- `wandb.init(resume_from=...)` now works without explicitly specifying the run's `id` (@kptkin in https://github.com/wandb/wandb/pull/9572)
