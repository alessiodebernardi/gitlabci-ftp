# Gitlab CI/CD - Deploy pipeline with FTP
> Author: Alessio Debernardi Venon

This pipeline use a minimal Docker Alpine image (https://hub.docker.com/_/alpine) and the LFTP library (https://lftp.yar.ru/) to mirror repository files into a remote host, using FTP protocol.  
This script is a starting point: configure it with your own paths (repository-dir/, remote-dir/) and excluded files (--exclude-glob ... ).

# Notes
- You need a Gitlab Runner associated with your repository (https://docs.gitlab.com/runner/)
- The Gitlab Runner have to be configured with DOCKER executor (https://docs.gitlab.com/runner/executors/docker.html)
- You have to configure proper CI Variables (FTP_HOST, FTP_USERNAME, FTP_PASSWORD) in your repository settings