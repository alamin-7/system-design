
# Indexing

indexing: A way to access elements in a data structure.

How Indexing Works: Use B-tree index, hash index, or full-text index to speed up data retrieval.

# Benefits of Indexing:

i. Faster data retrieval: Indexing allows the database to quickly locate data, reducing the time it takes.

ii. Improved query performance: Indexing can improve the performance of queries by allowing the database to quickly locate the data needed.

iii. Speeding Up JOIN Operations: Indexes on foreign keys or columns used in joins can significantly speed up join operations.

# Downsides of Indexing:

i. Increased storage requirements: Indexes require additional storage space, which can increase the size of the database. 

ii. Increased maintenance: Indexes require regular maintenance to ensure they remain effective.

iii. Slower Write Operations: delete, update, insert.

When to Use Indexing:

i. Frequent Searches: If you frequently search or filter data using a particular column, an index on that column can speed up queries.

# Create an index:

CREATE INDEX index_name ON table_name (column_name);

# B-tree indexing:

i. use indexing in a column which has the most unique values.

ii. B-Tree indexing is effective for high-cardinality columns.(id, email, phone) (unique) Because if the tree has duplicate 
    value then the search will take time. (Select * from table where sex="male") this will take time because there are many male in the table.

iii. Composite indexes must follow left-to-right order. INDEX (A, B) works for A but not just B.
 
# When not to use B-Tree indexing

i. For full-text search → Use GIN or TSVECTOR indexing. why - 

ii. For JSON fields → Use GIN indexing for JSONB data.

iii. For random lookups (e.g., UUID) → Hash indexes might be better.

# How can you optimize indexing in a write-heavy system?

Use fewer indexes (each index slows down writes).
Use partial indexes (index only necessary rows).
Use index maintenance strategies (rebuild/reindex periodically).

# partial indexing

CREATE INDEX idx_active_users
ON users (username)
WHERE status = 'active';
