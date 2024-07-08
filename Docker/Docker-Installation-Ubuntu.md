```markdown
# Docker Installation on Ubuntu

This guide provides step-by-step instructions for installing Docker on Ubuntu.

## Prerequisites

- Ubuntu 20.04 or later
- Sudo privileges

## Installation Steps

1. Update the apt package index:
- sudo apt-get update

2. Install packages to allow apt to use a repository over HTTPS:
sudo apt-get install 
apt-transport-https 
ca-certificates 
curl 
gnupg 
lsb-release
3. Add Docker's official GPG key:
- curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
4. Set up the stable repository:
"deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu 
$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null