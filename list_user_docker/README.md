# list_user_docker

This script lists all the current running docker containers (same as `docker ps -a`), adding additional useful information, such as the user who created the container.

## Getting started

To run this command, simply:

```bash
list_user_docker
```

```bash
mrt@atenea /home/mrt $ list_user_docker
Results might not be accurate, take them with a piece of salt (Marcos).
Container name: priceless_heisenberg with Container ID: c71bf9e645be belongs to User: mrt
Container name: stupefied_nash with Container ID: 596259de3dda belongs to User: lyc
Container name: compassionate_williamson with Container ID: eaac5cc33790 belongs to User: root
```

This information is similar to the one provided by `docker ps -a`, but with additional information and color coded (here the text doesn't appear colored due to GitHub markdown renderer).

```bash
mrt@atenea /home/mrt $ docker ps -a
CONTAINER ID   IMAGE           COMMAND                  CREATED          STATUS                    PORTS      NAMES
eaac5cc33790   nginx           "/docker-entrypoint.…"   6 seconds ago    Up 5 seconds              80/tcp     compassionate_williamson
c71bf9e645be   robomaster:v4   "tini -g -- start.sh…"   17 seconds ago   Up 16 seconds (healthy)   8888/tcp   priceless_heisenberg
596259de3dda   froster-env     "/bin/bash"              2 hours ago      Up 2 hours                           stupefied_nash
```

>[!Note]
>This script requires you to be able to execute `docker` commands. The easiest way is by adding your user to the `docker` group:
>
>```bash
>sudo usermod -aG docker user_name
>```
