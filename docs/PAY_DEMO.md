# CompileX Pay Demo

Live-Demo:

```text
https://compilex-token.dev/pay.html
```

Pay Guide:

```text
https://compilex-token.dev/pay-guide.html
```

## Zweck

CompileX Pay ist eine Testnet-Demo für einfache CMPX-Zahlungen auf Ethereum Sepolia.

Die Demo zeigt:

- Wallet-Verbindung,
- Payment Request,
- ERC-20 Transfer über MetaMask,
- Transaktionsbestätigung,
- Empfänger-Balance-Prüfung,
- Etherscan-Link zur Transaktion.

## Voraussetzungen

Der sendende Account benötigt:

1. **CMPX** für den Token-Transfer.
2. **SepoliaETH** für die Netzwerkgebühr.

Auch wenn CMPX übertragen wird, bezahlt die Wallet die Netzwerkgebühr immer in SepoliaETH.

Wenn CMPX oder SepoliaETH fehlt, kann MetaMask eine Warnung anzeigen oder die Transaktion kann fehlschlagen.

## Technischer Ablauf

Die Demo ruft über MetaMask eine Transaktion an den CMPX-Contract auf.

Die verwendete ERC-20 Funktion ist:

```solidity
transfer(address recipient, uint256 amount)
```

Der Contract ist:

```text
0xa1A09ba7357c5187d90E1De160bFd868151f3D8C
```

Das Netzwerk ist:

```text
Ethereum Sepolia
Chain ID: 11155111
```

## Funktionen der Demo

### Wallet verbinden

Die Website verbindet sich mit MetaMask und fordert Sepolia an.

### CMPX zu MetaMask hinzufügen

Der Button nutzt `wallet_watchAsset`, damit CMPX in MetaMask angezeigt werden kann.

### Payment Request aktualisieren

Die Seite erzeugt einen Payment Request auf Basis von:

- Empfängeradresse,
- CMPX-Betrag,
- optionaler Referenz.

### CMPX senden

Beim Klick auf „CMPX senden“ öffnet MetaMask eine Contract-Interaktion mit dem CMPX-Contract.

### Transaktion prüfen

Nach dem Senden wartet die Seite auf die Bestätigung. Danach kann die Transaktion auf Sepolia Etherscan geöffnet werden.

### Empfänger-Balance prüfen

Die Demo ruft `balanceOf(address)` auf und zeigt die CMPX-Balance des Empfängers an.

## Grenzen der Demo

Die Pay Demo ist bewusst einfach gehalten:

- kein Mainnet,
- kein Checkout-System,
- keine Warenkorb-Funktion,
- keine Server-Datenbank,
- keine Zahlungsforderung mit rechtlicher Abrechnung,
- keine Garantie für Wallet-Kompatibilität von Payment-URIs.

Die zuverlässigste Testmethode ist der direkte MetaMask-Transfer über den Button „CMPX senden“.

## Sicherheitshinweise

Private Keys oder Seed-Phrases werden niemals benötigt und dürfen niemals eingegeben oder weitergegeben werden.

CompileX Pay ist aktuell eine Sepolia-Testnet-Demo. Es gibt kein Gewinnversprechen, keine Anlageberatung und kein öffentliches Verkaufsangebot.
