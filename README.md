# minecraft-modding-hub

Static GitHub Pages frontend for the Minecraft Modding community.

The website is published at `https://uyen11a1-star.github.io/minecraft-modding-hub/`. It uses the deployed FastAPI backend for posts and three sign-in methods: GitHub OAuth, Google OAuth, and email/password. The frontend contains **no OAuth client secret**.

## Deployment

GitHub Pages serves `index.html` directly. API configuration lives in `config.js`; change only `apiBaseUrl` if the backend URL changes. Keep `frontendUrl` equal to the full GitHub Pages URL, including the trailing slash.

The backend must define `FRONTEND_URL=https://uyen11a1-star.github.io/minecraft-modding-hub/`. GitHub and Google OAuth callback URLs must point to the backend, not GitHub Pages:

```text
https://mc-modding-backend.onrender.com/auth/github/callback
https://mc-modding-backend.onrender.com/auth/google/callback
```
