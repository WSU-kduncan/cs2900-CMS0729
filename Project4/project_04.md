## Container Technologies

- Container technology 1: Docker
- Container technology 2: Podman 

## Investigate Container Networking

- Docker: 

    i.) Bridge: This is the default network driver. Bridge networks are usually used when your applications run in standalone containers that need to communicate. 

    ii.) Host: This mode is for standalone containers. It will remove network isolation between the container and the Docker host, and use the host’s networking directly.

    iii.) None: For this container, disable all networking. Usually used in conjunction with a custom network driver.

    iiii.) In order to run the container and bind a host port to the container port use this command: `Docker container run -p 8080:80 -d containerName`

- Podman: 

    i.) Bridge: This is the default network driver. It creates a network stack on the default bridge network.

    ii.) None: No networking is set up at all.

    iii.) container:<id>: Uses the same network as another container with ID.

    iiii.) Host: Uses the host’s network stack.

    iiiii.) network-id: Uses a user-defined network.

    iiiiii.) ns:<path>: Joins a network namespace found at path

    iiiiiii.) Private: Creates a new network namespace for the container

    iiiiiiii.) slirp4netns: Creates a user network stack with slirp4netns

    iiiiiiiii.) In order to run the container and bind a host port to the container port use this command: `podman run --add-host=host:ip`

## Investigate Vulnerability Scanners

- Dockerfile Linter:

    i.) [This is a link](https://hadolint.github.io/hadolint/)

    ii.) The best practices hadolint searches for is to validate a Dockerfile to build Docker images that follows this guide (https://docs.docker.com/develop/develop-images/dockerfile_best-practices/).

- Aqua Trivy: 

    i.) The types of vulnerbilities Trivy scans for is container images, file systems, and Git repositories, as well as for configuration issues.

    ii.) From my reasearch I could not find on what limits Trivy had scanning wise. I am sure there are some however. 


    