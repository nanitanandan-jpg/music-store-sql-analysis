# 🎵 Music Store SQL Analysis

A beginner-friendly SQL project that analyzes a digital music store database to uncover business insights — top customers, best-selling genres, highest-revenue cities, and more.

---

## Project Overview

This project uses PostgreSQL to query a relational music store database modeled after real-world e-commerce data. The analysis is structured across three difficulty levels — Easy, Moderate, and Advanced — covering progressively complex SQL concepts from basic aggregations to CTEs and window functions.

---

## Database Schema

The database consists of 11 interrelated tables:

| Table | Description |
|---|---|
| `employee` | Store staff with reporting hierarchy |
| `customer` | Customer details and assigned support rep |
| `invoice` | Purchase records per customer |
| `invoice_line` | Line items per invoice (track-level) |
| `track` | Individual songs with price, duration, media type |
| `album` | Albums linked to artists |
| `artist` | Artist names |
| `genre` | Music genres |
| `media_type` | Audio format types |
| `playlist` | Named playlists |
| `playlist_track` | Many-to-many: playlists ↔ tracks |

![MusicDatabaseSchema](MusicDatabaseSchema.png)

---

## Questions Answered

### Set 1 — Easy
- Who is the senior-most employee based on job title?
- Which countries have the most invoices?
- What are the top 3 invoice totals?
- Which city generated the highest revenue? *(for a promotional music festival)*
- Who is the best customer by total spend?

### Set 2 — Moderate
- Return all Rock music listeners ordered alphabetically by email
- Which artists have written the most Rock tracks? *(Top 10)*
- Which tracks are longer than the average song length?

### Set 3 — Advanced
- How much has each customer spent on each artist?
- What is the most popular genre per country? *(ties included)*
- Who is the top-spending customer per country? *(ties included)*

---

## SQL Concepts Covered

- `JOIN` (multiple tables, multi-level joins)
- `GROUP BY` + aggregate functions (`SUM`, `COUNT`, `AVG`)
- Subqueries and nested `SELECT`
- `WITH` — Common Table Expressions (CTEs)
- `WITH RECURSIVE` — Recursive CTEs
- `ROW_NUMBER()` window function with `PARTITION BY`
- Filtering with `WHERE`, `HAVING`, `LIKE`
- `ORDER BY`, `LIMIT`

---

## Tools

- **PostgreSQL** — database engine
- **pgAdmin 4** — GUI for running queries and exploring the schema

---

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/rishabhnmishra/SQL_Music_Store_Analysis.git
cd SQL_Music_Store_Analysis
```

### 2. Set up the database

Open pgAdmin 4, create a new database, then run:

```sql
-- Load the full schema and data
\i Music_Store_database.sql
```

Or import via pgAdmin: right-click your database → **Restore** → select `Music_Store_database.sql`.

### 3. Run the queries

Open `Music_Store_Query.sql` in pgAdmin's Query Tool and execute any or all queries. Questions are clearly labeled by set and difficulty.

---

## Project Structure

```
SQL_Music_Store_Analysis/
├── Music_Store_Query.sql            # All analysis queries (Easy → Moderate → Advanced)
├── Music_Store_database.sql         # Full database schema + seed data
├── MusicDatabaseSchema.png          # Entity-relationship diagram
├── Music Store Analysis-Questions.pdf   # Original question set
├── album2.csv                       # Raw album data (CSV)
└── music store data.zip             # Raw dataset archive
```

---

## Reference

- Original tutorial: [YouTube — Rishabh Mishra](https://www.youtube.com/watch?v=VFIuIjswMKM)

---

## License

MIT
