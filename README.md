# 🎧 SQL Practice – (Chinook Database)

## 📌 Overview
This project is part of my ongoing **SQL practice challenge** using the **Chinook SQLite database**.  
The Chinook database models a digital media store, with tables for **customers, invoices, tracks, albums, artists, genres, and more**.  
Today, I focused on writing **intermediate SQL queries** to extract meaningful business insights.

---

## 🗂️ Database Used
- **Chinook SQLite** (can be downloaded from [Chinook Database GitHub](https://github.com/lerocha/chinook-database))

---

## ✅ Queries Covered Today
This session explored:
- Joins across multiple tables  
- Grouping and aggregation with `HAVING`  
- Subqueries for filtering  
- Ranking and ordering results  

---

## 🧠 Business Questions Answered
1. **Albums with more than 10 tracks**
  
2. **Top 5 customers who spent the most on Rock music**

3. **Tracks longer than the average track length**

5. **Customers and the total number of invoices they have**

7. **Most popular media type by tracks sold**

---

## 💻 Sample Query

```sql
-- Find tracks that are longer than the average track length
SELECT 
    Name as Tracks_name,
    Milliseconds as Duration
FROM 
    tracks
WHERE Milliseconds > (
    SELECT avg(Milliseconds)
    FROM tracks
)
LIMIT 5
;

