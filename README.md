<div align="center">
  <img src="repository-assets/cover.jpg" width="100%" alt="CrossDrop Banner" />
  <br/>
  <img src="repository-assets/crossdrop.png" width="280" alt="CrossDrop Logo" />
</div>

<h1 align="center">CrossDrop</h1>

<p align="center"><b>Targeted marketing and precision airdrops for the next generation of on-chain audiences.</b></p>

<p align="center">
  <img src="https://img.shields.io/badge/Winner-Arbitrum%20Track-2D3748?style=for-the-badge&logo=arbitrum&logoColor=96DBFD" />
  <img src="https://img.shields.io/badge/Built%20at-ETHIndia%202023-3c63ff?style=for-the-badge&logo=ethereum&logoColor=white" />
  <img src="https://img.shields.io/badge/Stack-React%20%2B%20Node-38b2ac?style=for-the-badge&logo=react" />
  <img src="https://img.shields.io/badge/Data-Airstack%20%7C%20SimpleHash-8b5cf6?style=for-the-badge" />
</p>

---

## About

- **What** — CrossDrop turns broadcast airdrops into surgical campaigns. Protocols define audiences with cross-chain on-chain filters and ship rewards only to wallets that match.
- **Who** — Team `teamgpt`: Gyanesh Samanta, Priyadarsh S S, and Siddhardha.
- **When** — Built across the ETHIndia 2023 hackathon weekend (Dec 8–10, 2023).
- **Where** — [ETHIndia 2023](https://ethindia.co/), Bangalore. **Winner of the Arbitrum track.**
- **Why** — Most airdrops are won by Sybil farms, not real users. We wanted protocols to find their true champions, not their loudest farmers.

## The Story

In 2023, airdrops were Web3's favorite go-to-market tool — and also its most wasteful. Bots automated qualification, allocations got diluted, and protocols had no way to tell a power user from a Sybil cluster. Marketing budgets evaporated into wallets that never came back.

CrossDrop reframes the problem. Instead of "drop tokens broadly and pray," it gives PMs a **targeting console**: filter by protocol interactions, NFT holdings, transaction history, and social graph signals — across multiple chains in a single query. Under the hood we lean on **Airstack's GraphQL API** for social and transactional graphs, **SimpleHash** for multi-chain NFT data, and **Crossmint** for verification rails. Distribution itself runs on **Arbitrum** for fast, cheap settlement.

By the end of the weekend we had a working dashboard, a Node + MongoDB backend wired to three data providers, and an end-to-end demo that took the **Arbitrum track win**. **43 commits** across **3 contributors** in **3 days**.

## Gallery

<div align="center">
  <img src="repository-assets/1.png" width="45%" alt="Preview 1" />
  <img src="repository-assets/2.png" width="45%" alt="Preview 2" />
  <br/>
  <img src="repository-assets/3.png" width="30%" alt="Preview 3" />
  <img src="repository-assets/4.png" width="30%" alt="Preview 4" />
  <img src="repository-assets/5.png" width="30%" alt="Preview 5" />
</div>

---

## Tech Stack

- **Chain:** Arbitrum (L2 settlement)
- **Data:** Airstack GraphQL, SimpleHash, Moralis
- **Verification:** Crossmint modules
- **Frontend:** React 18, Vite, Chakra UI, Framer Motion, wagmi + viem, RainbowKit
- **Backend:** Node.js, Express, MongoDB / Mongoose, dotenv
- **Tooling:** nodemon, ESLint

## Repo Structure

```
ETHIndia23-teamgpt/
├── client/                 # React + Vite frontend (Chakra + RainbowKit)
├── controllers/            # Express route handlers
├── routes/                 # API route definitions
├── models/                 # Mongoose schemas
├── services/               # Business logic
├── modules/                # Reusable feature modules
├── Crossmint Modules/      # Crossmint integration
├── Web3Gates/              # On-chain gating logic
├── airstack graphql/       # Airstack query bundles
├── web3apis/               # Chain RPC helpers
├── constants/              # Shared constants
├── helper.js               # Shared helpers
├── index.js                # Express entry point
└── package.json
```

## Getting Started

**Prerequisites:** Node.js 16+, MongoDB connection string, API keys for Airstack and SimpleHash.

```bash
git clone https://github.com/GyaneshSamanta/ETHIndia23-teamgpt.git
cd ETHIndia23-teamgpt

# Backend
npm install
# create .env with MONGO_URI, AIRSTACK_KEY, SIMPLEHASH_KEY, CROSSMINT_KEY
npm start                  # nodemon index.js

# Frontend
cd client
npm install
npm run dev                # vite dev server
```

## Contributing

PRs welcome. Open an issue first for any non-trivial change so we can align on direction.

## License

ISC. See `package.json`.

## Team / Credits

Built at ETHIndia 2023 by:

- [Gyanesh Samanta](https://github.com/GyaneshSamanta)
- [Priyadarsh S S](https://github.com/Priyadarshsspatnaik)
- [Siddhardha](https://github.com/siddhardha123)

<div align="center">
  <br/>
  <i>Winner of the Arbitrum track at ETHIndia 2023.</i>
</div>
