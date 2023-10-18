<!-- Joins: -->
<!-- Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia -->
```sql
SELECT * , `degrees`.`name`
FROM `students`
JOIN `degrees`
ON `students`.`degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia';
```
<!-- Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze -->
```sql
SELECT *, `departments`.`name`
FROM `degrees`
JOIN `departments`
ON `degrees`.`department_id` = `departments`.`id`
WHERE `degrees`.`level` = 'Magistrale'
AND `departments`.`name` = 'Dipartimento di Neuroscienze';
```
<!-- Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44) -->
```sql
SELECT `degrees`.`name`, `teachers`,`name`, `teachers`.`surname`
FROM `courses`
JOIN `degrees` ON `courses`.`degree_id` = `degrees`.`id`                              
JOIN `course_teacher` ON `course_teacher`.`course_id` = `courses`.`id`
JOIN `teachers` ON `course_teacher`.`teacher_id` = `teachers`.`id`
WHERE `teachers`.`name` = 'Fulvio'
AND `teachers`.`surname` = 'Amato';
```
<!-- Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome -->
```sql
```
<!-- Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti -->
```sql
```
<!-- Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54) -->
```sql
```
<!-- BONUS: Selezionare per ogni studente il numero di tentativi sostenuti per ogni esame, stampando anche il voto massimo. Successivamente, filtrare i tentativi con voto minimo 18. -->
```sql
```

`