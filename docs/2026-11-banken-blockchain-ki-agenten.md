# Banken auf der Blockchain & Zugang via KI-Agenten
### Wer macht was, seit wann, mit welchem belegten Transaktionsvolumen — und was bedeutet das für den globalen Kapitalmarkt?

*Stand: 6. November 2026 — reine Faktenbasis aus Primärquellen (Bank-Pressemitteilungen, Reuters, Bloomberg, WSJ, Coindesk, The Block) und Fachpublikationen (BIZ, IWF, Deutsche Bank Research, World Economic Forum). Wo verfügbar, werden konkrete $-Volumen genannt und mit kritischer Einordnung (z. B. PR-Ankündigung vs. tatsächliche On-Chain-Nutzung) versehen.*

---

## TL;DR

- **Ja**, mehrere große Banken bieten bereits Krypto-/Blockchain-Zugang für Kunden: JPMorgan (JPM Coin/Kinexys), Citigroup (Citi Token Services), BNY Mellon (Custody + Tokenisierung mit Goldman Sachs), Goldman Sachs (GS DAP), Fidelity (Crypto-Trading + Custody + Bitcoin-ETF), Sygnum/SEBA (Schweizer Krypto-Banken), Deutsche Bank (Custody für Ende 2026 angekündigt).
- **KI-Agenten-Zugang zur Blockchain via Bank**: Die **Sygnum Bank (Schweiz)** hat am **18. Mai 2026** als erste FINMA-regulierte Bank live On-Chain-Transaktionen getestet, die ein KI-Agent (Anthropic Claude über einen bankeigenen MCP-Server) aus Klartext-Anweisungen plant — der Agent hält aber **keine eigene Wallet/Signaturgewalt**, der Kunde signiert jede Transaktion selbst (Human-in-the-Loop). Kein Live-Kundenprodukt, sondern ein interner Pilot.
- Außerhalb klassischer Banken ist Agenten-Infrastruktur schon operativ: Coinbase **Agentic Wallets** + **x402**-Protokoll (seit Feb. 2026), Circle **Agent Stack**, Stripe/Tempo **Machine Payments Protocol**, MoonPay **MoonAgents Card** — alle mit echten On-Chain-Transaktionsvolumen (x402: ~69.000 aktive Agenten, >165 Mio. Transaktionen, 50 Mio. USD Volumen bis April 2026).
- **Belegte Großtransaktionen Richtung Blockchain** (Details Abschnitt 3): JPMorgans privates Kinexys-Netzwerk ~7 Mrd. USD/Tag (Juli 2026); BlackRocks tokenisierter Geldmarktfonds BUIDL ~2,87 Mrd. USD AUM; Goldman Sachs/BNY-Tokenisierungsinitiative zielt auf einen 7,1-Billionen-USD-Geldmarktfonds-Markt; Broadridges Blockchain-Repo-Plattform DLR ~359 Mrd. USD/Tag.
- **Wichtige Relativierung**: JPMorgans öffentlich auf Ethereum/Base verfügbares JPM Coin (JPMD) hat laut On-Chain-Daten (Stand 3.11.2026) seit Juni 2025 nur **48 Transfers** auf Base und seit Februar 2026 **keine einzige** mehr — ausstehendes Volumen nur ca. 1 Mio. USD. Das eigentliche Volumen läuft fast vollständig über JPMorgans **privates** Kinexys-Netzwerk, nicht über öffentliche Chains.
- **Bedeutung für den Kapitalmarkt**: Tokenisierter Finanzmarkt aktuell nur ~30–39 Mrd. USD (RWA.xyz), Prognosen für 2030 reichen von 2,7 bis 8,2 Billionen USD. Kernspannung ist **Stablecoins vs. Bankeinlagen** — JPMorgan, Citi, Bank of America und >12 weitere US-Banken bauen seit Juni 2026 ein gemeinsames tokenisiertes Einlagen-Netzwerk, um einer Einlagenabwanderung zu Stablecoins vorzubeugen.
- Regulatorisch zentral: US **GENIUS Act** (2025, Stablecoin-Rahmen) und der vorrückende **CLARITY Act** (Zuständigkeitsabgrenzung SEC/CFTC).

