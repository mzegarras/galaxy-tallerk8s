## Evaluación
1. Generar la imagen del proyecto 03_node con el nombre apinode:1.0.0
1. Ports: 3000:3000
1. Environment
    * PORT: 3000
    * URL_DB: 'mongodb://localhost:27017/interfaces'
    * URL_DB_USER:
    * URL_DB_PWD:
1. Usar ./03_node/Dockerfile
1. Publicar las imágenes en tu repositorio mzegarra/apinode:1.0.0
1. Puede probar las apis request.http

## Evaluación

1. Create el servicio de mongo con el nombre: db-apellido
    * Por ejemplo: db-zegarra, db-perez
    * Este servicio sólo debe estar disponible dentro del cluster
1. Create el servicio de mongo con el nombre: backend-apellido
    * Por ejemplo: backend-zegarra, backend-perez
    * Este servicio sólo debe estar disponible desde cualquier parte del mundo