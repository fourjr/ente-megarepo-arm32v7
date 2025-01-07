To update:
```
docker-compose build --pull
docker-compose push
```

To install:
[Reference](https://github.com/ente-io/ente/blob/main/server/docs/docker.md) with a modified compose.yaml
1. Create directory
```mkdir ente && cd ente```
2. Download starter files
```
# compose.yaml
curl -L https://raw.githubusercontent.com/fourjr/ente-megarepo-arm32v7/master/install-compose.yaml -o compose.yaml

mkdir -p scripts/compose
cd scripts/compose

# scripts/compose/credentials.yaml
curl -LO https://raw.githubusercontent.com/ente-io/ente/main/server/scripts/compose/credentials.yaml

# scripts/compose/minio-provision.sh
curl -LO https://raw.githubusercontent.com/ente-io/ente/main/server/scripts/compose/minio-provision.sh

cd ../..

touch museum.yaml
```
3. Start
``` 
docker compose up
```