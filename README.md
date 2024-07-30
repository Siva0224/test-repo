
DROP TABLE IF EXISTS `tbl_activity`;
CREATE TABLE tbl_activity (
    activity_id INT auto_increment PRIMARY KEY,
    activity_name VARCHAR(30),
    type ENUM(`c`, `d` , `u`),
    activity_created_by VARCHAR(30),
    created_at VARCHAR(30),
    user_branch_id INT,
)
