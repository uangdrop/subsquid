
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

<h1> Run a Snapshot squid : </h1>

Create Folder & init
```shell
mkdir proc
cd proc
sqd init snapshot -t https://github.com/subsquid-quests/snapshot-squid
cd snapshot
```

Download your key
* Open https://app.subsquid.io/quests
* Download "Snapshot squid" Key
![Screenshot_9](https://github.com/uangdrop/subsquid/assets/128940865/78cb1632-7d41-4f41-89b4-6b9973346f65)

&nbsp;
* Pindah Key File ke VPS di Folder ``/proc/snapshot/query-gateway/keys``


Start Docker
```shell
docker compose up -d
```
&nbsp;
build
```shell
npm ci
```
```shell
sqd build
```
```shell
sqd migration:apply
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
