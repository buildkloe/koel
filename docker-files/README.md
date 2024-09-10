Docker build workflow

## Create release

Add tag

git push origin smart-playlist-using-liked
git tag v6.12.1-liked-pl
git push --tags

Goto https://github.com/buildkloe/koel/releases publish release

## Build

git checkout ship

Update Dockerfile by changing the ARG KOEL_VERSION_REF=v6.12.1-liked-pl

git push

## Deploy

Go to appfx
ship pull && ship stop && ship up -d

