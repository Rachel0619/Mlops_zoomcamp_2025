## VM in AWS EC2

### 1.1 Launch an EC2 instance

Just select whatever config that is most suitable for the project.

Note: you need to create a key pair (.pem), download it and put it in `~/.ssh/` folder

### 1.2 Set up `~/.ssh/config` file

```
Host mlops_zoomcamp
  HostName 34.222.4.143
  User ubuntu
  IdentityFile ~/.ssh/rachel_1.pem
  StrictHostKeyChecking no
```

Then you can get access to your VM by typing the bash command `ssh mlops_zoomcamp`.

### 1.3 Install Anaconda

Navigate to the anaconda official download website and copy the downloading url

```

```

### 1.4 Update existing packages

```
sudo apt update
```

### 1.5 Install Docker and Docker Compose

```
$ sudo apt install docker.io
$ mkdir soft
$ cd soft
$ wget https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-linux-x86_64
$ sudo mv docker-compose-linux-x86_64 /usr/local/bin/docker-compose
$ sudo chmod +x docker-compose

$ nano .bashrc
$ source ~/.bashrc
# add `export PATH="${HOME}/soft:${PATH}"` to the end
$ which docker-compose

# run docker without sudo
$ sudo groupadd docker
$ sudo usermod -aG docker $USER

# logout from the VM and then log back
$ docker run hello-world
```

