# ciberseguridad_lab13

## Install Docker

Before running Juice Shop, ensure Docker is installed:

Windows/macOS: Install Docker Desktop from the official site, run the installer, and verify with:
```bash
docker --version
```
Linux (Debian/Ubuntu/Kali):
```Bash
sudo apt update && sudo apt upgrade
sudo apt install docker.io docker-compose
sudo systemctl enable docker
sudo systemctl start docker
docker --version
```
## Run Juice Shop in Docker

Once Docker is ready, pull and run the Juice Shop container:

```Bash
docker pull bkimminich/juice-shop
docker run -d -p 3000:3000 --name juice-shop bkimminich/juice-shop

-d runs in detached mode.

-p 3000:3000 maps container port 3000 to your host.
```
--name juice-shop names the container for easy management.

## Access it in your browser:

 - http://localhost:3000

(If using Docker Machine on macOS/Windows, use http://192.168.99.100:3000 instead.)

## Manage the Container

Check if running:
```Bash
docker ps
```
 - Stop:

```Bash
docker stop juice-shop
```
Restart:

```Bash
docker start juice-shop
```


Always pull the latest imag
