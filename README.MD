# Setup

- Run `./setup` to clone down the devenv submodule and checkout latest commit.
- Run `./init` if this is the first time using this repo (this creates the docker compose file).
- For subsequent uses, run `./up` to bring up the containers.
- After starting the containers for the first time, run `./connect` to connect to the app container and go to the `/app` directory, then run `npm install`.
- Create a `.env` file in the `./code/` directory, using `.env.dist` as a tenplate, and setting the correct values for your discord bot
- Run `npm run update` to install the database tables.
- After that, you can use either `npm start` or `npm run dev` to start the bot. `npm run dev` will remove all commands registered with Discord and re-register them.

**Other helpful commands:**

`./connect <name>` will connect to the docker container specified, or the project's `-<type>` container by default.
`./stop` will bring down all the project containers.
`./destroy` will bring down and delete all the project containers and networks.

# Server Requirements

- This has only been tested on Ubuntu 20.04
- `jq` module must be installed: `apt install jq`
- If the scripts such as `./setup`, `./init` etc... give permission denied, you will need to grant them permission to execute, e.g. `chmod +x setup`