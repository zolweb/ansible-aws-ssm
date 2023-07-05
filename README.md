# Docker Ansible AWS SSM

This repository hold the code for a Dockerfile extending ansible docker image `willhallonline/ansible` to add AWS SSM module

This allows to run Ansible playbook on AWS EC2 instance through an SSM session instead of SSH

See [CHANGELOG](CHANGELOG.md) for all available versions.

## Dockerhub

This project is built on dockerhub, on zolweb account. Images are free to use and come AS IS. ZOL is not responsible for any mis-usage or any problem it may cause.

Automatic building is enabled, any tag push or main push trigger a build as following :

Source	Type	Tag docker
main	branch	latest
/^[0-9.]+/	tag	{sourceref}

Examples :

Pushing the tag 1.10 gives the image zolweb/docker-ansible-aws-ssm:1.10
Pushing to main updates the image zolweb/php-fpm:latest
You should not use latest tag, as the push order on this repository is done following our own needs, not original image versions. Use tag instead.