# CompileX (CMPX)

**CompileX** ist ein Bitcoin-inspiriertes digitales Asset für Builder, Entwickler und technische Communities.

Der aktuelle Stand ist ein verifizierter ERC-20-Prototyp auf **Ethereum Sepolia**.

> Kein Investment-Angebot. Keine Anlageberatung. Kein Gewinnversprechen. CompileX ist aktuell ein experimentelles Testnet-Projekt.

---

## Live-Links

| Bereich | Link |
|---|---|
| Website | https://compilex-token.dev |
| Pay Demo | https://compilex-token.dev/pay.html |
| Pay Guide | https://compilex-token.dev/pay-guide.html |
| Sepolia Token | https://sepolia.etherscan.io/token/0xa1A09ba7357c5187d90E1De160bFd868151f3D8C |
| Verifizierter Contract-Code | https://sepolia.etherscan.io/address/0xa1A09ba7357c5187d90E1De160bFd868151f3D8C#code |

---

## Token-Parameter

| Eigenschaft | Wert |
|---|---|
| Name | CompileX |
| Symbol | CMPX |
| Max Supply | 21.000.000 CMPX |
| Decimals | 8 |
| Minting | Nicht vorhanden |
| Owner/Admin | Nicht vorhanden |
| Blacklist | Nicht vorhanden |
| Transfersteuer | Nicht vorhanden |
| Burn | Aktiv |
| Permit / EIP-2612 | Aktiv |
| Netzwerk | Ethereum Sepolia |
| Contract | `0xa1A09ba7357c5187d90E1De160bFd868151f3D8C` |

---

## Warum Bitcoin-inspiriert?

CompileX übernimmt einige einfache, nachvollziehbare Prinzipien:

1. feste Obergrenze von 21 Millionen,
2. 8 Dezimalstellen,
3. keine nachträgliche Mint-Funktion,
4. keine zentralen Admin-/Owner-Rechte,
5. keine Transfersteuer oder Blacklist,
6. öffentlicher, überprüfbarer Contract-Code.

Wichtig: CompileX ist **kein Bitcoin-Fork** und keine eigene Proof-of-Work-Blockchain. Der aktuelle Prototyp ist ein ERC-20-Token.

---

## Projektstruktur

```text
contracts/CompileXToken.sol        Fixed-Supply ERC-20 Contract
test/CompileXToken.ts              Automatisierte Tests
scripts/deploy.ts                  Deployment Script
scripts/transfer.ts                Beispiel-Transfer Script
docs/                              Architektur, Tokenomics, Pay-Demo, Checklisten
branding/                          Logo-/Coin-Assets
.github/workflows/test.yml         GitHub Actions Testworkflow
```

---

## Installation

```bash
npm install
```

## Tests

```bash
npm test
```

## Compile

```bash
npm run compile
```

---

## Lokales Deployment

Terminal 1:

```bash
npx hardhat node
```

Terminal 2:

```bash
npm run deploy:local
```

---

## Sepolia Deployment

1. `.env.example` zu `.env` kopieren.
2. Sepolia RPC, Test-Wallet Private Key und Etherscan API Key eintragen.
3. Deployment ausführen:

```bash
npm run deploy:sepolia
```

Danach kann der Contract verifiziert werden:

```bash
npx hardhat verify --network sepolia <TOKEN_ADDRESS> <INITIAL_RECEIVER>
```

Der aktuelle verifizierte Sepolia-Contract ist:

```text
0xa1A09ba7357c5187d90E1De160bFd868151f3D8C
```

---

## CompileX Pay Demo

Die Pay Demo zeigt einfache CMPX-Zahlungen auf Sepolia:

- Wallet verbinden,
- Empfängeradresse eintragen,
- CMPX-Betrag festlegen,
- ERC-20 `transfer()` über MetaMask ausführen,
- Transaktionsstatus prüfen,
- Empfänger-Balance prüfen.

Wichtig: Der sendende Account benötigt **CMPX** und zusätzlich **SepoliaETH** für Gas.

---

## Sicherheit

Niemals committen:

```text
.env
Private Keys
Seed Phrases
node_modules/
artifacts/
cache/
```

Vor Mainnet-Schritten sind mindestens nötig:

- externer Smart-Contract-Review,
- Audit-Vorbereitung,
- rechtliche Prüfung,
- steuerliche Prüfung,
- finale Tokenomics,
- klare Wallet-/Treasury-Struktur.

---

## Lizenz

MIT. Siehe `LICENSE`.
