select 
el.leave_id,
el.leave_applied_on,
e.employee_name,
ed.name,
el.leave_status,
el.from_date, el.to_date, el.leave_type, e.branch_id
from 
tbl_emp_leaves el
join tbl_employees e on el.emp_id = e.employee_id and el.emp_branch_id = 1
join tbl_designations ed on el.emp_designation = ed.id and el.emp_designation = 1;
