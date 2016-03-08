# Magnon server manager
Simple script that allows for easy installation of our servers. It was specifically made to be run on Ubuntu, so don't expect it to work with other distros. While the script was made for our (Magnon's) servers, if you feel like it'll be of any use for you, feel free to fork and use it for your own purposes!

## Contribution
All contributions to this project are appreciated! If you find a bug, please report it in the bug manager and provide relevant information. If you want to contribute with code, feel free to send in a pull request and keep in mind that I'm very new to collaboration on GitHub.

## Usage

Before anything, give the script permission to run:
```
$ chmod +x manage
```
With that done, continue.

***IF YOU'RE HAVING PROBLEMS*** the cause is most likely that you try to execute this without having proper permission to docker. To fix this either, [add yourself to the docker group](https://docs.docker.com/engine/installation/linux/ubuntulinux/#create-a-docker-group) or run the commands with `sudo`.

### help / h
Shows a help message.

### proxy / p
Starts a proxy server. Runs with Let's Encrypt certificate manager if `PRODUCTION` variable is set to `true`.

### run / r
Creates and starts a new container behind the proxy. Syntax:
```
$ ./manage run <docker repository name> <URL(s) to link> [docker arguments]
```

### wipe / w
Wipes all docker containers. Doesn't wipe proxy container unless a `-d` flag was provided.

### command / c
Executes a command on a container. Syntax:
```
$ ./manage command <container name> <command with args>
```

### install / i
Installs the latest version of docker. Also installs docker-compose if `-c` flag was provided.

## License
MIT - You can read about it [here](https://en.wikipedia.org/wiki/MIT_License).
