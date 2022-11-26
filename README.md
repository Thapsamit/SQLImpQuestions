# SQLImpQuestions

## Q - 1 Difference between truncate and delete?

| Delete | Truncate |
| ------ | -------- |
| The DELETE statement is used when we want to remove some or all of the records from the table | while the TRUNCATE statement will delete entire rows from a table. |
| DML Command| DDL Command | 
| Allows where clause | Doesn't allow where clause |
| Slower | Faster |
| The DELETE statement removes rows one at a time and records an entry in the transaction log for each deleted row. | TRUNCATE TABLE removes the data by deallocating the data pages used to store the table data and records only the page deallocations in the transaction log. |
| DELETE activates all delete triggers on the table to fire. | no triggers are fired on the truncate operation because it does not operate on individual rows. |
| it acquires the lock on every deleted row. | TRUNCATE acquires the lock on the data page before deleting the data page; thus, it requires fewer locks and few resources. |


# Q - 2 What is MySQL Collatio?
- A MySQL collation is a well-defined set of rules which are used to compare characters of a particular character-set by using their corresponding encoding.
- Each character set in MySQL might have more than one collation, and has, at least, one default collation. Two character sets cannot have the same collation.
- Suppose, we have some alphabet with A,B,C,D,a,b,c,d. We assigned a number to all letters like A=1,B=2,C=3,D=4,a=5,b=6,c=7,d=8. So, for symbol A encoding is 1, for B encoding is 2, for C encoding is 3, and so on. If we want to compare string A, B, a, b. We have an easier method to do this, just a moment ago we have assigned a distinct value to some alphabets like encoding of A is 1, for B it is 2 similarly encoding for a and b is 5 and 6. So, how we have able to perform this comparison, just because of Collation. We explicitly apply the technique of Collation(Compare there corresponding encoding) to our Character-set.
- If you want the client program to communicate with the server using a Character-set different from the default, you’ll need to highlight which one of the character set you are using. For example, to use the utf8 Unicode character set, use this statement after  establishing connecting to the server


# Q - 3 Three different parameters in Stored Procedures?
- IN: 
 - This is the Default Parameter for the procedure. It always receives the values from calling program.
- OUT: 
 - This parameter always sends the values to the calling program.
- IN OUT:
 - This parameter performs both the operations. It Receives value from as well as sends the values to the calling program.
 
# Q - 4 What is the need for a MERGE statement?
- The MERGE command in SQL is actually a combination of three SQL statements: INSERT, UPDATE and DELETE. In simple words, the MERGE statement in SQL provides a convenient way to perform all these three operations together which can be very helpful when it comes to handling large running databases. But unlike INSERT, UPDATE and DELETE statements MERGE statement requires a source table to perform these operations on the required table which is called a target table.
- When will you need to insert the data in the target table?
  - Obviously when there is data in source table and not in target table i.e when data not matched with target table.
- When will you need to update the data?
  - When the data in source table is matched with target table but any entry other than the primary key is not matched.
- When will you need to delete the data?
  - When there is data in target table and not in source table i.e when data not matched with source table.
 
 
 # Q - 5 What are the advantages of PL/SQL functions?
 - We can make a single call to the database to run a block of statements. Thus, it improves the performance against running SQL multiple times.
 - We can divide the overall work into small modules which becomes quite manageable, also enhancing the readability of the code.
 - It is secure since the code stays inside the database, thus hiding internal database details from the application(user).
 
 
 
 # Q - 6 What are Nested Triggers?
 - A trigger can also contain INSERT, UPDATE, and DELETE logic within itself, so when the trigger is fired because of data modification it can also cause another data modification, thereby firing another trigger. A trigger that contains data modification logic within itself is called a nested trigger.
 
 
 # Q - 7 What is SQL injection?
 - SQL injection is a technique used to exploit user data through web page inputs by injecting SQL commands as statements. Basically, these statements can be used to manipulate the application’s web server by malicious users.
 
 
 # Q - 8 How do we avoid getting duplicate entries in a query without using the distinct keyword?
 - Using group by 
 - using self-join
 - Remove duplicates using row numbers.
 
 
 
 
 
 
 
