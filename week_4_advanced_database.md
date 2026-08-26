LAB 1: INSPECTING TABLE SIZE
Check table vs index size
The index-heavy tables are the tables whose index size is relatively large compared to their data size: payment, customer

LAB 2: THE IMPACT OF A NEW INDEX
1: Current size of payment indexes
Before creating the new index: 920 kB
2: Create a heavy index on payment_date
Index created successfully.
3: Check size again
After creating the new index: 1488 kB
-> The new index consumed 71 pages, where each PostgreSQL page is 8 KB. 

LAB 3: PARTIAL INDEX PRACTICE
Partial index created successfully.
Index size: 16kB
Number of films with replacement_cost > 25: 236
Total number of films: 1000

Comparison:
The partial index is smaller than a full index because it only contains rows where replacement_cost > 25.
-> A partial index saves storage space and is useful when queries frequently access only a specific subset of rows.