# [WIP]Guidelines for release managment

## Components
Each component will do its own integration testing. The individual developers have to make sure that all required tests are passed.
Preferably the integration testing is done using travis CI.

After successfully testing a potential release, a project maintainer can create a github release with tagging rules described in the Tagging subsection.
Based on this release an automated build pipeline is triggered to build the docker images. It should be part of the integration testing that the Dockerfile produces a working image. Currently Dockerhub is the main build and distribution platform. 

## Tagging rules
Release tagging should follow semantic versioning rules. For the stable releases the schema would be vX.Y.Z. (e.g. v1.0.3). All other releases should be marked with a trailing tag indicating the pre-release type, like dev, demo, beta, etc... and an additional build number (e.g. v1.0.3-dev1). The build version can optionally be a date or a commit hash, although introducing a natural ordering here is strongly prefered. The tags will be directly used to tag the container image. [WIP/Not yed implemeted] for easier handling additional tags will be introduced for the different version elements (major, minor), e.g. v1 will be the current stable version of any release with a major release version of 1.