# Feraset-Case-Study
Oracle PL/SQL procedure that generates monthly market reports from FERASET_IY—top categories by app count, total downloads, and revenue-per-download—with robust date normalization and tag splitting. Parameters: p_limit, p_month ('YYYY-MM'). Outputs a formatted DBMS_OUTPUT console report.

Here’s a short English **README.md**:

---

# FERASET Case – PL/SQL Monthly Analysis

Oracle PL/SQL procedure `PROC_FERASET_ANALIZ` used during the FERASET case to analyze **FERASET\_IY** and print monthly insights: top categories by app count, total downloads, and revenue-per-download (RPD). Includes robust date normalization and tag splitting.

## Requirements

* Oracle Database 11g+
* Table **FERASET\_IY** with: `Last_Update_Date`, `Tags`, `Downloads`, `TTD_Revenue`

## Usage

```sql
SET SERVEROUTPUT ON SIZE UNLIMITED;
@proc_feraset_analiz.sql

EXEC PROC_FERASET_ANALIZ;                          -- all months
EXEC PROC_FERASET_ANALIZ(p_month => '2025-07');    -- single month
EXEC PROC_FERASET_ANALIZ(p_limit => 15, p_month => '2025-08');
```

## Output

Formatted `DBMS_OUTPUT` report by month (top categories, downloads, RPD).

## License

MIT
