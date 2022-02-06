# Docker Compose Project

Compose a FastAPI app in a container together with a database container. We're building an APP and connect it to a database. This makes three containers in total

* The database
* The database admin tool
* The APP, which connects via REST-API to any frontend and a driver to the database backend

## Using a GIT client on my remote VM

I have dialled in to my remote machine via an SSH connection and Visual Studio Code is set up as the development environment. In order for the remote VM to connect to GitHub, the configuration must be set as follows:
1. Check if the SSH agent is running:

 `eval $(ssh-agent -s)`

2. Check whether the SSH agent already knows the certificates of the remote VM:

 `ssh-add -l`

3. This was not the case for me. I registered my certificates with the agent as follows: 

 `ssh-add ~/.ssh/`

4. Now the certificate should be visible:

 `ssh-add -l`

5. Only with the correctly stored certificates can I now execute the clone command:

 `git clone git@github.com:Impulsleistung/docker_compose`

6. Finally, I can list all remotes

 `git remote -v`
