github-action-deploy
======

Composite GitHub Action to deploy a brdgm.me application.

Usage example:

```yaml
name: Deploy

on:
  push:
    branches:
      - master
  workflow_dispatch:

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - uses: brdgm/github-action-deploy@v1
        with:
          gh-site-deploy-pat: ${{ secrets.GH_SITE_DEPLOY_PAT }}
          gh-site-deploy-username: ${{ secrets.GH_SITE_DEPLOY_USERNAME }}
          gh-site-deploy-email: ${{ secrets.GH_SITE_DEPLOY_EMAIL }}
          gh-site-deploy-name: ${{ secrets.GH_SITE_DEPLOY_NAME }}
```
