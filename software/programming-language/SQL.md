---
layout: default
---
The Stuctural Quary Language(SQL) is based on relational model, so basically it operates on the columns(selecting the attributes) and the rows(filtering the attributes).
# Paradigm
```sql
SELECT column -- Return, last excution precedence
FROM table;
-- Optional constraints, define virtual table
WHERE expressions -- Global filter, first execution precedence
GROUP BY column/expressions -- Execute after WHERE
HAVING expression -- Group filter, execute after GROUP
ORDER BY column DESC/ASC
LIMIT value OFFSET value;
```
# Aggregation function
Get multiple values, return single value
```sql
MIN();
MAX();
SUM();
AVG();
COUNT();
```
# Window function
Paradigm: aggregation + OVER expression
```sql
RANK(); -- Return rank of the entries inside OVER
SELECT column,
       aggregation function OVER (
         PARTITION BY column)
FROM table;
```

