# Keeper-App-ICP

A simple note-keeping app built for the Internet Computer using Motoko (backend) and React (frontend).

---

## Project Structure

```
src/
├── dkeeper/                # Motoko backend canister code
│   └── main.mo
├── dkeeper_assets/         # Frontend assets and source code
│   ├── assets/             # Static assets (favicon, logo, styles, etc.)
│   └── src/
│       ├── index.html
│       ├── index.jsx
│       └── components/     # React components (App.jsx, Header.jsx, etc.)
└── declarations/           # Auto-generated JS/TS canister bindings
```

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14+ recommended)
- [DFINITY SDK (dfx)](https://internetcomputer.org/docs/current/developer-docs/setup/install/)
- npm

### Install Dependencies

```bash
npm install
```

### Local Development

Start the local Internet Computer replica and deploy canisters:

```bash
dfx start --background
dfx deploy
```

Start the frontend development server:

```bash
npm start
```

- The frontend will be available at [http://localhost:8080](http://localhost:8080)
- The backend canister runs at [http://localhost:8000](http://localhost:8000)

---

## Usage

- Add, view, and delete notes in the web UI.
- Notes are stored on the Internet Computer via the Motoko backend.

---

## Troubleshooting

- If you see errors about `webpack-cli`, run:
  ```bash
  npm install webpack-cli@4.10.0 --save-dev
  ```
- If you see errors about missing canister IDs, ensure you have run `dfx deploy`.

---

## Environment Variables

- Canister IDs are injected automatically by webpack using `process.env`.
- For production, ensure `NODE_ENV=production` is set.

---

## Learn More

- [DFINITY Quick Start](https://internetcomputer.org/docs/current/developer-docs/quickstart/quickstart-intro)
- [Motoko Language Guide](https://internetcomputer.org/docs/current/motoko/main/motoko)
- [React Documentation](https://reactjs.org/)

---

