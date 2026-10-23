# VendiCose S.p.A. — Database vendite e logistica (MySQL)

Progettazione di un database relazionale per **VendiCose S.p.A.**, catena di supermercati con centri di distribuzione, punti vendita e gestione del magazzino, e analisi delle performance di vendita e di stock tramite query SQL.

**Autrice:** Carol Pagano · **Strumento:** MySQL Workbench

---

## Cosa contiene il progetto

- **Progettazione del modello dati**: modello concettuale (E-R) e modello logico relazionale, con 9 tabelle — anagrafiche (Region, Warehouse, Category, Store, Product) e tabelle transazionali e di associazione (SalesHeader, SalesDetail, Inventory, Restock).
- **Creazione e popolamento** del database con dati realistici (centri di distribuzione e negozi su più regioni italiane).
- **Vista SQL** (`v_ReportIncome`) che unisce le tabelle di vendita e fa da base per i report, così la logica di calcolo è definita una volta sola.
- **Query di analisi**: fatturato e pezzi venduti per regione, scontrini emessi, volume delle merci stoccate per centro di distribuzione.

## Tecniche SQL usate

Progettazione di uno schema a 9 tabelle con chiavi esterne · `CREATE VIEW` (vista riutilizzabile per i report) · `JOIN` multipli · aggregazioni con `GROUP BY`, `SUM`, `COUNT(DISTINCT …)` · `ORDER BY`.

## File

| File | Contenuto |
|---|---|
| `VendiCoseSpA.sql` | Script completo: creazione, popolamento, vista e query di analisi (commentato) |
| `VendiCoseSpA_Modello Concettuale E-R2.png` | Modello concettuale (entità-relazione) |
| `VendiCoseSpA_Modello Logico Relazionale.png` | Modello logico relazionale |
| `VendiCoseSpA_Relazione_.pdf` | Relazione del progetto |
| `VendiCoseSpA_Tabella.xlsx` | Dati di supporto |

## Come eseguire

In MySQL Workbench, apri ed esegui `VendiCoseSpA.sql`. Lo script ricrea il database da zero a ogni esecuzione (`DROP DATABASE IF EXISTS`), quindi è ripetibile senza errori.
