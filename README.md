# something

#DDl
```sql

use LojaF;
GO

CREATE TABLE Distritos (
DistritoID INT PRIMARY KEY IDENTITY(1, 1)NOT NULL, 
DistritoNome NVARCHAR (50) NOT NULL,
);

CREATE TABLE Concelhos (
ConcelhoID INT PRIMARY KEY IDENTITY(1, 1)NOT NULL,
ConcelhoNome NVARCHAR (50) NOT NULL,
DistritoID INT NOT NULL, 
FOREIGN KEY (DistritoID) REFERENCES Distritos (DistritoID));

CREATE TABLE Freguesias (
FreguesiaID INT PRIMARY KEY IDENTITY(1, 1)NOT NULL,
FreguesiaNome NVARCHAR (50) NOT NULL,
ConcelhoID INT NOT NULL, 
FOREIGN KEY (ConcelhoID) REFERENCES Concelhos (ConcelhoID));

```

#DML
