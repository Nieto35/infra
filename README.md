# infra

## Comenzar

### Archivo hosts

```
127.0.0.1 app.project.local 
```

### Docker

Docker para estandarizar entornos de trabajo.

[Instalar Docker](https://docs.docker.com/desktop/)

### Ansible

Ansible para estandarizar procesos. Esta herramienta está disponible como imagen de Docker:

```shell
#Construir imagen para ejecutar Ansible
cd ansible/docker; docker build -t project/ansible .; cd ../..

##### Clonar repositorios

```shell
./ansible-playbook.sh dev/clone-repositories.yml

##### Copiar archivos .env

```shell
./ansible-playbook.sh dev/copy-env-files.yml

##### Arrancar y parar proyectos

```shell
./ansible-playbook.sh dev/start.yml
./ansible-playbook.sh dev/stop.yml
