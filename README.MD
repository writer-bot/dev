# Setup

- Run `./setup` to clone down the devenv submodule and checkout latest commit.
- Run `./init` if this is the first time using this repo (this creates the docker compose file).
- For subsequent uses, run `./up` to bring up the containers.

**Other helpful commands:**

`./connect <name>` will connect to the docker container specified, or the project's `-<type>` container by default.
`./stop` will bring down all the project containers.
`./destroy` will bring down and delete all the project containers and networks.
