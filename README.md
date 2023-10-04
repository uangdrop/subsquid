
![photo_2023-09-28_16-56-07](https://github.com/uangdrop/subsquid/assets/128940865/ef19e477-81ee-447c-8b97-8739a1d9e2c8)

<h1 align="center"> Complete technical Subsquid Tasks <br> </h1>

<h1>  Persiapan: </h1>

Install NodeJS, Docker, git
```shell
sudo apt-get update && sudo apt install git -y && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y
```

```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
source ~/.bashrc
nvm install 18
nvm use 18
```
&nbsp;
Install Subsquid cli

```shell
npm install --global @subsquid/cli@latest
```  
&nbsp;
&nbsp;
&nbsp;

<h1> Run a single-proc squid : </h1>

Create Folder & init
```shell
mkdir proc
cd proc
sqd init single-proc -t https://github.com/subsquid-quests/single-chain-squid
cd single-proc
```

Download your key
* Open https://app.subsquid.io/quests
* Download "single-proc squid" Key
![Screenshot_12](https://github.com/uangdrop/subsquid/assets/128940865/21a5b1ae-abee-4950-918d-1abf786391a9)
&nbsp;
* Pindah Key File ke VPS di Folder ``/proc/single-proc/query-gateway/keys``


Start Docker
```shell
docker compose up -d
```
&nbsp;
build
```shell
npm ci
sqd build
```
&nbsp;
Run
```shell
sqd run .
```
&nbsp;
Setelah itu cek [website quest]([url](https://app.subsquid.io/quests)) milikmu akan berjalan sampai 100%
Setelah selesai kamu bisa Stop proc menggunakan CTRL+C
&nbsp;
Lalu Stop Docker 
```shell
docker compose down -v
```
&nbsp;
&nbsp;
&nbsp;

<h1> Run a double-proc squid : </h1>
Create Folder & init

```shell
cd ~/proc
sqd init double-proc -t https://github.com/subsquid-quests/double-chain-squid
cd double-proc
```

Download your key
* Open https://app.subsquid.io/quests
* Download "double-proc squid" Key
![Screenshot_13](https://github.com/uangdrop/subsquid/assets/128940865/1c815a35-4d93-4833-b131-57d78b663e6a)

&nbsp;
* Pindah Key File ke VPS di Folder ``/proc/double-proc/query-gateway/keys``


Start Docker
```shell
docker compose up -d
```
&nbsp;
build
```shell
npm ci
sqd build
```
&nbsp;
Run
```shell
sqd run .
```
&nbsp;
Setelah itu cek [website quest]([url](https://app.subsquid.io/quests)) milikmu akan berjalan sampai 100%
Setelah selesai kamu bisa Stop proc menggunakan CTRL+C
&nbsp;
Lalu Stop Docker 
```shell
docker compose down -v
```
&nbsp;
&nbsp;
&nbsp;

<h1> Run a triple-proc squid : </h1>
Create Folder & init

```shell
cd ~/proc
sqd init triple-proc -t https://github.com/subsquid-quests/triple-chain-squid
cd triple-proc
```

Download your key
* Open https://app.subsquid.io/quests
* Download "double-proc squid" Key
![Screenshot_14](https://github.com/uangdrop/subsquid/assets/128940865/629eaf92-937f-4a04-8ea2-c729b6dc9e36)


&nbsp;
* Pindah Key File ke VPS di Folder ``/proc/triple-proc/query-gateway/keys``


Start Docker
```shell
docker compose up -d
```
&nbsp;
build
```shell
npm ci
sqd build
```
&nbsp;
Run
```shell
sqd run .
```
&nbsp;
Setelah itu cek [website quest]([url](https://app.subsquid.io/quests)) milikmu akan berjalan sampai 100%
Setelah selesai kamu bisa Stop proc menggunakan CTRL+C
&nbsp;
Lalu Stop Docker 
```shell
docker compose down -v
```
&nbsp;
&nbsp;
&nbsp;

<h1> Run a quad-proc squid : </h1>
Create Folder & init

```shell
cd ~/proc
sqd init quad-proc -t https://github.com/subsquid-quests/quad-chain-squid
cd quad-proc
```

Download your key
* Open https://app.subsquid.io/quests
* Download "double-proc squid" Key

![Screenshot_15](https://github.com/uangdrop/subsquid/assets/128940865/476eee00-aa42-40c8-931a-ca2499e85622)

&nbsp;
* Pindah Key File ke VPS di Folder ``/proc/quad-proc/query-gateway/keys``


Start Docker
```shell
docker compose up -d
```
&nbsp;
build
```shell
npm ci
sqd build
```
&nbsp;
Run
```shell
sqd run .
```
&nbsp;
Setelah itu cek [website quest]([url](https://app.subsquid.io/quests)) milikmu akan berjalan sampai 100%
Setelah selesai kamu bisa Stop proc menggunakan CTRL+C
&nbsp;
Lalu Stop Docker 
```shell
docker compose down -v
```

