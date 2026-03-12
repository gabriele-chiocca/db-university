1. Contare quanti iscritti ci sono stati ogni anno
   SELECT YEAR(enrolment_date) AS anno, COUNT(\*) As numero_iscritti
   FROM university.students
   GROUP BY YEAR(enrolment_date)

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
   SELECT office_address AS uffici, COUNT(_) AS Numero_insegnanti
   FROM university.teachers
   GROUP BY office_address
   HAVING COUNT(_) > 1;

3. Calcolare la media dei voti di ogni appello d'esame
4. Contare quanti corsi di laurea ci sono per ogni dipartimento
