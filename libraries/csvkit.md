# CSVKit

## CSVSQL

**Description:** Generate SQL statements for a CSV file or execute those statements directly on a database.

**Documentation:** [ReadTheDocs](http://csvkit.readthedocs.io/en/0.9.1/scripts/csvsql.html)

### Creating a Table DDL

```shell
csvsql -d , -q \" --dialect mysql --table table_name --insert ~/file.csv
```
The DDL won't be perfect, things to look at are:
- decimal parameters
- keys/indexes

Run the DDL on the host and then you are ready to load the data

### Loading the Data

```shell
csvsql -d , -q \" --db mysql://user:password@host:3306/database --no-create --table table_name --insert ~/file.csv
```
