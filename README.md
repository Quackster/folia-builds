# folia-builds (weekly GitHub Actions releases)

This repository contains a GitHub Actions workflow that **automatically builds PaperMC’s Folia** and publishes the compiled **paperclip JARs** as **GitHub Releases**.

It builds **two targets** every run:

- **Default branch build** → uploaded as an asset prefixed with **`[main]`**
- **Latest `dev` branch build** → uploaded as an asset prefixed with **`[dev]`**

Both assets are attached to the **same release** for easy download.

## Schedule / Triggers

This workflow runs:

- **Weekly via cron:** `0 12 * * 4` (every **Thursday at 12:00 UTC**)
- **Manually:** via **Actions → Run workflow** (`workflow_dispatch`)

> Push / PR triggers are present but commented out in the workflow.
