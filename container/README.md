# OCI Container

## Local Build Instructions

To build run the following in the root of the repository.

```sh
sudo docker build . -t ibex -f container/Dockerfile
```

## Using the Container

To run the container,
use the following command in the root of the repository.

```sh
podman run --rm \
  -p 6080:6080
  -p 3333:3333 \
  -v $(pwd):/home/dev/demo:Z \
  ibex
```

To access the container go to [http://localhost:6080](http://localhost:6080).
