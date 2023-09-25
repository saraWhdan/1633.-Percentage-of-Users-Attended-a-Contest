# 1633. Percentage of Users Attended a Contest
 ### Problem Description : [Percentage of Users Attended a Contest](https://leetcode.com/problems/percentage-of-users-attended-a-contest/description/?envType=study-plan-v2&envId=top-sql-50)

 ### Solution
 ```sql
/* Write your T-SQL query statement below */
select contest_id ,Round((count(distinct user_id)*100.0/(SELECT COUNT(*) FROM users)),2) percentage
from register
Group by contest_id
order by percentage desc,contest_id asc

