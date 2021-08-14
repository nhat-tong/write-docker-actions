## Docker based actions

| Advantages        | Disadvantages           |
| ------------- |:-------------:|
| Docker actions package the source code that will be executed right alongside any dependencies that source code has.     | Slower execution time because the image containing your source code and dependencies gets built with every workflow run. |
| Docker containers package the environment with the GitHub Actions code. This creates a more consistent and reliable unit of work because the consumer of the action does not need to worry about the tools or dependencies.      | Docker container actions can only execute in the GitHub-hosted Linux environment.      |
| Ideal for running in environments with very specific configurations and tools.| Debugging can be difficult with containers.     |
| Actions can be written in any language you choose. | More files to maintain when changes to the action occur.      |

## Workflow
  * runs
    * using: docker
    * image: Dockerfile