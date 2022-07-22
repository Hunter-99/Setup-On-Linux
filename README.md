# :wrench: Setup-On-Linux

### Git
```shell
sudo apt-get -y install git
# sudo tar -xf .ssh.tar.xz -C ${HOME}
git config --global user.name "Your UserName"
git config --global user.password "Your Password"
git config --global user.email "Your e-mail"
```
---

### Python 3.10
```shell
sudo apt install python-is-python3
sudo apt install -y python3.10-venv
alias python=python3
sudo pip install --upgrade pip
```
---

### Poetry
```shell
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
```

---

### Docker
```shell
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
sudo apt install -y docker-ce
sudo apt install -y docker-compose
sudo chmod 666 /var/run/docker.sock
sudo groupadd docker
sudo usermod -aG docker $USER
```

---

### Slack
```shell
sudo snap install slack
```

---

### PyCharm
```shell
sudo snap install pycharm-professional --classic
```

---
### Telegram Desktop
```shell
sudo snap install telegram-desktop
```

---
### VSCode
```shell
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt install code
```

---
### Postman
```shell
sudo snap install postman
```

---
### VLC
```shell
sudo snap install vlc
```

---

### AWS CLI
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
aws configure
```

---