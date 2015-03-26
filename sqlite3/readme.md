## SQLite3 Cheat Sheet

#### Create a New Table
```
CREATE TABLE table_name(
  column_name1 column_type1,
  colmnn_name2 column_type2,
  colmnn_name3 column_type3
);
```
```
CREATE TABLE people(
  id int PRIMARY KEY NOT NULL,
  first_name text NOT NULL,
  last_name text
);
```

#### Insert a Record
```
INSERT INTO table_name (column_name1, column_name2, column_name3) VALUES ("value1", "value2", "value3");
```
```
INSERT INTO people (id, first_name, last_name) VALUES (9, "Josh", "Campoverde");
```

#### Find a Record
```
SELECT * FROM table_name WHERE id = 9;
```

#### Add a Column to a Table
```
ALTER table_name ADD new_column_name new_column_type;
```
```
ALTER people ADD nickname text;
```

#### Update a Record
```
UPDATE _table_name_ SET _column_name_ = "_column_value_" WHERE column_name = column_value;
```
```
UPDATE people SET first_name = "Joshua" WHERE id = 9;
```
```
UPDATE _table_name_ SET _column_name_ = "_column_value_", _column_name2_ = "_column_value2_" WHERE column_name = column_value;
```
```
UPDATE people SET first_name = "Josh", nickname = "campo" WHERE id = 9;
```

#### Delete All Records from a Table
```
DELETE FROM table_name;
```
```
DELETE FROM people;
```

#### Delete Specific Records from a Table
```
DELETE FROM table_name WHERE column_name = column_value;
```
```
DELETE FROM people WHERE id = 9;
```
