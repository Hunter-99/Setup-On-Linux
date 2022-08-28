# :cookie: Setup-On-Linux
Setup-On-Linux - repository is designed to install all the necessary programs to work on Linux. 
> :warning: Tested only for `Zorin OS 16.1`

## Preparation
```shell
sudo apt update 
sudo apt upgrade -y
```

## Git
```shell
sudo apt-get -y install git
git config --global user.name "Your UserName"
git config --global user.password "Your Password"
git config --global user.email "Your e-mail"
```

## Python 3.8
```shell
sudo apt install python-is-python3
alias python=python3
```
### Python venv
```shell
sudo apt install -y python3.8-venv
```
### Pip
```shell
sudo apt intall -y pip
sudo pip install --upgrade pip
```
### Poetry
```shell
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
```

## Docker
```shell
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

## Docker-compose 1.29.2
```shell
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## Use docker & docker-compose without `sudo`
```shell
sudo chmod 666 /var/run/docker.sock
sudo groupadd docker
sudo usermod -aG docker $USER
```

## ZSH
```shell
sudo apt-get install -y git-core zsh fonts-powerline
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
chsh -s $(which zsh)
```

### Install zsh-autosuggestions
- Install the zsh-autosuggestions:
    ```shell
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    ```
- Add plugin `~/.zshrc`:
    ```shell
    vi ~/.zshrc
    ...
    plugins=(git)
    plugins=(zsh-autosuggestions) # Add this line. under the "plugins"
    source $ZSH/oh-my-zsh.sh
    ```
## AWS CLI
```shell
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
aws configure
```

## PgAdmin4 (desktop)
```shell
sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
sudo apt install pgadmin4-desktop
```

## Terraform
```shell
wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list

sudo apt update && sudo apt install terraform
```

## Apps

-  Slack
    ```shell
    sudo snap install slack
    ```

- PyCharm
    ```shell
    sudo snap install pycharm-professional --classic
    ```

- Telegram Desktop
    ```shell
    sudo snap install telegram-desktop
    ```

- VSCode
    ```shell
    sudo apt install software-properties-common apt-transport-https wget
    wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
    sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
    sudo apt install code
    ```

- Postman
    ```shell
    sudo snap install postman
    ```

- VLC
    ```shell
    sudo snap install vlc
    ```

- Spotify
    ```shell
    sudo snap install spotify
    ```

- Notion
    ```shell
    sudo snap install notion-snap
    ```

- Zoom
    ```shell
     sudo snap install zoom-client
     ```
