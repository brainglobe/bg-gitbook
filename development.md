---
description: Instructions and conventions for developing BrainGlobe projects
---

# Development

## Dependency support
Packages have to choose which versions of dependencies they officially support,
with minimum supported versions of each dependency used in continuous
integration testing. BrainGlobe projects should follow
[NEP 29 — Recommend Python and NumPy version support as a community policy
standard](https://numpy.org/neps/nep-0029-deprecation_policy.html) to
determine the **minimum** set of supported package versions:

- The last 42 months of Python releases
- The last 24 months of NumPy releases

In addition to this the last 24 months of other dependencies should also be
supported.

## Releasing `cellfinder-core`

1. Make sure you have [`bump2version`](https://github.com/c4urself/bump2version/#installation) installed.
2. Check out the latest `main` branch from upstream.
3. Run `bump2version <type>`, where `<type>` is replaced by one of {major, minor, patch}. This will create a new pre-release commit and tag with "rc" in
the filename.
4. Push the result to the cellfinder-core repository using `git push upstream --follow-tags`.
5. Check that all the tests pass, the package builds correctly, and that all built packages are uploaded to PyPi.
6. Check that there are no issues with the new version of `cellfinder-core` and `cellfinder` by going to https://github.com/brainglobe/cellfinder/actions/workflows/test_and_deploy.yml, clicking on the "Run workflow" button the left, typing "true" into the prompt, and clicking "Run workflow". This will run the `cellfinder` tests with the development version of `cellfinder-core`. Make sure these tests pass.
7. If something goes wrong, fix the issues, run `bump2version rc` to create a new release candidate. Push to upstream again, and go back to step 5.
8. Run `bump2version <type>` to tag the final release version, and push to upstream.
9. Check that all the tests pass, the package builds correctly, and that all built packages are uploaded to PyPi.
10. Tag the new version using `bump2version --current-version X.Y.Z-rcN --new-version X.Y.Z <type>` and push to upstream.
