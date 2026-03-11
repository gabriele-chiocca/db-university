1. Selezionare tutti gli studenti nati nel 1990 (160)

SELECT `name`,`date_of_birth`
FROM university.students
WHERE YEAR(date_of_birth) = 1990;

2. Selezionare tutti i corsi che valgono più di 10 crediti (479)
   SELECT `name`,`cfu`
   FROM university.courses
   WHERE courses.cfu >= 11;

3. Selezionare tutti gli studenti che hanno più di 30 anni
   SELECT `name`, `date_of_birth`
   FROM university.students
   WHERE timestampdiff(YEAR, date_of_birth, CURDATE()) > 30;

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
   laurea (286)

SELECT `name`, `period`, `year`
FROM university.courses
WHERE courses.year = 1 &&
courses.period = "I semestre";

5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
   20/06/2020 (21)

   SELECT `hour`, `date`
   FROM university.exams
   WHERE exams.hour >= "16:00:00" &&
   exams.date = "2020/06/20";

6. Selezionare tutti i corsi di laurea magistrale (38)
   SELECT `name`, `level`
   FROM university.degrees
   WHERE degrees.level = "magistrale";
7. Da quanti dipartimenti è composta l'università? (12)

SELECT id
FROM university.departments;

8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

SELECT `name`, `surname`, `phone`
FROM university.teachers
WHERE teachers.phone IS NULL;
