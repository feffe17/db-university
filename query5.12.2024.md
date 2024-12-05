<!-- Group by -->

<!--1. Contare quanti iscritti ci sono stati ogni anno -->
select year(`date_of_birth`) as `year`, count(*) as `totale_iscritti`
from `students`
group by year(`date_of_birth`)

<!--2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio -->
SELECT `office_address` as `Indirizzo`, COUNT(*) as `totale_insegnanti`
from `teachers`
group by `office_address`


<!--3. Calcolare la media dei voti di ogni appello d'esame -->
SELECT AVG(`vote`) as `media_voto`, `exam_id`as `id_esame`
from `exam_student`
group by `exam_id`



<!--4. Contare quanti corsi di laurea ci sono per ogni dipartimento -->
select count(*) `corsi`, `degree_id` as `dipartimenti`
from `courses`
group by `degree_id`


<!-- Join -->

<!--1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia -->
SELECT `students`.*
FROM `students`
JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

<!--2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze -->
select `degrees`.*
from `degrees`
join `departments` on `departments`.`id` = `degrees`.`department_id`
where `degrees`.`level` = 'Magistrale'
and `departments`.`name` = 'Dipartimento di Neuroscienze'


<!--3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44) -->
select `courses`.`name` as `Nome Corso`
from `courses`
join `course_teacher` on `courses`.`id` = `course_teacher`.`course_id`
join `teachers` on `course_teacher`.`teacher_id` = `teachers`.`id`
where `teachers`.`id` = '44'

<!--4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome -->
select `students`.*, `departments`.`name` as `nome_dipartimento`, `degrees`.`name` as `corsi di larurea`
from `students`
join `degrees` on `students`.`degree_id` = `degrees`.`id` 
join `departments` on `degrees`.`department_id` = `departments`.`id`
order by `students`.`surname` ASC

<!-- Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti -->
SELECT `degrees`.`name` AS `facoltà`,
`courses`.`name` AS `corso`,
`teachers`.`name` AS `nome professore`,
`teachers`.`surname` AS `cognome professore`
FROM `degrees`
JOIN `courses` 
ON `courses`.`degree_id` = `degrees`.`id`
JOIN `course_teacher` 
ON `courses`.`id` = `course_teacher`.`course_id`
JOIN `teachers` 
ON `teachers`.`id` = `course_teacher`.`teacher_id`;

<!-- Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54) -->
SELECT DISTINCT `teachers`.`id`,
`teachers`.`name` AS `nome`,
`teachers`.`surname` AS `cognome`,
`departments`.`name` AS `dipartimento`
FROM `teachers`
JOIN `course_teacher` 
ON `teachers`.`id` = `course_teacher`.`teacher_id`
JOIN `courses` 
ON `course_teacher`.`course_id` = `courses`.`id`
JOIN `degrees` 
ON `degrees`.`id` = `courses`.`degree_id`
JOIN `departments` 
ON `departments`.`id` = `degrees`.`department_id`
WHERE `departments`.`name` = 'Dipartimento di Matematica';

