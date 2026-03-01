docker pull wcjiang/linux-command

docker run --name linux-command --rm -d -p 9665:3000 wcjiang/linux-command:latest

# Or

docker run --name linux-command -itd -p 9665:3000 wcjiang/linux-command:latest

http://localhost:9665/

cd deploy/docker
docker compose up -d