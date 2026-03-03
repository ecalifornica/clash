# Changelog

## [0.4.0](https://github.com/ecalifornica/clash/compare/v0.3.6...v0.4.0) (2026-03-03)


### ⚠ BREAKING CHANGES

* **policy:** `(sandbox ...)` blocks are removed in version 3. Use `(match ctx.http.domain ...)` and `(match ctx.fs.path ...)` instead. Run `clash policy upgrade` to auto-migrate.

### Features

* Add session and project level policies ([#63](https://github.com/ecalifornica/clash/issues/63)) ([c65efb9](https://github.com/ecalifornica/clash/commit/c65efb96af024afad1a068ee2e6c8c08b46b31ab))
* allow reading from agent transcript directory via internal policy ([3851b99](https://github.com/ecalifornica/clash/commit/3851b99cb1633762743ff15e38fe82c764197c1f)), closes [#103](https://github.com/ecalifornica/clash/issues/103)
* **init:** prompt user to choose scope instead of assuming both ([#90](https://github.com/ecalifornica/clash/issues/90)) ([dd49acf](https://github.com/ecalifornica/clash/commit/dd49acf04805161eaa5a08486f32df1a46e6146d))
* **policy:** add eq predicate for when guards ([#237](https://github.com/ecalifornica/clash/issues/237)) ([395f3d0](https://github.com/ecalifornica/clash/commit/395f3d0d45e3d6f6e53be80dd804a82734a39b4b)), closes [#219](https://github.com/ecalifornica/clash/issues/219)
* **policy:** add mcp invocation type and ctx.mcp.* observables ([#242](https://github.com/ecalifornica/clash/issues/242)) ([cf91bfb](https://github.com/ecalifornica/clash/commit/cf91bfb84c95547a0a2b5039fe39a1a807a23862)), closes [#217](https://github.com/ecalifornica/clash/issues/217)
* **policy:** add path-based matching to network capability rules ([#188](https://github.com/ecalifornica/clash/issues/188)) ([cce1325](https://github.com/ecalifornica/clash/commit/cce13252e1e286f9dce660aa738cb68bbe74c06c))
* **policy:** add version declaration and upgrade framework ([#158](https://github.com/ecalifornica/clash/issues/158)) ([cc47a4e](https://github.com/ecalifornica/clash/commit/cc47a4eb85cfcf5cc93473a96778d3e17227d49d))
* **policy:** add version syntax and upgrade command ([#185](https://github.com/ecalifornica/clash/issues/185)) ([cc47a4e](https://github.com/ecalifornica/clash/commit/cc47a4eb85cfcf5cc93473a96778d3e17227d49d))
* **policy:** deny all hooks on invalid policy and add validate subcommand (EMP-92) ([#89](https://github.com/ecalifornica/clash/issues/89)) ([cb1e568](https://github.com/ecalifornica/clash/commit/cb1e5686c2590d20665d8cb9e3468c8e615ac31d))
* **policy:** derive sandbox constraints from decision tree ([#243](https://github.com/ecalifornica/clash/issues/243)) ([ac20a05](https://github.com/ecalifornica/clash/commit/ac20a0573e1689a2f5c4fafc9a59d221f9188f69))
* **policy:** replace (default ...) with (use ...) + body-level effects ([#215](https://github.com/ecalifornica/clash/issues/215)) ([7379981](https://github.com/ecalifornica/clash/commit/7379981b04d57217f90a09a494993620ed08dbbd))
* **sandbox:** support localhost-only network policy ([#192](https://github.com/ecalifornica/clash/issues/192)) ([d6944a3](https://github.com/ecalifornica/clash/commit/d6944a3eb2dfe9da9eaeb546e4c0f11137c22ceb)), closes [#123](https://github.com/ecalifornica/clash/issues/123)
* Teach claude how to amend it's policy for a session after it asks for permission ([#70](https://github.com/ecalifornica/clash/issues/70)) ([cc13a87](https://github.com/ecalifornica/clash/commit/cc13a87921810bba37b361421fb3628b9007aecc))


### Bug Fixes

* AskUserQuestion auto-approved by (allow (tool)), skipping interactive UI ([#174](https://github.com/ecalifornica/clash/issues/174)) ([3a75ebb](https://github.com/ecalifornica/clash/commit/3a75ebbe397536140cfd609a4e3e5b9e5c79ce38))
* **eval:** skip env var prefixes when extracting binary name ([#110](https://github.com/ecalifornica/clash/issues/110)) ([3d8c010](https://github.com/ecalifornica/clash/commit/3d8c0103571dc986df6269aed5c29bfacc4b2df8)), closes [#105](https://github.com/ecalifornica/clash/issues/105)
* **explain:** handle "tool" as domain keyword in explain command ([#143](https://github.com/ecalifornica/clash/issues/143)) ([86be313](https://github.com/ecalifornica/clash/commit/86be313e87c07dd718206f537229050a43b11965)), closes [#106](https://github.com/ecalifornica/clash/issues/106)
* **hooks:** passthrough interactive tools to preserve Claude Code UI ([3a75ebb](https://github.com/ecalifornica/clash/commit/3a75ebbe397536140cfd609a4e3e5b9e5c79ce38))
* **hooks:** passthrough plan mode tools to preserve Claude Code native UI ([#186](https://github.com/ecalifornica/clash/issues/186)) ([7afaad3](https://github.com/ecalifornica/clash/commit/7afaad3f60cde34ff582776d3bdc9f9ce270b7dd))
