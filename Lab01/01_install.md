1. Actualizar centos (opcional)
    ```bash
    sudo sed -i -e "s|mirrorlist=|#mirrorlist=|g" /etc/yum.repos.d/CentOS-*
    sudo sed -i -e "s|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g" /etc/yum.repos.d/CentOS-*
    dnf clean all
    sudo dnf swap centos-linux-repos centos-stream-repos
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


1. docker-compose
https://docs.docker.com/compose/cli-command/

    ```console
sudo curl -L "https://github.com/docker/compose/releases/download/v2.3.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version

    ```