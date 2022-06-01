# Docker & Podman

## Why Podman is more secure (https://medium.com/@ganeshmani009/replacing-docker-with-podman-power-of-podman-cloudnweb-23cfb7541538)

### Daemon makes the copy of images in the local container and maintains it. Essentially the Docker daemon does all the work with registries, images, containers, and the kernel. The Docker command-line interface (CLI) asks the daemon to do this on your behalf.
you can ask me, what is the problem with it. Actually, there are few,
- A single process could be a single point of failure.
- This process owned all the child processes (the running containers).
- If there is any failure in the docker daemon, then every child processes are lost its track.
- Building containers led to security vulnerabilities.
- All Docker operations had to be conducted by a user (or users) with the same full root authority.

Podman directly interact with Image registry, containers and image storage. with Linux kernel through the runC container runtime process (not a daemon).

