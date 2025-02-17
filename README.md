# SHocker

**SHocker** is a basic container runtime written in Bash shell. It provides simple commands to create, run, list, delete, and prune containers based on Docker images. This project is intended as a learning tool and is not recommended for production use.

## Features

- **Create** a container from a Docker image
- **Run** commands inside a container
- **List** all containers or images
- **Delete** specific containers or images
- **Prune** all containers and images with confirmation

## Requirements

- Bash shell
- `curl` to pull from the Docker Hub
- `jq` for parsing JSON results from curl
- `tar` for extracting image layers
- `sudo` for certain operations

## Installation

Clone the repository and navigate to the project directory:

```bash
git clone https://github.com/beehivesystems/shocker.git
cd shocker
chmod +x shocker
```

## Usage

### Pull an Image

To pull an image from the Docker Hub:

```bash
./shocker pull <image:tag>
```

### Create a Container

To create a new container from a Docker image:

```bash
./shocker create <image:tag>
```

### Run a Command in a Container

To run a command inside an existing container:

```bash
./shocker run <container_id> <cmd>
```

Example:

```bash
./shocker run 1234567890 /bin/sh -c "echo Hello from SHocker."
```

### List All Containers

To list all containers:

```bash
./shocker container ls
```

### Delete a Container

To delete a specific container:

```bash
./shocker container rm <container_id>
```

### Delete an Image

To delete a specific image:

```bash
./shocker image rm <image:tag>
```

### Prune All Containers and Images

To remove everything:

```bash
./shocker prune
```

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request.

## Disclaimer

SHocker is a simple, educational tool and should not be used in production environments. It is designed to demonstrate basic container operations and is not secure or optimized for performance or stability.

## License

This project is licensed under the MIT license.
