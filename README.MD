# Setup

Run `git submodule update -init` to clone down the devenv repo.

Then run `./init` if this is the first time using this repo.

For subsequent uses, run `./up` to bring up the containers.

**Other helpful commands:**

`./connect <name>` will connect to the docker container specified, or the project's `web` container by default.
`./stop` will bring down all the project containers
`./destroy` will bring down and delete all the project containers and networks