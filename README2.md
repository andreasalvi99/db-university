1. Contare quanti iscritti ci sono stati ogni anno

```sql
SELECT
YEAR(enrolment_date),
COUNT(students.id)
FROM university.students
GROUP BY YEAR(enrolment_date);
```

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```sql
SELECT
office_address,
COUNT(teachers.id)
FROM university.teachers
GROUP BY office_address
```

3. Calcolare la media dei voti di ogni appello d'esame

```sql
SELECT
exams.date,
AVG(vote)
FROM university.exams
JOIN exam_student
ON exams.id = exam_student.exam_id
GROUP BY exams.date
```

4. Contare quanti corsi di laurea ci sono per ogni dipartimento
