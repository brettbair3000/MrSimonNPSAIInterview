# Mr. Simon Feedback Tool — Proxy Server

A lightweight Node.js server that securely proxies requests to the Anthropic API,
so your API key is never exposed to users.

## Deploy to Railway (recommended — free tier available)

1. Go to https://railway.app and sign up with GitHub
2. Click **New Project** → **Deploy from GitHub repo**
3. Push this folder to a GitHub repo first, then connect it
   — OR — use **Railway CLI**:
   ```
   npm install -g @railway/cli
   railway login
   railway init
   railway up
   ```
4. In Railway dashboard → your project → **Variables** tab, add:
   ```
   ANTHROPIC_API_KEY=sk-ant-your-key-here
   ```
5. Railway auto-detects Node.js and runs `npm start`
6. Copy your Railway URL (e.g. https://mrsimon-proxy.up.railway.app)
7. Share that URL — users just open it, no key needed!

## Deploy to Render (also free)

1. Go to https://render.com and sign up
2. Click **New** → **Web Service** → connect your GitHub repo
3. Set:
   - Build command: `npm install`
   - Start command: `npm start`
4. Under **Environment Variables**, add:
   ```
   ANTHROPIC_API_KEY=sk-ant-your-key-here
   ```
5. Click **Create Web Service** — Render gives you a live URL

## Local development

```bash
npm install
ANTHROPIC_API_KEY=sk-ant-your-key-here node server.js
```
Then open http://localhost:3000

## File structure

```
mrsimon-proxy/
├── server.js        # Express proxy server
├── package.json
└── public/
    └── index.html   # The feedback tool frontend
```
