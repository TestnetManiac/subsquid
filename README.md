<p align=center><img src="https://pbs.twimg.com/media/F7DAaWNaAAAZkIe?format=jpg&name=small"> </p>


<h1 align=center> Subsquid Tech Section Complete Tasks <br></h1>

## Preparation
1. Setting VPS or you can use <a href="https://github.com/codespaces">Codespaces from Github</a>
2. Install and Configure NodeJS, Docker, git
```
sudo apt-get update && sudo apt install git -y && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y
```
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
source ~/.bashrc
nvm install 18
nvm use 18
```
3. Install Subsquid CLI
```
npm install --global @subsquid/cli@latest
```

## Main Tasks
### Run a Single-proc Squid
Create Folder and Initialize Configuration Project
```
mkdir proc
cd proc
sqd init single-proc -t https://github.com/subsquid-quests/single-chain-squid
cd single-proc
```
Download Key
* Navigate to https://app.subsquid.io/quests
* Download "single-proc squid" (check this picture)
  ![image](https://github.com/TestnetManiac/subsquid/assets/117708040/6a74da5c-3650-42ed-b58a-f936a5e1a659)
* Move this key file to this folder ``/proc/single-proc/query-gateway/keys``
Start Docker
```
docker compose up -d
```
Buid Docker
```
npm ci
sqd build
sqd migration:apply
```
Running Docker
```
sqd run .
```
Wait for several minutes, if from quest website showing claim or was 100%, you can stop process using ``CTRL+C`` then copy this command
```
docker compose down -v
```
### Run a Double-proc Squid
Create Folder and Initialize Configuration Project
```
cd ~/proc
sqd init double-proc -t https://github.com/subsquid-quests/double-chain-squid
cd double-proc
```
Download Key
* Navigate to https://app.subsquid.io/quests
* Download "double-proc squid" (check this picture)
  ![image](https://github.com/TestnetManiac/subsquid/assets/117708040/66dae6f0-1bdb-4671-aa07-34489c011042)
* Move this key file to this folder ``/proc/double-proc/query-gateway/keys``
Start Docker
```
docker compose up -d
```
Buid Docker
```
npm ci
sqd build
sqd migration:apply
```
Running Docker
```
sqd run .
```
Wait for several minutes, if from quest website showing claim or was 100%, you can stop process using ``CTRL+C`` then copy this command
```
docker compose down -v
```
### Run a Triple-proc Squid
Create Folder and Initialize Configuration Project
```
cd ~/proc
sqd init triple-proc -t https://github.com/subsquid-quests/triple-chain-squid
cd triple-proc
```
Download Key
* Navigate to https://app.subsquid.io/quests
* Download "triple-proc squid" (check this picture)
  ![image](https://github.com/TestnetManiac/subsquid/assets/117708040/23fc6993-8cfe-45a1-a363-67366968dd6c)
* Move this key file to this folder ``/proc/triple-proc/query-gateway/keys``
Start Docker
```
docker compose up -d
```
Buid Docker
```
npm ci
sqd build
sqd migration:apply
```
Running Docker
```
sqd run .
```
Wait for several minutes, if from quest website showing claim or was 100%, you can stop process using ``CTRL+C`` then copy this command
```
docker compose down -v
```
### Run a Quad-proc Squid
Create Folder and Initialize Configuration Project
```
cd ~/proc
sqd init quad-proc -t https://github.com/subsquid-quests/quad-chain-squid
cd quad-proc
```
Download Key
* Navigate to https://app.subsquid.io/quests
* Download "quad-proc squid" (check this picture)
  ![image](https://github.com/TestnetManiac/subsquid/assets/117708040/8640aba0-094d-44c6-b685-4c91ae6d21d0)
* Move this key file to this folder ``/proc/quad-proc/query-gateway/keys``
Start Docker
```
docker compose up -d
```
Buid Docker
```
npm ci
sqd build
sqd migration:apply
```
Running Docker
```
sqd run .
```
Wait for several minutes, if from quest website showing claim or was 100%, you can stop process using ``CTRL+C`` then copy this command
```
docker compose down -v
```
