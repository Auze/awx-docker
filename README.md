# awx-docker

***AWX in docker container with nginx reverse proxy***

This is a modification of the docker-compose file generated by the AWX Official installer with nginx as a reverse proxy included.

## Installation : 

- Clone this repository in `/srv`
- Add necessary SSL certificates & key in `ssl` folder
*note*: provided SSL certificate is Self-signed

- Create the `SECRET_KEY` file in `secret` folder
- Copy service file in /etc/systemd/system/

```
cd /srv/awx-docker/
mv awx-docker.service /etc/systemd/system/
```

- Reload the daemon
```
systemctl daemon-reload
```
## Configuration

#### Configuration files

- credentials.py
- environment.sh
- docker-compose.yml (of course)
- nginx.conf (for SSL certificates)

These files are generally generated by AWX Official installer, for this repackaging, I've extract the file, so modify them **carefully** with a text editor.


## Todo

- Make an installation script
