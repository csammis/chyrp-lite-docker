# chyrp-lite-docker

A customized Dockerfile describing an image that is based on Chyrp Lite with theme customizations.

https://github.com/xenocrat/chyrp-lite

https://chyrplite.net/

## Why is this?

We self-host multiple blogs running Chyrp Lite with modified built-in themes and it's a pain in the rear to keep them updated.
The official instructions state that to update an installation, just copy the contents of the Github repo into the webroot - or, if using Docker, copy the contents of the Github repo and then run the Compose file from the repo to build an image from those copied repo contents. That doesn't really fit with the rest of our self-hosted services, where a `docker compose pull` is sufficient to spin up new blogs and bring in updates without having to muck around with copying customized files around.

Fact is, this _still_ doesn't make it that easy on account of we haven't set up Github actions to publish this image for real, but at least we don't have to worry about remembering to copy around the customized theme files anymore.
