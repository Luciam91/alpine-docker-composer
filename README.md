# Composer 1.1 Alpine Dockerfile

Composer provides dependency management in PHP, this Dockerfile has been inspired by the work done by Rob Loach at https://github.com/RobLoach/docker-composer but the images haven't been refreshed on Docker Hub in a long time, which resulted in PHP7.1 being unable to use these files.

## Installation / Usage

1. Pull the image

`docker pull luciam91/alpine-docker-composer`

2. Run any command available in the Composer [Documentation](https://getcomposer.org/doc/) with the following:

`docker run -it --rm -v $(pwd):/app -u $UID luciam91/alpine-docker-composer init`

If you are using SSH to install your packages either mount your entire home directory, or at least the `.ssh` directory to `/root`

`docker run -ti --rm -v $(pwd):/app -v $HOME/.ssh:/root/.ssh -u $UID luciam91/alpine-docker-composer install`
