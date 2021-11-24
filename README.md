# Parcial2-PWA-LOPEZJOVEManuel

Parcial N° dos de Programación Web Avanzada.
Dejo los pasos para la puesta en marcha del ambiente.

## Puesta en marcha del ambiente PRODUCCION:

- Asegurarse que en el docker-compose.yml la variable de entrno producción se encuentre en 1:

```
  environment:
     PRODUCCION: 1
```

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

- Asegurarse que en el docker-compose.yml la variable de entrno producción se encuentre en 0:

```
  environment:
     PRODUCCION: 0
```

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
sudo chmod 777 src/basic/runtime/ src/basic/web/assets/ \
src/basic/models src/basic/controllers -R src/basic/views
```
