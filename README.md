# TP1-PWA-LOPEZJOVEManuel

## Puesta en marcha del ambiente PRODUCCION:

- Ejecutar el docker compose:

```
  docker-compose up -d
```

- Igresar al contenedor e intalar composer:

```
docker-compose exec app bash -c "composer install"
```

- Asignar los permisos a las carpetas del repo:

```
sudo chmod 777 src/basic/runtime/ src/basic/web/assets/ &&\
sudo chmod 775 src/basic/models src/basic/controllers -R src/basic/views
```

## Puesta en marcha del ambiente DESARROLLO:

- Ejecutar el docker compose:

```
  docker-compose -f docker-compose.yml -f docker-compose-dev-yml up -d
```

- Igresar al contenedor e intalar composer:

```
docker-compose exec app bash -c "composer install"
```

- Asignar los permisos a las carpetas del repo:

```
sudo chmod 777 src/basic/runtime/ src/basic/web/assets/ \
src/basic/models src/basic/controllers -R src/basic/views
```
