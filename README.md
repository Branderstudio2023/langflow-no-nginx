# Langflow (no Nginx) on Fly.io

This setup uses the official Langflow image without any external Nginx or Basic Auth.

## Login

From Langflow v1.3+, it includes its own login system.

Set environment variables before deploying (Fly.io example):

```
fly secrets set LANGFLOW_SUPERUSER_EMAIL=admin@example.com LANGFLOW_SUPERUSER_PASSWORD=yourpassword
```

## Port

- Internal: 7860
- Fly.io will map to public HTTPS port

## Deployment

1. Push this folder to GitHub
2. Launch from GitHub on Fly.io
3. Access your app via the generated `.fly.dev` domain