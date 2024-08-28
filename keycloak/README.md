# Keycloak export

```
mkdir ./keycloak_export
sudo chown 1000:1000 ./keycloak_export # NOTE: to avoid permission problem when exporting realm and users
# NOTE: modify docker-compose.yml -> add volume on keycloak container -> ./keycloak_export:/opt/keycloak/data/export/
docker compose down && docker compose up -d
docker exec -it -e KC_DB=postgres keycloak /opt/keycloak/bin/kc.sh export --realm data_factory --users same_file --dir /opt/keycloak/data/export/
```

Documentation: https://www.keycloak.org/server/importExport