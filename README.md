## Docker based actions

| Advantages        | Disadvantages           |
| ------------- |:-------------:|
| Docker actions package the source code that will be executed right alongside any dependencies that source code has.     | Slower execution time because the image containing your source code and dependencies gets built with every workflow run. |
| Docker containers package the environment with the GitHub Actions code. This creates a more consistent and reliable unit of work because the consumer of the action does not need to worry about the tools or dependencies.      | Docker container actions can only execute in the GitHub-hosted Linux environment.      |
| Ideal for running in environments with very specific configurations and tools.| Debugging can be difficult with containers.     |
| Actions can be written in any language you choose. | More files to maintain when changes to the action occur.      |

## Workflow

| Component        | Description           |
| ------------- |:-------------:|
| Action     | Individual tasks that you combine as steps to create a job. Actions are the smallest portable building block of a workflow. To use an action in a workflow, you must include it as a step. |
| Artifact      | Artifacts are the files created when you build and test your code. Artifacts might include binary or package files, test results, screenshots, or log files. Artifacts can be used by the other jobs in the workflow or deployed directly by the workflow.      |
| Event | A specific activity that triggers a workflow run.      |
| Job | A defined task made up of steps. Each job is run in a fresh instance of the virtual environment. Jobs can run at the same time in parallel or be dependent on the status of a previous job and run sequentially.     |
| Runner | Any machine with the GitHub Actions runner application installed. You can use a runner hosted by GitHub or host your own runner. A runner waits for available jobs. Runners run one job at a time reporting the progress, logs, and final result back to GitHub.      |
| Step | A step is a set of tasks performed by a job. Steps can run commands or actions.      |
| Virtual Environment | The virtual environment of a GitHub-hosted runner includes the virtual machine's hardware configuration, operating system, and installed software.      |
| Workflow | A configurable automated process that you can set up in your repository. Workflows are made up of one or more jobs and can be scheduled or activated by an event.      |

![workflow](https://camo.githubusercontent.com/fd0a925f56ff417c793c7b84e3cd3998cfff191e6cc2a897f184c42c1ae9c6af/68747470733a2f2f692e696d6775722e636f6d2f437778476f62682e706e67)

  * runs
    * using: docker
    * image: Dockerfile