## Create node js server

```json
  "scripts": {
    "dev": "nodemon src/server.ts",
    "build": "tsc",
    "prod": "node dist/server.js",
    "test": "echo \"success: tested successfully\" && exit 0"
  }
```

## Install jenkins

- Install jenkins
- Install Plugins
- Setup node js on jenkis server
- Create configure (GitHub hook trigger for GITScm polling
?)
- Select git branch `*/main`
- Build step (Execute shell)
- Start on `http://localhost:8080`

```bash
npm install
npm run build
npm run test
```

## Setup ngrok to access jenkis via public url

- Install ngrok
- Run `ngrok http 8080`
- Now this forword to ` https://earmark-unsteady-entrap.ngrok-free.dev -> http://localhost:8080 `
- This is public access url

## Setup on github (web-hook)

- Go to the repository
- Click  on setting
- click on `Webhooks`
- Add webhook
- Payload url `https://earmark-unsteady-entrap.ngrok-free.dev/github-webhook`
- Clock on `Add webhook`

## Run in your code terminal

```bash
git add .
git commit -m "testing jenkins webhook"
git push
```