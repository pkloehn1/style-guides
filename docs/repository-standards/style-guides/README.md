# Style Guides

This directory contains style guides gathered from all repositories owned by this organization/user.

## How It Works

The [`gather-style-guides.yml`](../../../.github/workflows/gather-style-guides.yml) GitHub Actions workflow automatically discovers and copies style guide files from all accessible repositories into this directory.

Each file in this directory is named after its source repository using the pattern `owner--repo.md` (e.g., `acme-org--my-repo.md`). Using the full `owner/repo` path (with `/` replaced by `--`) prevents filename collisions when repositories from different owners share the same name.

## Prerequisites

To access **private** repositories, a [Personal Access Token (classic)](https://github.com/settings/tokens) with the `repo` scope must be created and stored as a repository secret named **`STYLE_GUIDES_PAT`**.

## Running Manually

You can trigger the workflow manually from the [Actions tab](../../../actions/workflows/gather-style-guides.yml) by clicking **Run workflow**.

## Supported Style Guide File Locations

The workflow searches for style guide files at the following paths within each repository:

- `STYLE_GUIDE.md`
- `docs/STYLE_GUIDE.md`
- `docs/style-guide.md`
- `.github/STYLE_GUIDE.md`
- `CONTRIBUTING.md` (if no other style guide is found)
