<!-- Group by: -->
<!-- Contare quanti iscritti ci sono stati ogni anno -->
```sql
SELECT COUNT(id), YEAR(students.enrolment_date)
FROM `students`
GROUP BY YEAR(enrolment_date);
```
<!-- Contare gli insegnanti che hanno l'ufficio nello stesso edificio -->
```sql
SELECT COUNT(id), `office_address`
FROM `teachers`
GROUP BY `office_address`;
```
<!-- Calcolare la media dei voti di ogni appello d'esame -->
```sql
SELECT AVG(exam_student.vote), `exams`.`date`
FROM `exam_student`
JOIN `exams`
ON `exam_student`.`exam_id` = `exams`.`id`
GROUP BY `exams`.`date`;
```
<!-- Contare quanti corsi di laurea ci sono per ogni dipartimento -->
```sql
SELECT COUNT(id), `departments`.`name`
FROM `degrees`
JOIN `departments`
ON `degrees`.`departments_id` = `departments`.`id`
GROUP BY `departments`.`name`;
```
