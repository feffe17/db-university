
CREATE DATABASE university
USE university
SELECT *
FROM `students`

<!-- 1. Selezionare tutti gli studenti nati nel 1990 (160) -->
SELECT *
 FROM `students`
 WHERE year(`date_of_birth`) = "1990"

<!-- 2. Selezionare tutti i corsi che valgono più di 10 crediti (479) -->
SELECT *
 FROM `COURSES`
 WHERE `cfu` > 10

<!-- 3. Selezionare tutti gli studenti che hanno più di 30 anni -->
SELECT *
 FROM `STUDENTS`
 WHERE 2024 - year(`date_of_birth`) >= 30
 LIMIT 0, 1000	1000 row(s) returned	0.000 sec / 0.000 sec

<!-- 4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286) -->
SELECT *
 FROM `COURSES`
 WHERE `year` = 1
 AND `period` = "I semestre"

<!-- 5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21) -->
SELECT *
 FROM `EXAMS`
 WHERE `date` = "2020-06-20"
 AND hour(`hour`) >= 14

<!-- 6. Selezionare tutti i corsi di laurea magistrale (38) -->
SELECT *
 FROM `degrees`
 WHERE `level` = "magistrale"

<!-- 7. Da quanti dipartimenti è composta l'università? (12) -->
SELECT *
 FROM `departments`

<!-- 8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50) -->
SELECT *
 FROM `teachers`
 WHERE `phone` IS NULL

<!-- 9. Inserire nella tabella degli studenti un nuovo record con i propri dati (per il campo degree_id, inserire un valore casuale) -->
INSERT INTO `students` (`name`, `surname`, `date_of_birth`, `email`, `fiscal_code`, `degree_id`, `enrolment_date`, `registration_number`)
 VALUES ('mario', 'rossi', '1903-02-17', 'ggg@gmail.com', 'RSSMRA85D15H501X', 64, "2024-08-20", "9999999")
 
 <!-- 10. Cambiare il numero dell’ufficio del professor Pietro Rizzo in 126 -->
UPDATE `teachers`
 SET `office_number` = 126
 WHERE `name` = 'Pietro' AND `surname` = 'Rizzo'	
 
 <!-- 11. Eliminare dalla tabella studenti il record creato precedentemente al punto 9 -->
DELETE FROM `students`
 WHERE `name` = "federico"
 AND `surname` = "di murro"	1 row(s) affected	0.032 sec




 ____________________

<!-- APPUNTI -->

 <!-- USE university;
#SELECT `courses`.*, `degreese`.*
/*SELECT `courses`.`id` AS `courses_id`,
`courses`.`name` AS `course_name`,
`courses`.`period`,
`courses`.`year`,
`courses`.`cfu`,
`degrees`.`id` AS `degrees_id`,
`degrees`.`name` AS `degrees_name`
FROM `courses`
JOIN `degrees`
ON `courses`.`degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = "Corso di Laurea in Informatica"*/

#Selezionare le informazioni sul corso con id = 144, con tutti i relativi appelli d’esame
/*SELECT `courses`.`id` AS `id_corso`,
`courses`.`name` AS `course_name`,
`courses`.`period`,
`courses`.`year`,
`courses`.`cfu`,
`courses`.`description`,
`courses`.`website`,
`exams`.`id` AS `Id_esame`,
`exams`.`date`,
`exams`.`hour`,
`exams`.`address`,
`exams`.`location`
FROM `courses`
JOIN `exams`
ON `exams`.`course_id` = `courses`.`id`
WHERE `courses`.`id` = 144*/ -->