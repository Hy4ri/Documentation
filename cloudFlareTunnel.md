# Create cloudflare tunnels

## Stetup

1. Install cloudflared
2. login with `cloudflared tunnel login`

## Create the tunnel

- `cloudflared tunnel create tunnel-name`

## Configure the Ingress Rules

```YAML

tunnel: YOUR_TUNNEL_ID_HERE
credentials-file: ~/.cloudflared/YOUR_TUNNEL_ID_HERE.json

ingress:
  - hostname: app.yourdomain.com
    service: http://192.168.1.50:8080

  - service: http_status:404          # Required: Catch-all rule
```

## Route the Domain

`cloudflared tunnel route dns tunnel-name app.yourdomain.com`

## Run the Tunnel

`cloudflared tunnel --config ~/.cloudflared/config.yml run`
