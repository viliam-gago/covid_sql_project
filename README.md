# Engeto Project 1 - SQL data handling process

The purpose of this project is practice data preparation. We received information about current Covid-19 situation around the world, along with information about particular countries, distributed into various tables. The process could be described as case study, where we are creating dataset along with requirements of data scientist, for example for further predictive analysis.


## Notes to the script:
- ##### Before creating the final table, I created four sub-tables, all listed in "queries_sub_tables". There is commented the query for creating corresponding table, along with deleting it.
- ##### Sub tables from above are used in final joininq_query -> "final_table"

## Work notes:

- Data through all tables are not consistent. For example - in case of weather table, we have measurements only from european cities. Therefore, there would be incomplete description vast majority of world's countries. 

- Along with above problem, there are many case of different names for corresponding countries. For example, we have country "Czechia" in one table, in another one the same country is listed as "Czech Republic". These issues occur across all tables and would need tidious work to be fixed. 

- Religion table contains years 2010 -> 2050. This datase might be the result of some predictive analysis. According to quick check, year 2010 seems like "closest to actual situation". Thus, I filtered the data by this year.

- Gini coefficient has zero value for many countries. Might be convienient to not include it.

- In few parts, LEFT JOINS are used. The purpose of this is to show all countries, even if they didn't have matching values across given tables. If we want not to include these incomplete entries, using inner join would serve well. Another reason for omitting these would be speeding up the queries, since using all the information started to be time consuming, due to the table size, quickly increasing, caused by joining multiple sub-tables.
