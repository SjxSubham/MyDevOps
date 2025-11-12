```sql

sudo systemctl status mysql
sudo systemctl start mysql
mysql -u root -p
sudo systemctl stop mysql

```

select user from mysql.user;

DQL 
DB -> Table

select now() -> server time;    

select * from worker where salary between 8000 and 20000;
select * from worker where department = 'HR' or department = 'Admin';

-- between In
select * from worker where department in ('hr', 'admin') -> we have reduces all or into single or;

-- not
select * from wroker where department not('admin');

--wildcard
'%p%'
select * from worker where first_name like '%p%;

## Sorting
-- assending
select * from worker order by salary;

-- decending
select * from worker order by salary desc;

## Disctincnt
select distinct department from worker;

-- Aggregation
select department, count(department) from worker group by department;

### avg
 - find avg. salary every department..??
>> -> select department , avg(salary) from worker group by department;
#### min
 - find min. salary from every department..??
 -> select department, min(salary) from worker group by department;
#### max
- find max salary from every department..??
-> select department, max(salary) from worker group by department;



>> -> select department, min(salary) from wroker group by department;
find number of employes in differnt department/coloumn ??
-- 
