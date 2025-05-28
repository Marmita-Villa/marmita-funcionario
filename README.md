
# Sistema de Marmitas para Funcionários

Sistema web em React + Firebase onde os funcionários fazem pedidos de marmita e visualizam relatórios.

## 🚀 Rodar Localmente

```bash
npm install
npm run dev
```

## 🌐 Publicar na Vercel

1. Conecte o GitHub à Vercel
2. Configure as variáveis de ambiente (.env)
3. Deploy automático após push

## ✅ Variáveis de Ambiente

```
VITE_API_KEY=
VITE_AUTH_DOMAIN=
VITE_PROJECT_ID=
VITE_STORAGE_BUCKET=
VITE_MESSAGING_SENDER_ID=
VITE_APP_ID=
```

## 🔐 Regras de Segurança do Firestore

```js
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```
