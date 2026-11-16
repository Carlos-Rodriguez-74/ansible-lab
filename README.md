
# Práctica de Ansible con Docker

## Objetivo
Crear y configurar dos servidores Ubuntu mediante contenedores Docker, utilizando Ansible para ejecutar tareas de forma automatizada.

## Estructura del proyecto
- docker-compose.yml: configuración de los contenedores.
- inventory.ini: inventario de servidores para Ansible.
- playbook.yml: tareas que se ejecutan en los servidores.
- README.md: documentación del proyecto.

## Iniciar los contenedores
Ejecutar el siguiente comando desde la carpeta del proyecto:

```bash
docker compose up -d
```

Para verificar que los contenedores estén funcionando:

```bash
docker ps
```

## Ejecutar el playbook
Ejecutar el siguiente comando:

```bash
ansible-playbook -i inventory.ini playbook.yml
```

## Tareas realizadas
El playbook realiza las siguientes operaciones:

1. Muestra el nombre del servidor.
2. Muestra el sistema operativo.
3. Crea el directorio `/tmp/ansible-demo`.
4. Crea el archivo `info.txt`.
5. Escribe el nombre del servidor y el sistema operativo en el archivo.
6. Crea los directorios `logs`, `backup` y `config` mediante un ciclo.
7. Muestra un mensaje si el sistema operativo es Ubuntu.

## Evidencia de ejecución
El playbook se ejecutó correctamente en ambos servidores:

- server1: 8 tareas correctas, 5 cambios y 0 errores.
- server2: 8 tareas correctas, 5 cambios y 0 errores.

Se adjunta una captura de pantalla del resultado de ejecución.
