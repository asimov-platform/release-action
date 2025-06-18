# `asimov-platform/release-action`

A simple action to download all artifacts from previous builds, parse [keep a changelog](https://keepachangelog.com) file and release a new version.

You probably want to use this action in combination with [asimov-platform/rust-build-action](https://github.com/asimov-platform/rust-build-action), or something similar.

## Preview

![Preview](assets/preview.png?raw=true)

## Features

- Can generate a GitHub token for the app.
- Downloads all artifacts.
- Computes checksums for all files.
- Parses [keep a changelog](https://keepachangelog.com).
- Creates a new release.

## Usage

### Inputs

```yaml
inputs:
  # App ID.
  # Default: ''
  app_id:
  # App private key.
  # Default: ''
  app_private_key:
  # GitHub token used to create the release.
  # Default: ${{ github.token }}
  token:
  # Path to changelog file.
  # Default: CHANGELOG.md
  changelog-path:
  # Compute checksum for each file?
  # Default: true
  compute-checksum:
```

### Outputs

```yaml
outputs:
  # github.com URL for the release.
  url:
  # ID of the release.
  id:
  # URL to upload assets to.
  upload_url:
  # JSON array containing information about each uploaded asset.
  assets:
```
