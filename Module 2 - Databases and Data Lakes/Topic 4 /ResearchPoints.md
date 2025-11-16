## Research Points 

In your learning journal, research the third-party database monitoring solutions that your company uses.

<b>New terms </b>

### Sharing / Horizontal Partitioning

Definition:<br>
Horizontal partitioning (also called sharding) means splitting a database table into multiple smaller tables, where each smaller table (or shard) contains different rows of the original table.
“Horizontal” = splitting by rows, not columns.

<br>
<img width="642" height="434" alt="image" src="https://github.com/user-attachments/assets/f9df807c-0235-49c5-879c-b806c71c82d2" />
<br>

### Caching

Caching is a technique where frequently accessed data is stored in fast memory (cache) so the system doesn’t have to repeatedly fetch it from the slower database or disk.
<br>
Why do it?
- Improves performance
- Reduces load on the database
- Reduces I/O operations (disk reads)

<br>
MSSQL doesn’t require you to implement an external cache for basic queries — it already has built-in caching mechanisms. But you can also use application-level caching for extra performance.

### How can i use MSSQL for caching?

<img width="704" height="424" alt="image" src="https://github.com/user-attachments/assets/fd217e9e-352c-491f-ab71-ec744b7b5065" />
<br>
<br>
<b>Indexed Views for Caching Queries in SQL Server</b>
<br>
<br>
<img width="732" height="466" alt="image" src="https://github.com/user-attachments/assets/93c1f704-c072-4a6d-b234-43b1c49c2d02" />
