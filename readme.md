# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## First setup
To run the anythink application in your local environment, please follow these steps:
1. Clone the anythink Git Repository. 
2. Install Docker on your system with docker-compose. The steps for installing docker are [here](https://docs.docker.com/desktop/#download-and-install). 
> In Arch Linux, Docker Desktop is incompatible with [docker-compose](https://wiki.archlinux.org/title/docker#Docker_Desktop) so just install the [docker-compose package](https://archlinux.org/packages/?name=docker-compose) available in the community repository.
3.  Open your terminal and change directory to the Anythink git repository.
4.  Run the `docker-compose up` command in the root of the directory to start the frontend and backend of the application.
5. To check if everything is fine, go to [http://localhost:3000/api/ping](http://localhost:3000/api/ping). 
> Incase, the `docker-compose up` command fails,  you can take a look at the logs to find the problem.  Some common problems:
> 1.  The application uses port 3000 for backend and port 3001 for frontend. Incase, these ports are exhausted, the application might fail.
> 2. There might be a conflict with another instance of mongodb running on the `tcp4 0.0.0.0:27017` address port on your local environment. On windows, you can go to task manager to disable the mongodb service and reboot. On linux, use systemd to disable the service like so `systemctl disable --now mongodb.service` and reboot(or kill the mongodb process that is using the port). 
