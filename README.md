# Native Java PrairieLearn course

Generated from [Java](https://github.com/BSU-RFCT-Afonenko-Courses/Java) source
`1265471489234fc8fe1445c0f20c38b81a2d4a17` by platform builder
`42ba43eba6e206f42c55206aa7a8f3d107d37ee6`. Content and image hashes are in
[provenance.json](provenance.json). Two independent exports are byte-identical.

The pilot uses one standard native Java code editor and the actual JDK25 grader.
The full local author project is in the source repository; download/upload
controls, README, Examples and .gitignore are absent from this native question.
The server-side tests are non-confidential demonstration fixtures already in
the public Java source commit, copied byte-for-byte. They check the published
Unicode contract (17 fixed string/boundary cases). No exam bank, identities,
submissions, credentials or runtime data is included. The reference solution
is not published. Do not edit generated course files manually.

The PL exporter is pinned to owner candidate11a6c73 (PR11), installed as a whole
package. The minor release is not yet published. Enrollment/publishing and
Moodle authentication require separate configuration; real Moodle is a final
stage. No production Student ACL acceptance is claimed.

## Local runtime from published sources

This selected-work delivery has no hidden laptop files. The required platform
and grader source is pinned to public platform commit
`42ba43eba6e206f42c55206aa7a8f3d107d37ee6`; its Dockerfile pins the Temurin25
base digest. For this development pilot the grader name is a **local build tag**,
not a claimed published registry image. Prepare it before starting PL:

```sh
git clone https://github.com/Afonenko-Course-Tools/prairielearn-platform platform
git -C platform checkout --detach 42ba43eba6e206f42c55206aa7a8f3d107d37ee6
docker build -t ghcr.io/afonenko-course-tools/java25-grader:pilot-local-20261008-r2 \
  platform/images/java25-grader
```

Use the platform's pinned PL image and `compose.dev.yml`. Supply this repository
as a read-only `/course` bind (or use exact registry storage as documented in
platform `docs/development.md`), and create a private absolute jobs directory.
The dev config uses synthetic identities and disables grader image pulling, so
PL uses the local build. Load from disk must finish successfully. Initial
course/instance publishing and enrollment are explicit settings; a staff test
can run the pilot in preview immediately. No actual Moodle credentials are
needed for this local path. Docker/network/runtime dependencies are declared
in the pinned platform source; no generated course file needs manual editing.

Course conditions, server-side checks and assessment policy are intentionally
public. Credentials and real user data belong outside the course repository.
