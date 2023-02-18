# Chapter 3 Assignment 2 Bitcoin Technology

## Implementing a Bitcoin Network using Bitcoin RPC

### Run the code

To run the notebook file, do the following.

1. Build the docker image

```bash
docker image build -t bitcoin-core .
```

2. After succesfully building the image, run the docker image

```bash
docker run -it --rm -p 8888:8888 -v ${PWD}:/code "bitcoin-core"
```

This will run the jupyter notebook on the port `8888`.

3. Remove the containers afterward.

```bash
docker container stop [container_id]
docker system prune
```

`[container_id]` can be obtained by running the command `docker container ls`

4. Remove the image

```bash
docker image rm [image_id]
```

`[image_id]` can be obtained by running the command `docker image ls`
