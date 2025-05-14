
## SQL

[PostgreSQL-cheat-sheet](https://sp.postgresqltutorial.com/wp-content/uploads/2018/03/PostgreSQL-Cheat-Sheet.pdf)

# Some of The Most Important SQL Commands

**SELECT** - *extracts data from a database*

**UPDATE** - *updates data in a database*

**DELETE** - *deletes data from a database*

**INSERT INTO** - *inserts new data into a database*

**CREATE DATABASE**- *creates a new database*

**ALTER DATABASE** - *modifies a database*

**CREATE TABLE**- *creates a new table*

**ALTER TABLE** - *modifies a table*

**DROP TABLE** - *deletes a table*

**CREATE INDEX** - *creates an index (search key)*

**DROP INDEX** - *deletes an index*

**JOIN** - *combine records from two or more tables in a database*

Link to the Demo-Database where you can practice SQL-Commands: https://www.w3schools.com/sql/sql_select.asp


# Connect to your database with psql or PgAdmin. Run the following SQL. You only need to install the features you want:

-- Enable PostGIS (as of 3.0 contains just geometry/geography)

CREATE EXTENSION postgis;

-- enable raster support (for 3+)

CREATE EXTENSION postgis_raster;

-- Enable Topology

CREATE EXTENSION postgis_topology;

-- Enable PostGIS Advanced 3D

-- and other geoprocessing algorithms

-- sfcgal not available with all distributions

CREATE EXTENSION postgis_sfcgal;

-- fuzzy matching needed for Tiger

CREATE EXTENSION fuzzystrmatch;

-- rule based standardizer

CREATE EXTENSION address_standardizer;

-- example rule data set
CREATE EXTENSION address_standardizer_data_us;

-- Enable US Tiger Geocoder

CREATE EXTENSION postgis_tiger_geocoder;