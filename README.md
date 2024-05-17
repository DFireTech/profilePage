# DFireTech Profile page website

This website uses the aafu theme.

## Installation

```shell
git clone https://github.com/DFireTech/profilePage.git
cd profilePage
npm install
hugo server
```

## Build website image

> Edit the tag to be what container registry, user and image name for your image.

```shell
hugo --gc --minify
buildah bud -t docker.io/hakuarise/mkpro:latest .
```

### Test run website image

```shell
podman run -ti --rm --name profilePage -p 8000:80 docker.io/hakuarise/mkpro:latest
```
Load [web page](http://localhost:8000)

### Push image to container repo

```shell
podman push docker.io/hakuarise/mkpro:/latest
```

#### Pull image on another machine

```shell
podman pull docker.io/hakuarise/mkpro:/latest
```

## Getting started

After cloning this repo, modify the `config.yaml` as you wish.

### The config file

You'll find a file called `config.yaml`. Customize it per your need.

Note that the sections to be displayed in the accordion, the order of the sections, and the section that should be expanded at the beginning can be specified in the `config.yaml`.

### Add your photo

Go to `static/images` and replace the `profile.jpg` with your own file.

### Theme Colors

The `aafu` theme provides `light` and `dark` theme.

## Reporting Issues

If you have discovered a bug or have a feature request, [create an issue on aafu theme](https://github.com/darshanbaral/aafu/issues/new).
