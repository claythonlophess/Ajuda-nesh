# AjudaMesh - Rede de Emergência Comunitária Offline

Uma aplicação web offline-first para coordenação de emergências em cenários sem internet, simulando uma rede mesh local.

## 🚀 Como Executar

### 1. Backend (Node.js + Express + Socket.io)

```bash
cd backend
npm install
npm run dev
```

O servidor roda em http://localhost:3000

### 2. Frontend (React + Vite + Tailwind + PWA)

```bash
cd frontend
npm install
npm run dev
```

Acesse http://localhost:5173

Para build de produção:
```bash
cd frontend
npm run build
```

Então sirva o `dist` com o backend (já configurado para servir static files).

## 🛠️ Configuração para Rede Local / Raspberry Pi

1. Configure um hotspot Wi-Fi no dispositivo servidor.
2. Defina o IP fixo do servidor como 192.168.4.1
3. Acesse via http://192.168.4.1:3000 (ou configure mDNS para ajudamesh.local)
4. Todos os dispositivos conectados ao Wi-Fi podem usar a app.

## Funcionalidades Implementadas (MVP)

- ✅ SOS em tempo real com broadcast WebSocket
- ✅ Chat comunitário
- ✅ Board de abrigos com atualização de ocupação
- ✅ Reporte e lista de desaparecidos
- ✅ Interface mobile-first com tema de emergência
- ✅ PWA configurado para uso offline
- ✅ Persistência com SQLite (em memória para demo, fácil trocar para arquivo)
- ✅ Simulação de múltiplos usuários

## Próximos Passos (Extras)

- Integração completa IndexedDB para sync offline
- Service Worker avançado para cache completo
- Geolocation API
- Autenticação simples por nickname
- Export de dados / logs

## Stack

- **Frontend**: React 18, Vite, TailwindCSS, Socket.io-client, PWA
- **Backend**: Node.js, Express, Socket.io, SQLite3

**Feito para impacto real em desastres.** 

Qualquer dúvida, contribua ou adapte para o contexto local!
