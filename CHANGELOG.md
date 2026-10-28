# Changelog (Dandelion fork)

Changes in `Dandelion-Science/GLMsingle` relative to upstream `cvnlab/GLMsingle`.
`main` tracks upstream; Dandelion changes live on `dandelion-v*` branches.

## dandelion-v1 (from upstream `1ab54a6`, 2025-11-09)

- **Fix:** the run-wise FIR diagnostic and the LSS fit (`wantlss=1`) fitted every
  run with run 1's `extra_regressors` and `maxpolydeg`. With extra regressors and runs
  of different lengths, `fit` crashed. Python and MATLAB; tests in
  `tests/test_per_run_options.py`.
- **Packaging:** `pyproject.toml` + `uv.lock` replace `setup.py` / `MANIFEST.in`. The
  distribution is `dandelion-glmsingle` (import name unchanged: `glmsingle`), versioned
  from git tags with `setuptools_scm`.
- **CI:** `pytest` on Linux and macOS (Python 3.14); `publish` builds and uploads to
  CodeArtifact on GitHub release; Dependabot targets `dandelion-v1`.
