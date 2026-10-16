# GitHub Actions Workflow Events

GitHub Actions workflows are triggered by events in your repository. These events determine when a workflow runs, helping automate tasks such as continuous integration, testing, and deployment.

Here are some common workflow triggers.

## Push

Run a workflow when code is pushed to a specific branch.

```yaml
on:
  push:
    branches:
      - main
      - release/*
```

## Pull request

Run a workflow when a pull request is opened, updated, or synchronized.

```yaml
on:
  pull_request:
    branches:
      - main
```

## Schedule

Run workflows at specific times or intervals using cron expressions. This example runs every day at midnight UTC.

```yaml
on:
  schedule:
    - cron: '0 0 * * *'
```

## Issue comment

Run a workflow when a comment is created on an issue or pull request.

```yaml
on:
  issue_comment:
    types:
      - created
```

## Webhook

Run a workflow in response to custom webhook payloads sent to your repository.

```yaml
on:
  repository_dispatch:
    types:
      - my-custom-event
```

## Manual trigger

Allow a workflow to be run manually through the GitHub Actions UI or API.

```yaml
on:
  workflow_dispatch:
```

These triggers can be customized to suit your project and automate workflows based on specific events and conditions. See the [GitHub Actions events documentation](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows) for the full list of available events.