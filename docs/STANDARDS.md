# Studio standards

These are defaults for WLKR.SI projects. Existing project instructions, licenses and release processes take precedence.

## A useful front door

A README says what the project does, shows a real example and gives the shortest working start. Name platform requirements and current limitations. Link documentation, issue reporting and the actual license. Use the [WLKR.SI family badge](https://wlkr.si/brand) while retaining the project's own identity.

## Small changes with evidence

Keep each change focused and reversible. Check behavior that could break, including failure paths. Run the project's checks and report what passed and what was skipped. Never weaken a check to make a release pass. Record the source commit for a release.

## Checks you can run

Start from the repository root and follow its README to install the pinned tools and dependencies. These public workflows run for pull requests and changes to `main`:

| Project | Local check | Runtime checked in CI | Results and exact workflow |
| --- | --- | --- | --- |
| [wlkr/ui](https://github.com/wlkr-si/ui) | `pnpm release:check` | Node 26.8.2, pnpm 11.15.0 | [Latest runs](https://github.com/wlkr-si/ui/actions/workflows/release-check.yml) · [Verified definition](https://github.com/wlkr-si/ui/blob/b4e5f27bd19d913846a32af0db98fc748f749648/.github/workflows/release-check.yml) |
| [starter](https://github.com/wlkr-si/starter) | `npm ci` then `npm run verify` | Node 24.22.3 and 26.8.2 | [Latest runs](https://github.com/wlkr-si/starter/actions/workflows/verify.yml) · [Verified definition](https://github.com/wlkr-si/starter/blob/0ca2ecfadb6523cb2936173b5ecf93159e33aa7b/.github/workflows/verify.yml) |
| [studio-check](https://github.com/wlkr-si/studio-check) | `node --test *.test.mjs`; for MCP: `npm ci --prefix mcp` then `npm --prefix mcp test` | Node 24.22.3 and 26.8.2 | [Latest runs](https://github.com/wlkr-si/studio-check/actions/workflows/verify.yml) · [Verified definition](https://github.com/wlkr-si/studio-check/blob/9691072e620c3ef0c9d2131bf9baf7d5a908470b/.github/workflows/verify.yml) |

The linked definitions were verified against successful `main` runs on November 12, 2026. Open the latest run for its current result. Application deployments use their own live checks and undo process; a successful source workflow does not publish a release. Keep this table aligned when a project's documented checks change.

## Ship, then check

Use existing infrastructure and the project's documented release process. Save the previous working release before changing a live service. Check the deployed version and the user action at the live address. Undo a failed release before starting more work. A local test, upload receipt and live result are different kinds of evidence.

## Design with intent

Use the existing brand and components. Make the primary action obvious. Keep layouts useful on a phone, with a keyboard and with reduced motion. Cut copy that repeats the layout. Use real examples; do not present mock data or planned features as working products.

## Honest maintenance

Describe released, experimental and unavailable capabilities accurately. Keep known limitations, install instructions and compatibility current. Preserve upstream attribution and project-specific licensing. Do not publish private source or make support, legal status or availability claims without evidence.

## Respect resources

Use the existing local-first checks. Do not enable paid hosted runners or add services as a side effect of a contribution. Keep credentials outside source and browser bundles. Remove disposable builds and recordings after verification; preserve source, active work and user data.
