# github-package-demo
```sh
export GH_USERNAME="529149"
export GH_TOKEN=""
export GH_IMAGE_NAME="hello-world"
export GH_VER="1.0.0"
export TAG_NAME="ghcr.io/$GH_USERNAME/$GH_IMAGE_NAME:$GH_VER"
```
- **Note:** Personal Access Token (PAT) not allowed to push, it will throws error by secret scanning

## step 1: login docker
> echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

## step 2: tag docker image to ghcr.io
> docker tag hello-world:latest ghcr.io/529149/hello-world:1.0.0
> or docker tag hello-world:latest $TAG_NAME

## step 3: push docker image to ghcr.io
> docker push ghcr.io/529149/hello-world:1.0.0
> or docker push $TAG_NAME
