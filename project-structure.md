# GitHub Actions Quick guide:

![screenshot](/assets/appScreanShot2.JPG)

## What is github actions and its key features

1. workflow contains one or more jobs which can run in sequential order or in parallel.
2. **Each job will run inside its own virtual machine runner, or inside a container**.
3. jobs has one or more steps that either run a script that you define or run an action, which is a reusable extension that can simplify your workflow.
4. **Workflows** are defined by a YAML file checked in to your repository
5. **Workflows** will run when triggered by an event in your repository, or they can be triggered manually, or at a defined schedule.
6. **Workflows** are defined in the .github/workflows directory in a repository.
7. repository can have multiple workflows, each of which can perform a different set of tasks. For example:
    - you can have one workflow to build and test pull requests
    - another workflow to deploy your application every time a release is created
    - and still another workflow that adds a label every time someone opens a new issue.
8. You can reference a workflow within another workflow.
9. An **event** is a specific activity in a repository that triggers a workflow run. For example:
    - activity can originate from GitHub when someone creates a pull request, opens an issue, or pushes a commit to a repository.
    - You can also trigger a workflow to run on a schedule, by posting to a REST API, or manually.
10. A **job** is a set of steps in a workflow that is executed on the same runner. Each step is either a shell script that will be executed, or an action that will be run. Steps are executed in order and are dependent on each other. Since each step is executed on the same runner, you can share data from one step to another.
11. You can configure a job's dependencies with other jobs; by default, jobs have no dependencies and run in parallel with each other. When a job takes a dependency on another job, it will wait for the dependent job to complete before it can run.
12. An **action** is a custom application for the GitHub Actions platform that performs a complex but frequently repeated task.
    - Use an action to help reduce the amount of repetitive code that you write in your workflow files.
    - An action can pull your git repository from GitHub, set up the correct toolchain for your build   environment, or set up the authentication to your cloud provider.
    - You can write your own actions, or you can find actions to use in your workflows in the GitHub Marketplace.
13. A **runner** is a server that runs your workflows when they're triggered.
    - Each runner can run a single job at a time. GitHub provides Ubuntu Linux, Microsoft Windows, and macOS runners to run your workflows
    - **each workflow run executes in a fresh, newly-provisioned virtual machine.**
    - If you need a different operating system or require a specific hardware configuration, you can host your own runners.
14. GitHub provides starter workflows for a variety of languages and tooling.


