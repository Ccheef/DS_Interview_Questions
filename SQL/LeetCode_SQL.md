#175
```
SELECT p.FirstName, p.LastName, a.City, a.State 
FROM Person p LEFT JOIN Address a on p.PersonId = a.PersonId;
```

#176
```
#use double max to compare and get null if no second largest value exists
SELECT MAX(salary) AS secondhighestsalary
FROM employee
WHERE salary < (SELECT MAX(salary) FROM employee);
```
