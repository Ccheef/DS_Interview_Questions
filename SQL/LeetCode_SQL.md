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

#177
```
#USE dense_rank to rank the duplicated salary as the same rank and distinct to only select one duplicated salary
CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
BEGIN
  RETURN (
      Select DISTINCT sub1.Salary
      FROM
          (SELECT e.Salary, DENSE_RANK() over (order by e.Salary DESC) as 'Rank'
           FROM Employee e
           ) sub1
      WHERE sub1.rank = N
      
  );
END
```
#178
```
#use dense_rank to rank score in consecutive order
SELECT s.Score, DENSE_RANK() over (ORDER BY s.Score DESC) as 'Rank'
FROM Scores s
```
