# RealPage Official Docker Image for FPM/Nginx

[![Build Status](https://travis-ci.org/realpage/fpm-nginx.svg?branch=master)](https://travis-ci.org/realpage/fpm-nginx) 
[![Docker Pulls](https://img.shields.io/docker/pulls/realpage/fpm-nginx.svg)](https://hub.docker.com/r/realpage/fpm-nginx)

Sometimes it's best to combine provide a single container for service/app distribution.  These containers include both PHP-FPM and Nginx in a single container.  Other processes can easily be added as well.

## Adding Processes

This container uses [S6 Overlay](https://github.com/just-containers/s6-overlay) as it's process monitoring solution.  Add a new directory to `services.d` with a `run` file in it where `run` in a shell script that kicks off the process.  The rest is taken care of for you.

## FAQs
**We need an extension that isn't included in this image? How do I get an image with the extension I need?**
To adjust the base images to suit your application's needs, we recommend creating a `Dockerfile` that extends this one.  Only commonly used packages within Realpage will be included in this base image.

**How can I request updates to this image**
Long term we plan to automate keeping the PHP version in this image up to date.  In the meantime, if you need updates that aren't here or would like to request an extension or other change to this base image please [create an issue](https://github.com/realpage/fpm-nginx/issues/new) or pull request.

## Issues
If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/realpage/fpm-nginx/issues).

## License
View [license information](http://php.net/license/) for the software contained in this image.
