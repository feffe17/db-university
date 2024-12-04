	#	Time	Action	Message	Duration / Fetch
0	1	14:06:47	USE db-university	Error Code: 1064. You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '-university' at line 1	0.000 sec
3	2	14:07:16	USE `db-university`	0 row(s) affected	0.000 sec
0	3	14:08:29	USE `db-university`
 SOURCE `C:\Users\fpmas\Desktop\DBS\1\db.sql;`	Error Code: 1064. You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'SOURCE `C:\Users\fpmas\Desktop\DBS\1\db.sql;`' at line 2	0.000 sec
0	4	14:08:46	USE `db-university`
 SOURCE C:\Users\fpmas\Desktop\DBS\1\db.sql	Error Code: 1064. You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'SOURCE C:\Users\fpmas\Desktop\DBS\1\db.sql' at line 2	0.000 sec
0	5	14:18:48	USE `db-university`
 SHOW DATABASES	Error Code: 1064. You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'SHOW DATABASES' at line 2	0.000 sec
0	6	14:18:56	USE `db-university`
 SHOW DATABASES	Error Code: 1064. You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'SHOW DATABASES' at line 2	0.000 sec
3	7	14:19:14	SHOW DATABASES	8 row(s) returned	0.000 sec / 0.000 sec
0	8	14:20:23	SOURCE `C:\Users\fpmas\Desktop\DBS\1\db.sql`	Error Code: 1064. You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'SOURCE `C:\Users\fpmas\Desktop\DBS\1\db.sql`' at line 1	0.000 sec
3	9	14:23:12	DROP DATABASE `db-university`	0 row(s) affected	0.016 sec
3	10	14:25:05	CREATE DATABASE university	1 row(s) affected	0.031 sec
3	11	14:37:21	DROP DATABASE university	8 row(s) affected	0.187 sec
3	12	14:37:35	CREATE DATABASE university	1 row(s) affected	0.015 sec
3	13	14:38:10	USE university	0 row(s) affected	0.000 sec
3	14	14:43:32	SELECT *
 FROM `students`
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
0	15	14:46:19	SELECT *
 FROM `students`
 WHERE `date_of_birth` = "1990"
 LIMIT 0, 1000	Error Code: 1525. Incorrect DATE value: '1990'	0.000 sec
3	16	14:46:42	SELECT *
 FROM `students`
 #WHERE `date_of_birth` = "1990"
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
3	17	14:49:18	SELECT *
 FROM `students`
 WHERE `date_of_birth` = "1990-01-30"
 LIMIT 0, 1000	2 row(s) returned	0.015 sec / 0.000 sec
0	18	14:49:32	SELECT *
 FROM `students`
 WHERE `date_of_birth` = "1990-*-*"
 LIMIT 0, 1000	Error Code: 1525. Incorrect DATE value: '1990-*-*'	0.000 sec
3	19	14:50:07	SELECT *
 FROM `students`
 WHERE `date_of_birth` = "1990-01-30"
 LIMIT 0, 1000	2 row(s) returned	0.000 sec / 0.000 sec
3	20	14:51:32	SELECT *
 FROM `students`
 WHERE year(`date_of_birth`) = "1990"
 LIMIT 0, 1000	160 row(s) returned	0.000 sec / 0.000 sec
3	21	14:52:52	SELECT *
 FROM `COURSES`
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
3	22	14:53:54	SELECT *
 FROM `COURSES`
 WHERE `cfu` > 10
 LIMIT 0, 1000	479 row(s) returned	0.015 sec / 0.000 sec
0	23	14:54:51	SELECT *
 FROM `STUDENTS`
 WHERE `age` > 30
 LIMIT 0, 1000	Error Code: 1054. Unknown column 'age' in 'where clause'	0.000 sec
3	24	14:55:06	SELECT *
 FROM `STUDENTS`
 #WHERE `age` > 30
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
3	25	14:57:11	SELECT *
 FROM `STUDENTS`
 WHERE 2024 - year(`date_of_birth`) >= 30
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
3	26	14:58:28	SELECT *
 FROM `STUDENTS`
 #WHERE 2024 - year(`date_of_birth`) >= 30
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
3	27	14:59:25	SELECT *
 FROM `STUDENTS`
 WHERE 2024 - year(`date_of_birth`) >= 30
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
3	28	15:00:05	SELECT *
 FROM `COURSES`
 #WHERE 2024 - year(`date_of_birth`) >= 30
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.015 sec
3	29	15:01:57	SELECT *
 FROM `COURSES`
 WHERE `year` = 1
 AND `period` = "I semestre"
 LIMIT 0, 1000	286 row(s) returned	0.000 sec / 0.000 sec
3	30	15:02:48	SELECT *
 FROM `EXAMS`
 LIMIT 0, 1000	1000 row(s) returned	0.015 sec / 0.000 sec
3	31	15:05:58	SELECT *
 FROM `EXAMS`
 WHERE `date` = "2020-06-20"
 AND hour(`hour`) >= 14
 LIMIT 0, 1000	21 row(s) returned	0.000 sec / 0.000 sec
