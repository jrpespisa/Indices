Commands written to execute queries
​
For:
​
* Find all rows that have an ingredient `name` of `Brussels sprouts`.
​
SELECT *
FROM ingredients
WHERE ingredients.name = 'Brussels sprouts';
​
* Calculate the total count of rows of ingredients with a `name` of `Brussels sprouts`.
​
SELECT COUNT (*)
FROM ingredients WHERE                                                                                                                                                             ingredients.name = 'Brussels sprouts';
​
* Find all `Brussels sprouts` ingredients having a unit type of `gallon(s)`.
​
SELECT (name, unit)
FROM ingredients
WHERE name
LIKE '%Brussels sprouts%' AND unit LIKE '%gallon%';
​
* Find all rows that have a unit type of `gallon(s)`, a name of `Brussels sprouts` or has the letter `j` in it.
​
SELECT *
FROM ingredients
WHERE name LIKE '%Brussels sprouts%' OR name LIKE '%j%'
AND unit LIKE '%gallon%';
​

* Command for creating the index:

CREATE INDEX ON ingredients(name);

​
Screenshots for indexed queries:
​
Link to query for #1
http://imgur.com/ZDkM5Nm
​
Link to query for #2, #3, #4
http://imgur.com/a/oSahv
