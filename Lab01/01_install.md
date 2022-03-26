1. Actualizar centos (opcional)
    ```bash
    sudo dnf update -y
    ```

1. Agregar Docker-CE repositorio
    ```console
    sudo dnf config-manager --add-repo=https://download.docker.com/linux/centos/docker-ce.repo
    ```

1. Instalar última versión docker
    ```console
    sudo dnf install -y docker-ce --nobest
    ```

1. Actualizar última versión docker
    ```console
    sudo dnf update -y docker-ce --nobest
    ```

1. Iniciar docker cuando iniciar el SO
    ```console
    sudo systemctl start docker
    sudo systemctl enable docker
    ```
1. Verificar versión
    ```console
    docker --version
    ```

1. Verificar permisos
    ```console
    sudo docker run -p 8080:80 nginx
    CTRL + C
    ```
    
1. Fix permisos
    ```console
    sudo groupadd docker
    sudo usermod -a -G docker $USER
    sudo chmod 666 /var/run/docker.sock
    sudo service docker restart
    systemctl is-active docker
    docker run hello-world
    ```