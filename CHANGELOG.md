# Changelog

Notable changes to the monitoring configuration. The data commits under
`history/`, `api/` and `graphs/` are written by CI and are not listed here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## 2026-08-28

### Added

- Initial Upptime instance for PaceStreak, split out from the owner's private
  all-projects status page.
- Four monitors: `www.pacestreak.com` (canonical) and `pacestreak.com` (which,
  because redirects are followed, asserts the whole chain), each with a body
  content assertion; plus a TLS expiry check for **each** hostname.
- Status page themed to the product palette, at `status.pacestreak.com`.

### Fixed

- `api/` and `graphs/` were deleted outright when clearing the template's demo
  data. Upptime scandirs both unconditionally, so every run logged `ENOENT`.
- Five workflows existed on disk but were invisible to the Actions API and so
  could not be dispatched. GitHub only registers a workflow when a push
  modifies it.

### Notes

- Licence remains MIT, inherited from upstream Upptime. Most of this repository
  is their code, so it is not ours to relicense.
- `update-template` cannot regenerate the workflows here: `GITHUB_TOKEN` may
  never write under `.github/workflows`, whatever the org permissions say. That
  needs a PAT with the `workflow` scope stored as `GH_PAT`.
