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

INSERT INTO Products(Code, Name, Price, Manufacturer) VALUES(1, 'Hard Drive', 240, 5);
INSERT INTO Products(Code, Name, Price, Manufacturer) VALUES(2, 'Creative Labs');
INSERT INTO Products(Code, Name) VALUES(3, 'Hewlett-Packard');
INSERT INTO Products(Code, Name) VALUES(4, 'Iomega');
INSERT INTO Products(Code, Name) VALUES(5, 'Fujitsu');
INSERT INTO Products(Code, Name) VALUES(6, 'Winchester');
INSERT INTO Products(Code, Name) VALUES(3, 'Hewlett-Packard');
INSERT INTO Products(Code, Name) VALUES(4, 'Iomega');
INSERT INTO Products(Code, Name) VALUES(5, 'Fujitsu');
INSERT INTO Products(Code, Name) VALUES(6, 'Winchester');
```
