# 第N高的薪水

## mysql实现

```
CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
BEGIN
  SET N = N - 1;
  RETURN (
      # Write your MySQL query statement below.
	  select distinct Salary from Employee order by Salary DESC limit N, 1
  );
END
```
