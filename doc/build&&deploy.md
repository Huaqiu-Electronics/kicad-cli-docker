# Build && Deploy To Github

## Build

docker build . -t wandb/openui --load
docker run -p 7878:7878 -e OPENAI_API_KEY wandb/openui

    - docker build --pull -t kicad:build-temp -f ${DOCKERFILE_PATH} --build-arg="KICAD_VERSION=${VERSION}" .

## Deploy to github

/bin/bash ./deploy-helper.sh -i ghcr.io/kicad/kicad
