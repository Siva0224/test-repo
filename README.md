
DROP TABLE IF EXISTS `tbl_activity`;
CREATE TABLE tbl_activity (
    activity_id INT auto_increment PRIMARY KEY,
    activity_name VARCHAR(30),
    type ENUM(`c`, `d` , `u`),
    activity_created_by VARCHAR(30),
    created_at VARCHAR(30),
    user_branch_id INT,
)

DROP TABLE IF EXISTS `tbl_notification`;
CREATE TABLE tbl_notification (
    notification_id INT AUTO_INCREMENT PRIMARY KEY,
    notification_name VARCHAR(30),
    notification_created_date VARCHAR(30),
    user_branch_id INT
)

DROP TABLE IF EXISTS `tbl_emp_leaves`;
CREATE TABLE tbl_emp_leaves(
    leave_id INT AUTO_INCREMENT PRIMARY KEY,
    emp_id INT,
    emp_designation INT,
    leave_applied_on VARCHAR(30),
    leave_status ENUM(`pending`, `approved`, `rejected`),
    from_date VARCHAR(30),
    to_date VARCHAR(30),
    shift_id INT,
    leave_type ENUM(`sick leave`,`casual leave`),
    emp_branch_id INT,
    FOREIGN KEY (emp_id) REFERENCES(tbl_employees),
    FOREIGN KEY (id) REFERENCES(tbl_designations)
)
