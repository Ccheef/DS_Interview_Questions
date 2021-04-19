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

#180
```
#Use lag and lead as window functions
SELECT DISTINCT sub1.Num AS 'ConsecutiveNums'
FROM
(SELECT l.Num, LAG(l.Num, 1) OVER (ORDER BY l.Id) AS 'Lag_Num', LEAD(l.Num, 1) OVER (ORDER BY l.Id) AS 'Lead_Num'
FROM Logs l) sub1
WHERE sub1.Num = sub1.Lag_Num AND sub1.Num = sub1.Lead_Num

#Use joins
SELECT DISTINCT l1.Num AS 'ConsecutiveNums'
FROM Logs l1
JOIN Logs l2 on l1.Id = l2.Id+1
JOIN Logs l3 on l1.Id = l3.Id+2 
WHERE l1.Num= l2.Num AND l2.Num= l3.Num
```

#181
```
SELECT a.Name as Employee
FROM Employee a JOIN Employee b ON a.ManagerId = b.Id
WHERE a.Salary > b.Salary
```

#182
```
SELECT DISTINCT Email 
FROM Person
GROUP BY Email
HAVING COUNT(Email) > 1
```

#183
```
SELECT c.Name as Customers 
FROM Customers c LEFT JOIN Orders o ON c.Id = o.CustomerId
WHERE o.Id IS NULL
```

#184
```
#Two solutions I wrote

SELECT t2.Department, e1.Name as Employee, e1.Salary
FROM Employee e1 JOIN 
    #subtable with department and corresponding highest salary to join back 
    (SELECT t1.Id, t1.Department, Max(t1.Salary) as Max_salary
     FROM
        (SELECT e.Salary, d.Id, d.Name as Department
         FROM Employee e JOIN Department d ON e.DepartmentId = d.Id) t1
    GROUP BY t1.Id ) t2
ON e1.DepartmentId = t2.Id and e1.Salary = t2.Max_salary

SELECT t1.Department, t1.Employee, t1.Salary #use dense rank to get duplicated max salary
FROM
    (SELECT d.Name AS Department, e.Name AS Employee,  e.Salary, 
     DENSE_RANK() OVER (Partition BY d.Id ORDER BY e.Salary DESC) AS salary_rank
    FROM Employee e JOIN Department d ON e.DepartmentId = d.Id) t1
WHERE t1.salary_rank = 1
```

#196
```
DELETE FROM Person
WHERE (Id, Email) NOT IN
(SELECT Id, Email from 
 (SELECT MIN(Id) AS Id, Email
FROM Person 
GROUP BY Email) p
)
```
