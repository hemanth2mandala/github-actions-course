# GitHub Actions Workflows, Jobs, and Steps

GitHub Actions is an automation tool that lets you build, test, and deploy code from your GitHub repository. Understanding its core building blocks—workflows, jobs, and steps—is essential for creating effective automation.

## Workflows

A workflow is an automated process that you define in your repository. Workflows are commonly used for continuous integration (CI), continuous deployment (CD), and other automation tasks.

Key aspects of workflows:

- **Triggers:** Workflows run in response to events such as pushes, pull requests, or scheduled events. You define when and how a workflow runs. See [Workflow events](../02-workflow-events/Readme.md) for more information.
- **YAML configuration:** Workflows are defined in YAML files, such as `.github/workflows/main.yml`. The configuration specifies the workflow's name, triggers, jobs, and steps.

## Jobs

A job is a unit of work within a workflow. A workflow can contain multiple jobs that run in parallel or sequentially.

- **Runner environment:** Each job specifies the environment it runs on, such as Ubuntu, macOS, or Windows.
- **Parallelism:** Jobs can run concurrently to speed up workflow execution.

## Steps

A step is an individual task within a job. Steps are the smallest building blocks of a workflow and perform the actual work.

- **Name:** A descriptive name identifies the step in the GitHub Actions logs.
- **Run commands:** Steps can execute shell commands or scripts, or invoke actions from GitHub Marketplace or your own repository.
- **Inputs and outputs:** Steps can accept inputs and produce outputs, allowing them to share data with other steps.