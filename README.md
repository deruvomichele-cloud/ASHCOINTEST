# One‑Click ASH — dApp (Buy / Sell)

Pagina statica che permette agli utenti di comprare e vendere ASH tramite il FixedPriceSwap.

File inclusi nel repository:
- `index.html` — frontend one‑click (MetaMask + ethers.js)
- `.github/workflows/pages.yml` — workflow GitHub Actions per pubblicare su GitHub Pages
- `README.md` — questo file

Configurazione embeddata (attuale):
- Swap contract: `0xE5104018379973BA5a65b82bC7E876b766357de6`
- ASH token: `0xd4FbB5E4Dd24C3F9A0F58Efa656A489D24E93BCd`
- USDC token (Mainnet): `0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eb48`

Pubblicazione (GitHub Pages)
1. Ho aggiunto un workflow GitHub Actions che deploya tutto il contenuto della cartella root su GitHub Pages automaticamente al push su `main`.
2. Dopo la run del workflow la pagina sarà disponibile (se il repository è pubblico) a:
   `https://deruvomichele-cloud.github.io/ASHCOINTEST/`

Nota: la prima esecuzione del workflow può impiegare alcuni secondi/minuti. Vai su Actions nel repo per vedere lo stato della run.

Test locale
- Clona il repo e apri index.html con un server statico:
  - `git clone https://github.com/deruvomichele-cloud/ASHCOINTEST.git`
  - `cd ASHCOINTEST`
  - `python3 -m http.server 8000` e apri `http://localhost:8000`

Sicurezza e checklist prima di invitare utenti
- Verifica che il contratto swap sia funded con ASH (per acquisti) e USDC (per vendite).
- Testa con piccole somme prima del lancio pubblico.
- Spiega chiaramente agli utenti che il meccanismo è centralizzato e che l'owner può modificare il rate o ritirare fondi.

Se vuoi, posso:
- Aggiungere branding (logo, colori) e migliorare UI (React/TS).
- Preparare una versione con supporto per più reti (testnet, Polygon).
- Aggiungere logica per permit (EIP‑2612) se i token lo supportano.
