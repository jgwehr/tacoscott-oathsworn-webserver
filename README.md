# tacoscott-oathsworn-webserver
## What is this?
A simple example of using a reverse proxy to make this Oathsworn Web App available over your network

## Who is this for?
If you're familiar with Docker or already use a reverse proxy, this is a way of exposing the "flat" output of this (great) work as a web app. If you're not familiar, it's a simple example you can use for inspiration / education. 

## Why might somebody be interested?
This example allows you to access this app from a different computer. Maybe you have it running in your office and would like access to it from your tablet at the game table. If you're like me, you might have a server downstairs and what it available upstairs. If you have good knowledge of Docker and Caddy, exposing it publicly on your personal domain is within reach. Taking this approach also allows the server to exist behind SSL.

## How to Set it Up
Prequisite: you must have a functioning Docker environment. Setting this up is outside the scope of this project.
Prequisite: you must have already followed instructions from https://github.com/TheTacoScott/oathsworn-webapp

### Clone the repository
```
git clone https://github.com/jgwehr/tacoscott-oathsworn-webserver.git
```

### Edit `.env`
1. Rename the file `.env.template` to `.env`
2. Set `DIR_OATHSWORN_WEBAPP` to the directory where you set up oathsworn-webapp; the `index.html` file should exist at this directory.
3. Set `LOCALHOST` to the IP address of the machine where you set up TheTacoScott's Oathsworn Webserver
4. Set `PORT_OATHSWORN` to your preferred port number.

These two variables define how you will access the webapp: http://{LOCALHOST}:{PORT_OATHSWORN} or, for example, http://192.168.1.2:8096

### Start the server
Run `docker compose up -d`


