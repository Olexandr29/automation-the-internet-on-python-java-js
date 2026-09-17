# Docker Fundamentals

## Images and Containers

A Docker image is a read-only template used to create containers.

A Docker container is a runnable instance of a Docker image.

## Basic Docker Commands

### Verify Docker installation

```bash
docker --version
````

Displays the installed Docker version.

```bash
docker info
```

Displays detailed information about the Docker Engine and environment.

### Download an image

```bash
docker pull nginx
```

Downloads the `nginx` image from Docker Hub.

### List images

```bash
docker images
```

Displays locally available Docker images.

### Create and run a container

```bash
docker run -d --name my-nginx nginx
```

Creates and starts a container named `my-nginx` from the `nginx` image.

* `-d` — runs the container in detached mode.
* `--name my-nginx` — assigns a custom name to the container.

### List running containers

```bash
docker ps
```

Displays currently running containers.

### List all containers

```bash
docker ps -a
```

Displays running and stopped containers.

### Stop a container

```bash
docker stop my-nginx
```

Stops the running `my-nginx` container.

### Remove a container

```bash
docker rm my-nginx
```

Removes the stopped `my-nginx` container.

## Basic Container Lifecycle

```text
nginx image
    ↓
docker run
    ↓
running container
    ↓
docker stop
    ↓
stopped container
    ↓
docker rm
    ↓
container removed
```

## Practice Summary

The following Docker workflow was successfully completed:

1. Verified Docker installation and Docker Engine.
2. Pulled the `nginx` image.
3. Created and started the `my-nginx` container.
4. Inspected running containers.
5. Inspected all containers.
6. Stopped the container.
7. Verified the stopped container.
8. Removed the container.
9. Verified that the container was removed while the `nginx` image remained available.


<details><summary>Practical details - terminal log</summary>

```Windows PowerShell

PS C:\Users\User\Desktop> docker --version
Docker version 29.7.2, build a7dcaa6
PS C:\Users\User\Desktop> docker info
Client:
 Version:    29.7.2
 Context:    desktop-linux
 Debug Mode: false
 Plugins:
  agent: Docker AI Agent Runner (Docker Inc.)
    Version:  v1.127.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-agent.exe
  ai: Docker AI Agent - Ask Gordon (Docker Inc.)
    Version:  v1.30.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-ai.exe
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.36.1-desktop.1
    Path:     C:\Users\User\.docker\cli-plugins\docker-buildx.exe
  compose: Docker Compose (Docker Inc.)
    Version:  v5.5.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-compose.exe
  debug: Get a shell into any image or container (Docker Inc.)
    Version:  0.0.47
    Path:     C:\Users\User\.docker\cli-plugins\docker-debug.exe
  desktop: Docker Desktop commands (Docker Inc.)
    Version:  v0.4.3
    Path:     C:\Users\User\.docker\cli-plugins\docker-desktop.exe
  dhi: CLI for managing Docker Hardened Images (Docker Inc.)
    Version:  v0.0.7
    Path:     C:\Users\User\.docker\cli-plugins\docker-dhi.exe
  extension: Manages Docker extensions (Docker Inc.)
    Version:  v0.2.31
    Path:     C:\Users\User\.docker\cli-plugins\docker-extension.exe
  init: Creates Docker-related starter files for your project (Docker Inc.)
    Version:  v1.4.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-init.exe
  mcp: Docker MCP Plugin (Docker Inc.)
    Version:  v0.43.3
    Path:     C:\Users\User\.docker\cli-plugins\docker-mcp.exe
  model: Docker Model Runner (Docker Inc.)
    Version:  v1.2.6
    Path:     C:\Users\User\.docker\cli-plugins\docker-model.exe
  offload: Docker Offload (Docker Inc.)
    Version:  v0.6.13
    Path:     C:\Users\User\.docker\cli-plugins\docker-offload.exe
  pass: Docker Pass Secrets Manager Plugin (beta) (Docker Inc.)
    Version:  v0.2.2
    Path:     C:\Users\User\.docker\cli-plugins\docker-pass.exe
  sandbox: "docker sandbox" is deprecated, use Docker Sandboxes instead (Docker Inc.)
    Version:  v0.13.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-sandbox.exe
  scout: Docker Scout (Docker Inc.)
    Version:  v1.24.0
    Path:     C:\Users\User\.docker\cli-plugins\docker-scout.exe

