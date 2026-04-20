# Deploy PaguePay Dashboard → Firebase Hosting

## Pré-requisitos
Node.js instalado (https://nodejs.org)

## Passos

### 1. Instalar Firebase CLI (uma vez só)
```bash
npm install -g firebase-tools
```

### 2. Login no Firebase
```bash
firebase login
```

### 3. Na pasta `pagueplay-deploy/`, fazer o deploy:
```bash
firebase deploy --only hosting
```

### 4. URL do site após deploy:
```
https://pagueplay-70a8c.web.app
https://pagueplay-70a8c.firebaseapp.com
```

## Estrutura do projeto
```
pagueplay-deploy/
├── firebase.json       ← configuração do hosting
├── .firebaserc         ← projeto Firebase: pagueplay-70a8c
├── DEPLOY.md           ← este arquivo
└── public/
    └── index.html      ← dashboard com Firebase Analytics integrado
```

## Atualizar o site (quando tiver nova versão do HTML)
Substitua o arquivo `public/index.html` e rode novamente:
```bash
firebase deploy --only hosting
```
