# Magnon server manager
This is a very simple scripts that just asks you a few questions to configure a server correctly. Currently, all it does is asks if you want to istall docker and then lets you input a mail to use as your let's encrypt email. If you choose to install docker, it will also install python-pip and then docker-compose.

## Usage
```
$ chmod +x manage
$ . ./manage
```
The extra dot is needed if you want to set the email. If not, you can leave it out.

## License
MIT - You can read about it [here](https://en.wikipedia.org/wiki/MIT_License).
