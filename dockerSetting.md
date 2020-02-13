# Ubuntu OS Docker Setting
### https://docs.docker.com/install/linux/docker-ce/ubuntu/

### Older versions of Docker were called docker, docker.io, or docker-engine. If these are installed, uninstall them:

sudo apt-get remove docker docker-engine docker.io containerd runc

### Install Docker Engine - Community

### Install using the repository

sudo apt-get update

### Install packages to allow apt to use a repository over HTTPS:

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

### Add Docker’s official GPG key:

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

### Use the following command to set up the stable repository.
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

### INSTALL DOCKER ENGINE - COMMUNITY

### Update the apt package index.
sudo apt-get update

### Install the latest version of Docker Engine - Community and containerd, or go to the next step to install a specific version:

sudo apt-get install docker-ce docker-ce-cli containerd.io

### To install a specific version of Docker Engine - Community, list the available versions in the repo, then select and install:

apt-cache madison docker-ce

### Add user to Docker User Group
sudo usermod -a -G docker $USER

### Verify that Docker Engine - Community is installed correctly by running the hello-world image
sudo docker run hello-world