3	32	15:06:51	SELECT *
 FROM `courses`
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
3	33	15:07:16	SELECT *
 FROM `degrees`
 LIMIT 0, 1000	75 row(s) returned	0.016 sec / 0.000 sec
3	34	15:07:42	SELECT *
 FROM `degrees`
 WHERE `level` = "magistrale"
 LIMIT 0, 1000	38 row(s) returned	0.016 sec / 0.000 sec
3	35	15:10:22	SELECT *
 FROM `departments`
 LIMIT 0, 1000	12 row(s) returned	0.016 sec / 0.000 sec
3	36	15:10:41	SELECT *
 FROM `teachers`
 LIMIT 0, 1000	100 row(s) returned	0.016 sec / 0.000 sec
3	37	15:11:18	SELECT *
 FROM `teachers`
 WHERE `phone` = null
 LIMIT 0, 1000	0 row(s) returned	0.015 sec / 0.000 sec
3	38	15:11:29	SELECT *
 FROM `teachers`
 #WHERE `phone` = null
 LIMIT 0, 1000	100 row(s) returned	0.000 sec / 0.000 sec
3	39	15:12:11	SELECT *
 FROM `teachers`
 WHERE `phone` = NULL
 LIMIT 0, 1000	0 row(s) returned	0.000 sec / 0.000 sec
3	40	15:12:49	SELECT *
 FROM `teachers`
 WHERE `phone` IS NULL
 LIMIT 0, 1000	50 row(s) returned	0.015 sec / 0.000 sec
3	41	15:13:22	SELECT * FROM university.students
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
3	42	15:21:24	SELECT *
 FROM `students`
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec
0	43	15:27:57	INSERT INTO `students` (`name`, `sourname`, `date_of_birth`, `email`, `fiscal_code`, `degree_id`, `enrolment_date`, `registration_number`)
 VALUES ('Federico', 'Di Murro', '2000-02-17', 'fpm.asd@gmail.com', 'DMRFRC00B17H501D', 64, "2024-08-20", "9999999")	Error Code: 1054. Unknown column 'sourname' in 'field list'	0.000 sec
3	44	15:28:19	INSERT INTO `students` (`name`, `surname`, `date_of_birth`, `email`, `fiscal_code`, `degree_id`, `enrolment_date`, `registration_number`)
 VALUES ('Federico', 'Di Murro', '2000-02-17', 'fpm.asd@gmail.com', 'DMRFRC00B17H501D', 64, "2024-08-20", "9999999")	1 row(s) affected	0.063 sec
0	45	15:31:47	SELECT `TEACHERS`
 LIMIT 0, 1000	Error Code: 1054. Unknown column 'TEACHERS' in 'field list'	0.000 sec
0	46	15:32:01	SELECT `teachers`
 LIMIT 0, 1000	Error Code: 1054. Unknown column 'teachers' in 'field list'	0.000 sec
3	47	15:33:01	SELECT *
 FROM `teachers`
 LIMIT 0, 1000	100 row(s) returned	0.000 sec / 0.000 sec
0	48	15:33:44	UPDATE `teachers`
 SET `office_number` = 126
 WHERE `first_name` = 'Pietro' AND `last_name` = 'Rizzo'	Error Code: 1054. Unknown column 'first_name' in 'where clause'	0.000 sec
0	49	15:34:14	UPDATE `teachers`
 SET `office_number` = 126
 WHERE `name` = 'Pietro' AND `surname` = 'Rizzo'	Error Code: 1175. You are using safe update mode and you tried to update a table without a WHERE that uses a KEY column. 
 To disable safe mode, toggle the option in Preferences -> SQL Editor and reconnect.	0.000 sec
0	50	15:36:05	UPDATE `teachers`
 SET `office_number` = 126
 WHERE `name` = 'Pietro' AND `surname` = 'Rizzo'	Error Code: 1175. You are using safe update mode and you tried to update a table without a WHERE that uses a KEY column. 
 To disable safe mode, toggle the option in Preferences -> SQL Editor and reconnect.	0.000 sec
3	51	15:36:38	SET SQL_SAFE_UPDATES = 0	0 row(s) affected	0.000 sec
3	52	15:36:46	UPDATE `teachers`
 SET `office_number` = 126
 WHERE `name` = 'Pietro' AND `surname` = 'Rizzo'	1 row(s) affected
 Rows matched: 1  Changed: 1  Warnings: 0	0.000 sec
3	53	15:38:38	SELECT *
 FROM `students`
 WHERE `name` = "federico"
 AND `surname` = "di murro"
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec
0	54	15:39:24	DROP *
 FROM `students`
 WHERE `name` = "federico"
 AND `surname` = "di murro"	Error Code: 1064. You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '*
 FROM `students`
 WHERE `name` = "federico"
 AND `surname` = "di murro"' at line 1	0.000 sec
3	55	15:40:22	DELETE FROM `students`
 WHERE `name` = "federico"
 AND `surname` = "di murro"	1 row(s) affected	0.032 sec