# Build && Deploy To Github

## Deploy to github

/bin/bash ./deploy-helper.sh -i ghcr.io/kicad/kicad

### Login to Github

1. Create a new personal access token (classic) with the appropriate scopes for the tasks you want to accomplish. If your organization requires SSO, you must enable SSO for your new token.

2. Save your personal access token (classic). We recommend saving your token as an environment variable.

```bash

export CR_PAT=YOUR_TOKEN

```

3. Using the CLI for your container type, sign in to the Container registry service at ghcr.io.

```bash

$ echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin

```

> Login Succeeded

### Pushing container images

docker push ghcr.io/NAMESPACE/IMAGE_NAME:latest

## Push existing container images && Build

### Pushing existing container images

docker pull ghcr.io/kicad/kicad

docker tag kicad:latest ghcr.io/liangtie/kicad:latest

docker push liangtie/kicad:latest

### Build container images

docker build - < Dockerfile.cli-server

## References

1. https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry
2. https://stackoverflow.com/questions/48038969/an-image-does-not-exist-locally-with-the-tag-while-pushing-image-to-local-regis
