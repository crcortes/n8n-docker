services:
  n8n:
    image: n8nio/n8n:latest
    restart: always
    ports:
      - "5678:5678"
    environment:
      - N8N_BASIC_AUTH_ACTIVE=true
      - N8N_BASIC_AUTH_USER=admin
      - N8N_BASIC_AUTH_PASSWORD=n8npassword
      - GENERIC_TIMEZONE=America/Argentina/Buenos_Aires
    volumes:
      - n8n_data:/home/node/.n8n

volumes:
  n8n_data:
