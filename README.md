# Subsetter
## Architecture
Leverages the power of diesel.rs to make it compatible with PostgreSQL, MySQL and more.

## Algorithm
1. Collect a data tree structure of all table relationships in the database
2. Go through each tree.
    * Tables that occur multiple times in the data tree(s) will have their rows matched against the previously collected ones. This way, the algorithm will not get stuck in an endlessly repetitive process of collecting previous rows.
3. Persist to a .sql file or to another database.
