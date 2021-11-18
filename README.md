## How to run on AWS?

- Go to EC2
- Launch a new instance
- Choose t2.medium or higher, other settings could be by default
- Install docker inside (the shell script for Ubuntu below)
- Enjoy


**Example for Ubuntu**
```shell
#!/bin/bash
apt-get update
apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
apt-get update
apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose
```

## Default credentials

- login: **admin**
- password: **admin**

More info by link [here](https://docs.sonarqube.org/latest/setup/get-started-2-minutes/)
