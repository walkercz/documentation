---
id: start
title: Configuration
description: "Configuration"
---

:::info
_This page assumes you have already completed the [installation](/docs/installation/prerequisites)_
:::

Nothing happen after installation without configuration.

### 1. create personal access token on git
go to your github account > settings > developer settings > Personal access tokens
https://github.com/settings/tokens
create new token just named it and create

### 2. save your token to secrets.yaml
copy token to your secrets.yaml
```yaml
HACS_gihub: your token from github
```
### 3. configure HACS
copy this to your configuration.yaml
```yaml
hacs:
    token: !secret HACS_gihub
    appdeamon: true
    python_script: true
    theme: true
```

### 4. restart your HA

:::tip
Read [this FAQ](/docs/faq/initial_startup) about the first startup of HACS.
:::
