# Intermediate SQL Notes

### Table of contents


- [Window Funtions](#window-funtions)


## Window Funtions    

A window function performs a calculation across a set of table rows that are related to the current row within a specific "window" or subset of data. This is comparable to the type of calculation that can be done with an aggregate function  (such as SUM(), AVG(), COUNT(), etc.).

But unlike regular aggregate functions, use of a window function does not cause rows to become grouped into a single output row — the rows retain their separate identities.


**Syntax:**

```sql
FUNCTION() OVER (PARTITION BY column_name ORDER BY column_name)
```

A window function always has two components. This second part here defines your window:

```sql
OVER (PARTITION BY column_name ORDER BY column_name)
```

Your window here is how you want to be viewing your data when you're applying your function

- PARTITION BY: divides the result set into groups (optional).

- ORDER BY: defines the order of processing rows within the partition.
