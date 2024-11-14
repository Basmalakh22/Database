# Functions

- In SQL Server, a scalar function is one which returns a `single value`, be that a string of text, a number, or a date.  There are many built-in functions in SQL Server.

```sql
SELECT
--The length of the film name
LEN(FilmName)

--Replaces NULL with custom value
,ISNULL(FilmName, 'No title entered')

--The weekday of the date
,DATENAME(DW,FilmReleaseDate)

--Date in UK format
,CONVERT(CHAR(10),FilmReleaseDate,103)

--Converts one data type into another
,CAST(FilmRunTimeMinutes AS DECIMAL)/60
FROM tblFilm
```

```sql
SELECT FilmName,FilmReleaseDate
DATENAME(DW,FilmReleaseDate) + ' ' +
DATENAME(D,FilmReleaseDate) + ' ' +
DATENAME(M,FilmReleaseDate) + ' ' +
DATENAME(YY,FilmReleaseDate)

FROM tblFilm
```

- [SQL Server Programming Part 7 - User Defined Functions](https://youtu.be/6BslHItOTjU?si=ngmfFDMU_HJI58bT)
