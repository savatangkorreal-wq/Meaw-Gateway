# Meaw Gateway

Official release distribution for Meaw Gateway, with Khmer / English UI and verified automatic updates.

## Download / ទាញយក

[Download the latest release](https://github.com/savatangkorreal-wq/Meaw-Gateway/releases/latest)

- New installation: choose `Meaw-Gateway-VERSION-Full.zip`, extract to a new folder, install Python 3.12, and open `run.bat`.
- Existing installation using the new launcher: choose **Update Now** inside the dashboard. Accounts and settings stay in `data/`; `.env` is not replaced.
- Do not extract a Full ZIP over an existing installation. Legacy installations need the launcher/bootstrap upgrade once.

## Automatic updates

The app uses this stable manifest URL:

```text
https://github.com/savatangkorreal-wq/Meaw-Gateway/releases/latest/download/version.json
```

Downloads are checked against the manifest SHA-256 and size before staging. The launcher drains active requests, installs app files, restarts, and restores the previous app if startup fails.

Each release contains the Full ZIP, Update ZIP, and version.json. GitHub-generated Source code archives contain this distribution repository, not the application installer.

## Account configuration

Releases contain no user accounts, API keys, or OAuth client secrets. Add your own accounts after installing. Google sign-in requires local OAuth client configuration described in the packaged README. Existing literal OAuth credentials are migrated locally from the previous app during an in-app update.

## Publishing future versions

Build a higher semantic version with the project’s `build_distributable_package.py`, set the HTTPS asset URL, and fill both release notes in the generated manifest. Upload all three assets to a draft release, then publish it as the latest release. Keep published version assets immutable; publish a new version for changes.