---

## 1. Banken mit Krypto-/Blockchain-Zugang für Kunden

| Bank/Institut | Angebot | Seit | Quelle |
|---|---|---|---|
| **JPMorgan Chase** | JPM Coin/JPMD (tokenisierte Dollar-Einlagen), Kinexys-Plattform (Zahlungen, Tokenisierung) | JPM Coin seit 2019 (institutionell), JPMD auf Base seit Juni 2025, auf Ethereum Mainnet seit Okt. 2026 | [CoinDesk](http://www.coindesk.com/markets/2026/10/19/jpmorgan-s-jpm-coin-representing-dollar-deposits-is-coming-to-ethereum-bloomberg) |
| **Citigroup** | Citi Token Services (tokenisierte Geschäftseinlagen), Citi Integrated Digital Assets Platform | Citi Token Services seit 2023 live | [bitcoin.com-Ranking](https://news.bitcoin.com/fidelity-bny-goldman-sachs-jpmorgan-morgan-stanley-citi-lead-strategys-bitcoin-banking-adoption/) |
| **BNY Mellon** | Krypto-Custody (Bitcoin/Ether), Tokenisierung von Geldmarktfonds-Anteilen mit Goldman Sachs | Custody seit 2022, MMF-Tokenisierung seit 23.7.2025 | [BNY Pressemitteilung](https://www.bny.com/corporate/global/en/about-us/newsroom/company-news/bny-and-goldman-sachs-launch-tokenized-money-market-funds-solution.html) · [Reuters](https://www.reuters.com/markets/wealth/goldman-bny-team-up-launch-tokens-tied-money-market-funds-2025-07-23/) |
| **Goldman Sachs** | GS DAP (Tokenisierungsplattform), institutioneller Bitcoin-Handel/-Exposure | GS DAP seit 2021, geplante Ausgliederung als eigenständiges Unternehmen seit Nov. 2024 angekündigt | [Bitbond-Übersicht](https://www.bitbond.com/resources/digital-bond-issuance-platforms) |
| **Fidelity** | Fidelity Crypto (Retail-Handel), Fidelity Digital Assets (institutionelle Custody), Bitcoin-ETF (FBTC) | Fidelity Digital Assets seit 2018 | [bitcoin.com-Ranking (Juli 2026)](https://news.bitcoin.com/fidelity-bny-goldman-sachs-jpmorgan-morgan-stanley-citi-lead-strategys-bitcoin-banking-adoption/) |
| **Morgan Stanley** | Bitcoin-ETF (Morgan Stanley Bitcoin Trust), Bitcoin-ETP-Zugang via E*TRADE | — | [bitcoin.com-Ranking](https://news.bitcoin.com/fidelity-bny-goldman-sachs-jpmorgan-morgan-stanley-citi-lead-strategys-bitcoin-banking-adoption/) |
| **Sygnum Bank (Schweiz)** | Krypto-Custody, Handel, Lending; Pilot für KI-Agent-gestützte On-Chain-Transaktionen | FINMA-Banklizenz seit 2019; KI-Agent-Pilot 18.5.2026 | [Sygnum Pressemitteilung](https://www.sygnum.com/news/sygnum-completes-first-live-ai-agent-driven-digital-asset-transactions-by-a-regulated-swiss-bank/) |
| **Deutsche Bank** | Bitcoin-Custody für institutionelle europäische Kunden | Angekündigt für Ende 2026 | [LinkedIn/Branchenbericht](https://www.linkedin.com/posts/arab-global-crypto-exchange-uae_deutsche-bank-is-preparing-to-offer-bitcoin-activity-7512839698516680704-ndNB) |
| **BayernLB** | Digitale Wertpapiere/Commercial Paper via Eurosystem-PONTES-Infrastruktur | Erste Live-Emission als Issuer 28.10.2026 (vorherige Pilotteilnahme seit 2024) | [Leaders League](https://www.leadersleague.com/en/news/bayernlb-completes-eur100m-digital-securities-transaction-using-eurosystem-s-pontes) |
| **Hana Bank (Südkorea)** | Digitale Anleihe über Euroclear-Blockchain-Plattform, T+0-Abwicklung | Erste Emission 19.9.2026 | [CoinDesk](https://www.coindesk.com/business/2026/09/21/hana-bank-issues-south-korea-s-first-digital-bond-using-euroclear-s-blockchain) |

**Einordnung (bitcoin.com-Ranking, Juli 2026):** Charles Schwab und TD Bank je 32 %, BNP Paribas/HSBC/Crédit Agricole/UBS je 30 %, Deutsche Bank/Mizuho 22 %, MUFG 18 %, Lloyds 17 %, SMBC/RBC je 13 % (Scoring-Methodik des jeweiligen Berichts, nicht amtlich).

---

## 2. KI-Agenten mit Blockchain-/Krypto-Zugang

### 2.1 Via regulierte Bank: Sygnum (Schweiz)

Am **18. Mai 2026** meldete Sygnum als erste FINMA-regulierte Schweizer Bank einen abgeschlossenen Pilot für KI-Agent-gesteuerte Live-Transaktionen auf einer Blockchain-Mainnet:

- Architektur: Anthropics **Claude** als Modell, eingebunden über einen bankeigenen **Model Context Protocol (MCP)**-Server — Claude bekommt keinen offenen Chain-Zugriff, sondern nur einen begrenzten, bank-kontrollierten Werkzeugsatz (Smart-Contract-Reader, Quote-Engines, Transaktions-Builder, Risiko-Flags).
- Der Kunde gibt eine Klartext-Anweisung; der Agent plant mehrstufige Transaktionen (Stablecoin-Transfers, Asset-Swaps, On-Chain-Lending, Token-Wrapping, Liquidity-Provisioning), bewertet Smart-Contract-Risiken und legt dem Kunden jeden Schritt zur Freigabe vor.
- **Entscheidend:** Jede Transaktion wird ausschließlich über die **Self-Custody-Wallet des Kunden auf dessen eigenem Gerät** signiert — private Keys verlassen nie die Kundenkontrolle. Der Agent selbst hält **keine Wallet und keine Spending-Autorität**.
- Der Pilot lief unter kontrollierten Bedingungen mit Geldern aus persönlicher Custody der Testperson — **keine echten Sygnum-Kunden, -Wallets oder -Produktionsinfrastruktur** waren beteiligt. Produktiver Rollout für Kunden ist noch nicht terminiert (steht unter regulatorischem/Compliance-Vorbehalt).

*(Quellen: [Sygnum](https://www.sygnum.com/news/sygnum-completes-first-live-ai-agent-driven-digital-asset-transactions-by-a-regulated-swiss-bank/) · [The Paypers](https://thepaypers.com/crypto-web3-and-cbdc/news/sygnum-becomes-first-swiss-bank-to-test-ai-agent-for-live-crypto-transactions) · [Branchenanalyse](https://blockainews.com/sygnum-claude-mcp-ai-agent-regulated-bank-execution-2026-05-18/))*

### 2.2 Außerhalb klassischer Banken: die "Machine Economy"-Infrastruktur

Da KI-Agenten keine Rechtsperson sind und damit kein KYC-fähiges Bankkonto eröffnen können, hat sich für autonome Agent-Zahlungen eine parallele Krypto-Infrastruktur etabliert — mit bereits messbarem Volumen:

| Anbieter | Produkt | Live seit | Belegtes Volumen |
|---|---|---|---|
| Coinbase | Agentic Wallets (MPC-Wallets, Spend-Limits) + **x402**-Protokoll (HTTP-402-Zahlungsstandard) | AgentKit Nov. 2024, Agentic Wallets Feb. 2026 | ~69.000 aktive Agenten, >165 Mio. Transaktionen, ~50 Mio. USD Volumen (Stand April 2026) |
| Circle | Agent Stack (USDC-Wallets für Agenten, Agent Marketplace) | Mai 2026 | — |
| Stripe / Tempo | Machine Payments Protocol (einmalige Budget-Autorisierung, dann autonomes Streaming von Zahlungen) | März 2026 | — |
| MoonPay | MoonAgents Card (virtuelle Mastercard-Debitkarte für Agenten, Stablecoin-Belastung) | Mai 2026 | — |
| Amazon/Coinbase/Stripe | Bedrock AgentCore Payments | 2026 (Preview) | — |

**Kritische Einordnung (Forbes, Spark.money, Chainalysis):** Ein Experiment von Redwood Research/METR gab einem KI-Agenten (Claude Opus 4.7) 5.000 USD und vier Tage Zeit, eigenständig Geld zu verdienen — der Agent erzielte in allen vier Durchläufen **0 USD**, weil er wiederholt an CAPTCHAs und Identitätsprüfungen scheiterte. Laut einem Keyrock-Report (Mai 2026) liegen 76 % aller Agent-Transaktionen unter der fixen 0,30-USD-Gebührengrenze von Visa — Kreditkarten-Rails sind für Mikrozahlungen von Agenten strukturell unwirtschaftlich, was den Trend zu Stablecoin-Rails erklärt.

---

## 3. Belegte Großtransaktionen Richtung Blockchain (mit Zahlen)

| Institut/Produkt | Volumen | Zeitpunkt/Stand | Einordnung | Quelle |
|---|---|---|---|---|
| **JPMorgan Kinexys** (privates Netzwerk, Blockchain Deposit Account) | **~7 Mrd. USD/Tag** Gesamtvolumen, davon ca. 3,5 Mrd. USD/Tag BDA | Juli 2026 (von >5 Mrd. USD/Tag in 2025 gestiegen) | Entspricht nur ~0,03 % von JPMorgans gesamtem Zahlungsvolumen (12 Bio. USD/Tag) | [Tiger Research](https://reports.tiger-research.com/p/jpmorgan-kinexys-how-should-banks-use-eng) |
| **JPM Coin/JPMD auf öffentlicher Chain (Base)** | Nur **48 Transfers** seit Juni 2025, keine seit 20.2.2026; ausstehend **~1 Mio. USD** | Stand 3.11.2026 | **Relativierung:** die PR-Ankündigung (Ethereum-Expansion Okt. 2026) steht in starkem Kontrast zur realen Nutzung auf öffentlichen Chains — das eigentliche Volumen bleibt privat (Kinexys) | [Tiger Research](https://reports.tiger-research.com/p/jpmorgan-kinexys-how-should-banks-use-eng) |
| **BlackRock BUIDL** (tokenisierter Geldmarktfonds, Verwaltung durch Securitize) | **~2,87 Mrd. USD AUM**, über 7–9 Blockchains | Juli 2026 (Start März 2024 mit 100 Mio. USD) | Größter tokenisierter US-Treasury-Fonds; BlackRock hat im Mai 2026 bei der SEC zwei weitere tokenisierte Fonds plus On-Chain-Anteile für einen bestehenden 7-Mrd.-USD-Geldmarktfonds beantragt | [Spark.money](https://spark.money/research/tokenized-money-market-fund-landscape) |
| **BNY/Goldman Sachs Tokenisierungsinitiative** (GS DAP + LiquidityDirect) | Zielmarkt: **7,1 Billionen USD** (gesamter US-Geldmarktfonds-Markt) | Live seit 23.7.2025; Teilnehmer: BlackRock, Fidelity, Federated Hermes, BNY Dreyfus, Goldman Sachs Asset Management | Erste US-Umsetzung "gespiegelter" Tokenisierung von MMF-Anteilen zur besseren Nutzung als Collateral | [The Block](https://www.theblock.co/news/business/2025-07-23-bny-goldman-sachs-tokenized-money-market-363970) |
| **Broadridge DLR** (konkurrierende Blockchain-Repo-Plattform) | **~359 Mrd. USD/Tag** Durchschnittsvolumen | September 2026 | Übertrifft JPMorgans kumuliertes historisches Volumen allein an einem Tag deutlich | [Tiger Research](https://reports.tiger-research.com/p/jpmorgan-kinexys-how-should-banks-use-eng) |
| **BayernLB** (Deutschland) | **100 Mio. Euro** Commercial Paper, Emittent selbst (Investor: Siemens AG) | 28.10.2026, Abwicklung in Minuten via Eurosystem-PONTES in Zentralbankgeld | Erste Live-Emission als Emittent (nicht nur Pilotteilnahme); DekaBank als Verwahrstelle, Deutsche Bank für Zahlungsdienste | [Leaders League](https://www.leadersleague.com/en/news/bayernlb-completes-eur100m-digital-securities-transaction-using-eurosystem-s-pontes) |
| **Hana Bank** (Südkorea, zweitgrößte Bank, ~500 Mrd. USD AUM) | **100 Mio. USD** digitale Anleihe via Euroclear-Blockchain | 19.9.2026, T+0-Abwicklung (sonst 3–5 Geschäftstage) | Erste direkte Nutzung von Euroclears DLT-Infrastruktur durch ein koreanisches Institut, vor Südkoreas landesweitem Tokenisierungs-Rahmen (Start Feb. 2027) | [CoinDesk](https://www.coindesk.com/business/2026/09/21/hana-bank-issues-south-korea-s-first-digital-bond-using-euroclear-s-blockchain) |
| **Schroders (1,1 Bio. USD AUM)** | Tokenisiertes Emerging-Markets-Anleihen-Fonds (SISF) auf Solana via Centrifuge | 4.11.2026 | Centrifuge-Plattform insgesamt >750 Mio. USD tokenisiert (inkl. Janus Henderson, Baillie Gifford, New York Life, JPMorgan) | [Solana Compass](https://solanacompass.com/news/schroders-brings-its-emerging-market-bond-fund-to-solana-through-centrifuge) |
| **Gesamtmarkt tokenisierte US-Treasuries/Geldmarktfonds** | **~14 Mrd. USD** von insgesamt ~39 Mrd. USD tokenisiertem RWA-Markt | November 2026 (RWA.xyz-Daten via CoinDesk) | Cash-ähnliche Produkte dominieren bislang; aktiv gemanagte Strategien (Anleihen, Kredite) sind der nächste Schritt | [Solana Compass](https://solanacompass.com/news/schroders-brings-its-emerging-market-bond-fund-to-solana-through-centrifuge) |

**Wichtigster Befund:** Die größten real belegten Volumen laufen fast ausschließlich über **private/permissioned Netzwerke** der Banken selbst (Kinexys, GS DAP, BNY-Mirror-Tokens), nicht über öffentliche, permissionless Chains — trotz Schlagzeilen wie "JPMorgan bringt Einlagen auf Ethereum". Die tatsächliche Nutzung auf öffentlichen Chains (JPMD auf Base) ist nach den verfügbaren On-Chain-Daten verschwindend gering.

---

## 4. Bedeutung für den globalen Kapitalmarkt

- **Marktgröße heute vs. Prognose:** Der tokenisierte Finanzmarkt (ohne Stablecoins) liegt aktuell bei ca. 30–39 Mrd. USD (RWA.xyz/Callan) — ein Rundungsfehler gegenüber globalen Kapitalmärkten. Prognosen für 2030 reichen von konservativ 2,7 Billionen über eine Basisannahme von 5,5 Billionen bis optimistisch 8,2 Billionen USD (Callan-Research). Separat: Stablecoins + digitale Geldmarktfonds + tokenisierte Einlagen könnten laut BNY-Analyse bis 2030 zusammen 3,6 Billionen USD erreichen.
- **Strukturelle Spannung Stablecoins vs. Bankeinlagen:** Laut WSJ (Juni 2026) bauen JPMorgan, Citi, Bank of America und über ein Dutzend weitere US-Banken ein gemeinsames tokenisiertes Einlagen-Netzwerk ("the bridge"/"the chain"), explizit um einer Einlagenabwanderung zu Stablecoins vorzubeugen — Einlagen sind die Basis, auf der Banken Kredite vergeben; eine Abwanderung in Stablecoin-Wallets würde dieses Modell untergraben.
- **Regulatorische Weichenstellung:** Der US-**GENIUS Act** (2025) schuf den ersten föderalen Rahmen für Stablecoins (Reserve-, Rücknahme-, AML-Pflichten). Der vorrückende **CLARITY Act** soll die Zuständigkeit zwischen SEC (Wertpapiere) und CFTC (Rohstoffe) für Digital Assets klären — laut SEC-Zeugenaussage (März 2026) hält regulatorische Unsicherheit derzeit 66 % der institutionellen Investoren von stärkerem Engagement ab.
- **Tokenisierung senkt Kosten, schafft aber keinen neuen Wert per se:** Laut BIZ-Analysen (zitiert in SEC-Testimony) zeigen tokenisierte Anleihen bereits messbar engere Bid-Ask-Spreads (−5,3 %, bei Retail-Anleihen −10,8 %) und niedrigere Emissionsrenditeaufschläge (−23,9 %) — die Technologie reduziert Friktion/Kosten, verändert aber nicht den fundamentalen Wert eines Assets.
- **KI-Agenten als neue ökonomische Akteure:** Sollte sich die "Machine Economy" (Agent-zu-Agent-Zahlungen, autonome Mikrotransaktionen) wie in Abschnitt 2.2 beschrieben durchsetzen, entstünde ein paralleler Zahlungsverkehr-Layer, der strukturell außerhalb des klassischen, KYC-basierten Bankensystems läuft — mit noch weitgehend unklarer Regulierung (wer haftet, wenn ein Agent fehlerhaft/betrügerisch handelt?).
- **Konkreter, bereits messbarer Nutzen:** T+0-Abwicklung statt T+3-5 (Hana Bank, BayernLB/PONTES), 24/7-Verfügbarkeit, bessere Collateral-Mobilität (BNY/Goldman-MMF-Tokenisierung) — das sind die primären, schon heute nachweisbaren Vorteile, nicht spekulative neue Renditen.

---

## Fazit

Ja — mehrere große, etablierte Banken (JPMorgan, Citigroup, BNY Mellon, Goldman Sachs, Fidelity, Sygnum u. a.) bieten bereits heute Kunden Zugang zu Krypto/Blockchain, mit teils seit Jahren laufenden, teils 2025/26 gestarteten Angeboten. **KI-Agenten-Zugang zur Blockchain via Bank** existiert bislang nur als kontrollierter interner Pilot (Sygnum, Mai 2026) mit strikter menschlicher Signatur-Kontrolle — kein Agent hat heute bei einer regulierten Bank eigenständige Verfügungsgewalt über Kundengelder. Außerhalb des Bankensystems ist die Infrastruktur für autonome Agent-Zahlungen (x402, Agentic Wallets) dagegen schon operativ und verzeichnet reales, wenn auch noch kleines Volumen. Bei den **Großtransaktionen der Banken selbst** zeigt sich eine wichtige Diskrepanz zwischen Schlagzeilen (öffentliche Chains) und tatsächlichem Volumen (weit überwiegend private/permissioned Netzwerke). Für den globalen Kapitalmarkt bedeutet das: Tokenisierung ist real und wächst, bleibt aber mengenmäßig noch ein Nischenphänomen gegenüber dem traditionellen Finanzsystem — mit der Stablecoin-vs.-Bankeinlagen-Frage als dem eigentlichen strukturellen Spannungsfeld der kommenden Jahre.

*Recherche KI-unterstützt erzeugt am 06.11.2026 für otype.*
