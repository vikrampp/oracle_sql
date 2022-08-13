##Can be used for https://livesql.oracle.com/

drop table employee;
CREATE TABLE employee (
    emp_id              NUMBER(4)      NOT NULL,
    ename       		VARCHAR2(20),
    job					VARCHAR2(9),
    mgr_id              NUMBER(4),
    salary              NUMBER(7,2),
    dept_id             NUMBER(2)
);

drop table department;
CREATE TABLE department (
    dept_id             NUMBER(2)      NOT NULL,
    dept_name           VARCHAR2(20),
    location_id			VARCHAR2(15)
);

INSERT INTO department (dept_id, dept_name, location_id) VALUES(10, 'ACCOUNTING', 'NEW YORK');
INSERT INTO department (dept_id, dept_name, location_id) VALUES(20, 'RESEARCH', 'DALLAS');
INSERT INTO department (dept_id, dept_name, location_id) VALUES(30, 'SALES', 'CHICAGO');
INSERT INTO department (dept_id, dept_name, location_id) VALUES(40, 'OPERATIONS', 'BOSTON');
COMMIT;

INSERT INTO employee VALUES (7839, 'KING', 'PRESIDENT', NULL, 5000, 10);
INSERT INTO employee VALUES (7698, 'BLAKE', 'MANAGER', 7839, 2850, 30 );
INSERT INTO employee VALUES (7782, 'CLARK', 'MANAGER', 7839, 2450, 10);
INSERT INTO employee VALUES (7566, 'JONES', 'MANAGER', 7839, 2975, 20);
INSERT INTO employee VALUES (7788, 'SCOTT', 'ANALYST', 7566, 3000, 20);
INSERT INTO employee VALUES (7902, 'FORD', 'ANALYST', 7566,3000, 20);
INSERT INTO employee VALUES (7369, 'SMITH', 'CLERK', 7902, 800, 20);
INSERT INTO employee VALUES (7499, 'ALLEN', 'SALESMAN', 7698, 1600, 30);
INSERT INTO employee VALUES (7521, 'WARD', 'SALESMAN', 7698, 1250, 30);
INSERT INTO employee VALUES (7654, 'MARTIN', 'SALESMAN', 7698, 1250, 30);
INSERT INTO employee VALUES (7844, 'TURNER', 'SALESMAN', 7698, 1500, 30);
INSERT INTO employee VALUES (7876, 'ADAMS', 'CLERK', 7788, 1100, 20);
INSERT INTO employee VALUES (7900, 'JAMES', 'CLERK', 7698, 950, 30);
INSERT INTO employee VALUES (7934, 'MILLER', 'CLERK', 7782, 1300, 10);
COMMIT;
