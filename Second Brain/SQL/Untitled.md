-   Join (inner vs left is mostly what we care about)
-   Aggregation / grouping (sum, average, max, min)    
-   what a "having" statement does, and when to ue it
-   order by    
-   coalesce (what it does and when you'd use it)
-   ordered analytical / window functions (row_number, rank, dense rank() etc)    
-   union / union all and what the difference is between them
-   subqueries


-   Question: What is a DISTINCT clause? Answer: Used to return only unique (different) values
-   Question: What is the difference between a UNION and UNION ALL? Answer: Union extracts the rows that are being specified in the query while Union All extracts all the rows including the duplicates (repeated values) from both the queries.    
-   Question: How do Window Functions work? Answer: Window Functions execute calculations at the row level with a related set of values. Compared to using aggregate functions like SUM(), window functions don’t collapse the output of the rows into a single value. Rather, the output is returned for every row.
-   Question: What is the difference between a primary and a foreign key? Answer: Primary keys are either a column or a set of columns in a table that hold uniquely identifiable rows in the table. While a foreign key could be a column or a set of columns in a table whose values correspond to the values of the primary key in another table.
-   Question: What is the difference between LEAD and LAG? Answer: LEAD will give you the rows AFTER the row you are finding a value for. LAG will give you the rows BEFORE the row you are finding a value for