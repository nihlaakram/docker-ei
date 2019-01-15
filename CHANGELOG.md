# Changelog
All notable changes to this project 6.3.x per each release will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

## [Unreleased]

### Changed
- Improve the Docker resources to use the optimized WSO2 Enterprise Integrator product profile
packs to build the corresponding profile Docker images.
- Changed the folders to which configuration files with new changes to be copied are mounted.
Originally this was `wso2-server-volume` in general and for Kubernetes, this was
`kubernetes-volumes`. But with this release, there will not be any platform specific
folders for mounting configuration files. Instead we are introducing a single folder
for this purpose by the name, `wso2-config-volume`.
- Changed the folder to which any other non-configuration type artifacts to be copied are mounted.
Originally this was `wso2-server-volume`. But with this release, this is changed to `wso2-artifact-volume`.

### Compatibility with kubernetes-ei releases
- If you are to use images built using this release with the latest v6.3.0.1 Kubernetes release, please do change
your deployment mount paths appropriately to match above folder changes.

## v6.3.0.1 - 2018-07-15

### Added
- Per profile Docker resources of WSO2 Enterprise Integrator v6.3.x for Ubuntu
- Docker Compose resources for WSO2 Integration v6.3.x deployment patterns

[v6.3.0.2]: https://github.com/wso2/docker-ei/compare/v6.3.0.1...v6.3.0.2