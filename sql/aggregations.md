# Aggregations

## Aggregation Functions
Perform computations on sets of values on multiple rows of the relation. Examples: MIN, MAX, SUM, AVG, COUNT

## GROUP BY Clause 
Allow us to partition our relation into groups in which we apply the aggregation functions. Only used in conjunction with aggregations
    - If you select column x and group by column y, but column x is not unique in every group, if you are in postgres this throws an error, but if you are in mysql or sqlite the result in column x will be a random value

## HAVING Clause
Allows us to filter (apply conditions to) aggregation results
- GROUP BY and HAVING can be used together