# DEV

## Deploy Token in docker build

It's not an issue to use the clean DEPLOY_TOKEN_PASSWORD in the docker builds, because it's a multi-stage build so it's not kept in the image history.

## Docker build args

Couldn't find the way to pass multiple parameters on the same building arg, for example the ldFlags of go build. Thats why we use separate variables and build the ldFlags inside the Dockerfile instead of just passing BUILD_ARGS all together.
