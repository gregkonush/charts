# Helm Charts for Self-Hosted Projects

This repository contains a collection of Helm charts for various self-hosted applications and services.

## Usage

1. **Add the Helm repository:**

   ```bash
   helm repo add selfhosted https://gregkonush.github.io/charts
   helm repo update
   ```

   _(Replace `<your-repo-name>` with a name you prefer, e.g., `selfhosted`)_

2. **Search for available charts:**

   ```bash
   helm search repo selfhosted
   ```

3. **Install a chart:**

   ```bash
   helm install my-release selfhosted/affine
   ```

   _(Replace `my-release` with your desired release name and `<chart-name>` with the chart you want to install)_

## Automation

Chart releases are automatically managed via GitHub Actions using [helm/chart-releaser-action](https://github.com/helm/chart-releaser-action).
When changes to charts are pushed to the `main` branch, the workflow will:

- Lint the chart.
- Package the chart.
- Create/update a GitHub Release.
- Update the `index.yaml` on the `gh-pages` branch.
