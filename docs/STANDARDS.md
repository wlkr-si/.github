# Studio standards

These are defaults for WLKR.SI projects. Existing project instructions, licenses and release processes take precedence.

## A useful front door

A README says what the project does, shows a real example and gives the shortest working start. Name platform requirements and current limitations. Link documentation, issue reporting and the actual license. Use the [WLKR.SI family badge](https://wlkr.si/brand) while retaining the project's own identity.

## Small changes with evidence

Keep each change focused and reversible. Check behavior that could break, including failure paths. Run the project's checks and report what passed and what was skipped. Never weaken a check to make a release pass. Record the source commit for a release.

## Ship, then check

Use existing infrastructure and the project's documented release process. Save the previous working release before changing a live service. Check the deployed version and the user action at the live address. Undo a failed release before starting more work. A local test, upload receipt and live result are different kinds of evidence.

## Design with intent

Use the existing brand and components. Make the primary action obvious. Keep layouts useful on a phone, with a keyboard and with reduced motion. Cut copy that repeats the layout. Use real examples; do not present mock data or planned features as working products.

## Honest maintenance

Describe released, experimental and unavailable capabilities accurately. Keep known limitations, install instructions and compatibility current. Preserve upstream attribution and project-specific licensing. Do not publish private source or make support, legal status or availability claims without evidence.

## Respect resources

Use the existing local-first checks. Do not enable paid hosted runners or add services as a side effect of a contribution. Keep credentials outside source and browser bundles. Remove disposable builds and recordings after verification; preserve source, active work and user data.
