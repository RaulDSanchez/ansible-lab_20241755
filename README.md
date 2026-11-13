# Ansible Lab
# Raul Daniel Sanchez Sanchez - 2024-1755

## Objetivo de la práctica

Aprender los fundamentos de Ansible usando dos contenedores Docker como servidores administrados. La práctica incluye un inventario, la verificación de conexión con ping y un playbook que muestra información del host, crea directorios y archivos, usa un loop y ejecuta una tarea condicional.

## Iniciar los contenedores

```bash
docker compose up -d
docker ps
docker exec server1 bash -c "apt update && apt install -y python3"
docker exec server2 bash -c "apt update && apt install -y python3"
```

## Comprobar la conexión

```bash
ansible docker -i inventory.ini -m ping
```

## Ejecutar el playbook

```bash
ansible-playbook -i inventory.ini playbook.yml
```

## Captura de la ejecución exitosa

<img width="834" height="112" alt="Screenshot 2026-11-13 at 12 28 02 PM" src="https://github.com/user-attachments/assets/848f21e1-ea62-4b6b-b7b7-d4694bb924e5" />

