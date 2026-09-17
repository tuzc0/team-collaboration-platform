# Team Collaboration Platform

Plataforma de comunicación y gestión ligera de proyectos con aplicaciones independientes para escritorio y móvil.

## Clientes

- **Desktop:** Java, JavaFX, Maven y SQLite.
- **Mobile:** Flutter, Dart y SQLite mediante Drift.

## Backend

- **Auth Service:** Rust, Axum, Tokio, Tower y SQLx.
- **Core Service:** Elixir, Phoenix y Erlang/OTP.

## Persistencia

- **PostgreSQL:** usuarios, autenticación, grupos, roles, proyectos y demás información estructurada.
- **Cassandra:** mensajes, historial, eventos y actividad.
- **Redis:** caché, sesiones, presencia, rate limiting e información temporal.
- **MinIO:** imágenes, documentos, audios, videos y archivos adjuntos.

## Infraestructura

El entorno local se ejecuta sobre:

- Ubuntu Server 24.04 LTS;
- Vagrant y VirtualBox;
- Docker Engine;
- Docker Compose.

La máquina virtual utiliza:

- 6 GB de RAM;
- 4 CPU virtuales;
- disco principal de 80 GB;
- IP privada `192.168.33.30`.

### Servicios de desarrollo

| Servicio | Inicio | Puerto | Propósito |
|---|---|---:|---|
| PostgreSQL | Predeterminado | 5432 | Persistencia relacional |
| Redis | Predeterminado | 6379 | Caché e información temporal |
| Mailpit | Predeterminado | 1025 / 8025 | Pruebas locales de correo |
| Cassandra | Perfil `messaging` | 9042 | Mensajería e historial |
| MinIO | Perfil `storage` | 9000 / 9001 | Almacenamiento de objetos |

## Inicio rápido

Requisitos del equipo anfitrión:

- Vagrant 2.4.9 o una versión compatible;
- VirtualBox 7.2 o una versión compatible;
- virtualización de hardware habilitada;
- al menos 16 GB de RAM;
- conexión a Internet durante el primer aprovisionamiento.

Crear la configuración local en PowerShell:

```powershell
Copy-Item .\infrastructure\.env.example .\infrastructure\.env
```

El archivo `infrastructure/.env` no debe subirse al repositorio. Antes de iniciar la máquina, deberán sustituirse sus valores de ejemplo por credenciales locales.

Crear y aprovisionar la VM:

```powershell
vagrant validate
vagrant up --provider=virtualbox
vagrant ssh
```

PostgreSQL, Redis y Mailpit se inician durante el aprovisionamiento. Para revisar su estado dentro de la VM:

```bash
cd /vagrant/infrastructure
docker compose ps
```

Iniciar Cassandra:

```bash
docker compose --profile messaging up -d
```

Iniciar MinIO:

```bash
docker compose --profile storage up -d
```

Iniciar todos los servicios:

```bash
docker compose --profile messaging --profile storage up -d
```

Interfaces disponibles desde el equipo anfitrión:

- Mailpit: `http://192.168.33.30:8025`
- MinIO Console: `http://192.168.33.30:9001`

Detener los contenedores sin eliminar los datos:

```bash
docker compose --profile messaging --profile storage down
```

> No utilice `docker compose down -v` salvo que se desee eliminar permanentemente los datos locales.

## Seguridad

- Los archivos `.env` reales no deben versionarse.
- `.env.example` únicamente debe contener valores de referencia.
- No deben incorporarse contraseñas, tokens, claves privadas ni certificados al repositorio.
- Los datos persistentes son administrados mediante volúmenes nombrados de Docker dentro de la VM.

## Documentación

- [Estándar de desarrollo](docs/STANDARD_DEVELOPMENT.md)
- [Definition of Done](docs/DEFINITION_OF_DONE.md)
- [Guía de contribución](CONTRIBUTING.md)

## Estado

🚧 En fase inicial de diseño y desarrollo.