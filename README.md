# DarkShard_setup
Launch scripts and docker configurations for the darkshard server and services

# Initialisation
`yarn setup`

This will clone all dependency repositories. 
# NOTE THE PROJECT DIRECTORIES WILL BE DELETED IF THEY ALREADY EXIST - MAKE SURE TO COMMIT ANY CHANGES BEFORE RUNNING THIS A SECOND TIME
## subscripts
- `yarn clone-darkshard`
    This can be used to clone only the darkshard html/front end server repository
- `yarn clone-gateway`
    This can be used to clone only the gateway api server repository

# Install deps
`yarn install-all`

This will run `yarn install` in each repository directory using the following subscripts
## subscripts
- `yarn install-darkshard`
    This will call `yarn install` in the darkshard html/front end server repository
- `yarn install-gateway`
    This will call `yarn install` in the gateway api server repository

# Launching
`yarn launch`

This will call `yarn build` in each repository and then launch the docker containers with the following scripts
## subscripts
- `yarn build-all`
    This will call each repositories build script
- `yarn build-darkshard`
    This will call `yarn build` in the DarkShard htlm/front end server repository

These scripts will run in parralel on linux based systems (including macOS) however they will be sequencial on windows.

# New environment setup
## pre-requisites
- node version 8.11.3 or higher
- npm version 5.6 or higher
- docker

## setup steps
Clone the setup repo (this one) with `git clone git@github.com:DarkShardDesign/DarkShard_setup.git`

Once the repo is cloned enter the directory `cd darkshard_setup` and run `yarn setup` followed by `yarn install-all`

This will now have all repositories clone inside darkshard_setup folder with their dependencies installed.

## running the projects
To run the project and all dependant backend projects use `yarn launch` which will build all repositories and launch the docker containers.
