# Publishing checklist for v1.4.0

The package is release-ready, but the repository URL and DOI must be added after the public destinations exist.

1. Create a public GitHub repository named `prophylactic-pelvic-nodal-nnt-comparator` and upload this directory.
2. Run `npm test` and confirm all tests pass.
3. Replace no files: instead, add the final `repository-code` and `url` fields to `CITATION.cff`, and the `repository` field to `package.json`.
4. Connect the GitHub repository to Zenodo and enable archiving for releases.
5. Create and push the signed or annotated tag `v1.4.0`, then publish a GitHub release from that tag.
6. Confirm that Zenodo has archived the release and issued a version DOI.
7. Add the version DOI to `CITATION.cff` as `doi`, add a DOI badge to `README.md`, and record the concept DOI separately for discovery.
8. Correct only metadata in the archived Zenodo record. If software changes, create a new version and release rather than altering the v1.4.0 archive.
9. Verify the public citation by downloading the archive, opening `index.html`, and rerunning `npm test` from the archived source.

## Release record

- GitHub repository: pending
- Git tag: `v1.4.0`
- GitHub release URL: pending
- Zenodo version DOI: pending
- Zenodo concept DOI: pending

