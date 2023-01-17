# Setup

- Run `./setup` to clone down the devenv submodule and checkout latest commit.
- Run `./init` if this is the first time using this repo (this creates the docker compose file).
- Edit the `./docker-compose.yml` file to set the root database password, and user and password to use for the application.
- For subsequent uses, run `./up` to bring up the containers.
- After starting the containers for the first time, run `./connect` to connect to the app container and go to the `/app` directory, then run `npm install`.
- Create a `.env` file in the `./code/` directory, using `.env.dist` as a template, and setting the correct values for your discord bot.
- Run `npm run update` to install the database tables.
- The first time you run the bot, you will want to use `npm run dev` as that will register the commands (also use that if you make any code changes and add/remove commands).
- Otherwise, you can use `npm start`
- If you want to run the bot in the background using a script manager, you can instead use the script `./src/go` which will install and run via `pm2`.

**Other helpful commands:**

`./connect <name>` will connect to the docker container specified, or the project's `-<type>` container by default.
`./stop` will bring down all the project containers.
`./destroy` will bring down and delete all the project containers and networks.
`npm run register -- purge` will delete all commands from the servers the bot is on (unless ENV=dev, then just your test server/guild)
`npm run register` will create all the commands again in all servers the bot is on (unless ENV=dev, then just your test server/guild)

# Server Requirements

- This has only been tested on Ubuntu 20.04
- `jq` module must be installed: `apt install jq`
