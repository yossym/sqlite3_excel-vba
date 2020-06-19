readme.txt
==========

sample database
---------------
SQLite Sample Database And Its Diagram (in PDF format)
https://www.sqlitetutorial.net/sqlite-sample-database/

sqlite3 library for excel vba
------------------------------
Releases  govert/SQLiteForExcel  GitHub
https://github.com/govert/SQLiteForExcel/releases


sample database summary
-------------------------
>sqlite3 chinook.db
SQLite version 3.32.2 2020-06-04 12:58:43
Enter ".help" for usage hints.
sqlite>
.table
albums          employees       invoices        playlists
artists         genres          media_types     tracks
customers       invoice_items   playlist_track
sqlite> .schema employees
CREATE TABLE IF NOT EXISTS "employees"
(
    [EmployeeId] INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,
    [LastName] NVARCHAR(20)  NOT NULL,
    [FirstName] NVARCHAR(20)  NOT NULL,
    [Title] NVARCHAR(30),
    [ReportsTo] INTEGER,
    [BirthDate] DATETIME,
    [HireDate] DATETIME,
    [Address] NVARCHAR(70),
    [City] NVARCHAR(40),
    [State] NVARCHAR(40),
    [Country] NVARCHAR(40),
    [PostalCode] NVARCHAR(10),
    [Phone] NVARCHAR(24),
    [Fax] NVARCHAR(24),
    [Email] NVARCHAR(60),
    FOREIGN KEY ([ReportsTo]) REFERENCES "employees" ([EmployeeId])
                ON DELETE NO ACTION ON UPDATE NO ACTION
);
CREATE INDEX [IFK_EmployeeReportsTo] ON "employees" ([ReportsTo]);
sqlite> .exit

