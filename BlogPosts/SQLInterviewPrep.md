## SQL Interview Prep With SQLite

Here's solutions to some practice SQL interview questions (courtesy of wikibooks):

Let's create our Relational Schema by creating tables Manufacturers and Products:

```SQL
INSERT INTO Manufacturers(Code, Name) VALUES(1, 'SONY');
INSERT INTO Manufacturers(Code, Name) VALUES(2, 'Creative Labs');
INSERT INTO Manufacturers(Code, Name) VALUES(3, 'Hewlett-Packard');
INSERT INTO Manufacturers(Code, Name) VALUES(4, 'Iomega');
INSERT INTO Manufacturers(Code, Name) VALUES(5, 'Fujitsu');
INSERT INTO Manufacturers(Code, Name) VALUES(6, 'Winchester');

INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(1, 'Hard Drive', 240, 5);
INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(2, 'Memory', 120, 6);
INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(3, 'ZIP Drive', 150, 4);
INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(4, 'Floppy Disk ', 5, 6);
INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(5, 'Monitor', 240, 1);
INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(6, 'DVD Drive', 90, 2);
INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(7, 'CD Drive', 90, 2);
INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(8, 'Printer', 270, 3);
INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(9, 'Toner Cartridge', 66, 3);
INSERT INTO Products(Code, Name, Price, Manufacturer)  VALUES(10, 'DVD Burner', 180, 2);
```

Now that we've created our schema, lets get started with the questions.

---
1. Select the names of all the products in the store.

  Solution:
```SQL
SELECT Name FROM Products;
```
2. Select the names and the prices of all      the products in the store.

  Solution:
```SQL
SELECT Name, Price FROM Products;
```
3. Select the name of the products with a   
   price less than or equal to $200.

   Solution:
```SQL
SELECT Name From Products
Where Price <= 200
```
4. Select all the products with a price between $60 and $120.

  Solution:
```SQL
SELECT * From Products
Where Price > 60 AND Price < 120;
```
5. Select the name and price in cents (i.e., the price must be multiplied by 100).

  Solution:
  ```SQL
  SELECT Name, Price * 100 AS PriceCents FROM Products;
  ```
6. Compute the average of all the products.

    Solution:
    ```SQL
    SELECT avg(Price) FROM Products;
    ```
7. Compute the average price of all products with manufacturer code is equal to 2.

    Solution:
    ```SQL
    SELECT avg(Price) FROM Products
    WHERE Manufacturer = 2;
    ```
8. Compute the number of products with a price larger than or equal to $180.

    Solution:
    ```SQL
    SELECT COUNT(*) FROM Products WHERE Price >= 180; 
    ```