Server:
 Containers: 0
  Running: 0
  Paused: 0
  Stopped: 0
 Images: 1
 Server Version: 29.7.2
 Storage Driver: overlayfs
  driver-type: io.containerd.snapshotter.v1
 Logging Driver: json-file
 Cgroup Driver: cgroupfs
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 CDI spec directories:
  /etc/cdi
  /var/run/cdi
 Discovered Devices:
  cdi: docker.com/gpu=webgpu
 Swarm: inactive
 Runtimes: io.containerd.runc.v2 nvidia runc
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: aad11006b869517fcd3009450b6f82da282e1a9b
 runc version: v1.4.3-0-gbb14dabe
 init version: de40ad0
 Security Options:
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 6.18.33.2-microsoft-standard-WSL2
 Operating System: Docker Desktop
 OSType: linux
 Architecture: x86_64
 CPUs: 8
 Total Memory: 3.705GiB
 Name: docker-desktop
 ID: a2abf1ff-1233-4f83-a68b-502b87f3c436
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 HTTP Proxy: http.docker.internal:3128
 HTTPS Proxy: http.docker.internal:3128
 No Proxy: hubproxy.docker.internal
 Labels:
  com.docker.desktop.address=npipe://\\.\pipe\docker_cli
 Experimental: false
 Insecure Registries:
  hubproxy.docker.internal:5555
  ::1/128
  127.0.0.0/8
 Live Restore Enabled: false
 Firewall Backend: iptables

PS C:\Users\User\Desktop> docker pull nginx
Using default tag: latest
latest: Pulling from library/nginx
3fe5ab3f8614: Pull complete
0478569e858e: Pull complete
76225461b7d3: Pull complete
9302921ce9b3: Pull complete
c06193164a25: Pull complete
ab606a349520: Pull complete
d18f12d40fc4: Download complete
59379d3e12b2: Download complete
Digest: sha256:d0d674272be3be36f9a13d79194fa0db5aa630ab3ede9bec459d12f67370aaef
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest
PS C:\Users\User\Desktop> docker images
                                                i Info →   U  In Use
IMAGE               ID             DISK USAGE   CONTENT SIZE   EXTRA
docker/welcome-to-docker:latest
                    c4d56c24da4f       22.2MB         6.03MB
nginx:latest        d0d674272be3        253MB         69.2MB
PS C:\Users\User\Desktop> docker run -d --name my-nginx nginx
3266e6842b3fe59aafdfd205dfaee4df885d63977b677096a3fda7fae4c9429d
PS C:\Users\User\Desktop> docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS     NAMES
3266e6842b3f   nginx     "/docker-entrypoint.…"   20 seconds ago   Up 20 seconds   80/tcp    my-nginx
PS C:\Users\User\Desktop> docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS              PORTS     NAMES
3266e6842b3f   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute   80/tcp    my-nginx
PS C:\Users\User\Desktop> docker stop my-nginx
my-nginx
PS C:\Users\User\Desktop> docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
PS C:\Users\User\Desktop> docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS                      PORTS     NAMES
3266e6842b3f   nginx     "/docker-entrypoint.…"   2 minutes ago   Exited (0) 20 seconds ago             my-nginx
PS C:\Users\User\Desktop> docker rm my-nginx
my-nginx
PS C:\Users\User\Desktop> docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
PS C:\Users\User\Desktop> docker images
                                               i Info →   U  In Use
IMAGE              ID             DISK USAGE   CONTENT SIZE   EXTRA
docker/welcome-to-docker:latest
                   c4d56c24da4f       22.2MB         6.03MB
nginx:latest       d0d674272be3        253MB         69.2MB
PS C:\Users\User\Desktop>

```

</details>