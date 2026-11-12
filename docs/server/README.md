# RomM no servidor (Debian 13, Docker)

Baseado nas notas do servidor: 8 GB de RAM, apps em `/opt/stacks/<app>`, ROMs no HD (`/mnt/hd`).

1. `mkdir -p /opt/stacks/romm /mnt/hd/Roms` e copiar `compose.yaml` e `.env.example` (como `.env`).
2. `docker compose up -d` e abrir `http://192.168.3.50:8080` para criar o admin.
3. Porta 8080 não conflita com os containers atuais. Para `romm.casa`, acrescentar uma entrada no Caddy (só LAN) e a reescrita no AdGuard.
4. Pareie o app: RomM > Settings > Client API Tokens.

O app já vem com `http://192.168.3.50:8080` como servidor padrão (`config.js`). Não expor o RomM no túnel da Cloudflare.
