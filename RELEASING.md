# Releasing

The plugin is the folder `plugins/lovitations/`. It holds only manifests,
skills, images and docs; tooling stays outside it so plugin directories can
scan everything that ships. The Claude directory only accepts Markdown, text,
JSON, YAML and PNG/JPEG/GIF/WebP/ICO images (no SVG, nothing starting with
`#!`) from organizations that aren't Verified; `scripts/check.mjs` enforces
that for the plugin folder. The Claude directory submission must use
`plugins/lovitations` as its plugin path, not the repo root.

One version number lives in five places, all under the plugin folder except
the marketplace: `.claude-plugin/plugin.json`, `.codex-plugin/plugin.json`,
`gemini-extension.json`, a `## X.Y.Z` section in `CHANGELOG.md`, and the
entry in the repo-root `.claude-plugin/marketplace.json`.
`scripts/check.mjs` fails CI when they disagree.

1. On a branch: `node scripts/bump.mjs X.Y.Z` and replace the TODO in
   `plugins/lovitations/CHANGELOG.md` with what changed. Patch for wording
   fixes, minor for a new or changed skill, major for a removed or renamed
   skill.
2. Open a PR. CI checks the manifests, validates for Claude and Gemini, and
   builds the ZIP.
3. After the merge, tag the merge commit on `main` and push the tag:
   `git tag vX.Y.Z && git push origin vX.Y.Z`
4. The release workflow checks that the tag is on `main` and matches the
   manifests, builds `lovitations-X.Y.Z.zip` and publishes a GitHub
   release with the ZIP as its only asset and the CHANGELOG section plus the
   ZIP's SHA-256 as notes. Keep it to one asset: Gemini CLI installs a release's single
   asset and falls back to the whole-repo tarball when there are more.

`v*` tags cannot be moved or deleted (repository ruleset "release tags are
immutable"), so a bad release is fixed with a new patch version, never by
re-tagging.

After a release:
- lovitations.nl: link the ZIP from the free tools page if it is offered there.
- OpenAI: upload the new ZIP as a new version in the plugin dashboard.
- Anthropic picks up new commits from the repository; Gemini CLI picks up the
  new release.
- Grok Build: bump the pinned `sha` in xai-org/plugin-marketplace, once listed there.

Local build: `bash scripts/build-zip.sh` (writes `dist/`).
