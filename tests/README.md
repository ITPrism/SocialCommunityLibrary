Unit Testing Information
====================

This document provides additional information on the folder structure within the unit tests and some basic information about the test suite

Folder Structure
---------------------
* `schema` - This folder contains all SQL schema for setting up the environment for tests using `TestCaseDatabase`.  The `ddl.sql` file is used by `TestCaseDatabase` to create a SQLite in-memory database which is destroyed at the end of the test cycle.  The other SQL files are specific to each database vendor and require you to manually create the databases.
* `stubs` - Contains miscellaneous test data used throughout the suite.
    * `database` - CSV files loaded by various tests to populate the database with test data
* `suites` - The actual test classes
* `tmp` - A temporary directory used for filesystem operations in the test suite
* `bootstrap.php` - The testing bootstrap called when PHPUnit is run
