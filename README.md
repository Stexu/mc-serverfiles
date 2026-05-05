```yaml
services:
  mc:
    image: 'itzg/minecraft-server:latest'
    tty: true
    stdin_open: true
    ports:
      - '25565:25565'
    environment:
      EULA: 'TRUE'
      TYPE: MODRINTH
      MODRINTH_MODPACK: 'https://github.com/Stexu/mc-serverfiles/raw/refs/heads/main/Create+%20Server%20edition%201.0.0.mrpack'
      MEMORY: 3072M
      MAX_PLAYERS: '32'
      MOTD: 'Create with frens :3'
      USE_MEOWICE_FLAGS: 'true'
      OPS: Stexu
      TZ: Europe/Berlin
    volumes:
      - './data:/data'
```
