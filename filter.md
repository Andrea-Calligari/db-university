

# 1 Selezionare tutti gli studenti nati nel 1990 : 
    - 160 studenti.

    SELECT *
    FROM `students`
    WHERE `date_of_birth` LIKE '1990%';

# 2 Selezionare tuutti i corsi che valgono più di 10 crediti :
    -  479 corsi.

    SELECT *
    FROM `courses`
    WHERE `cfu` > 10;

# 3 Seleziona gli studenti che hanno più di 30 anni : 
     - 3646 stuenti.
     SELECT * 
    FROM `students`
    WHERE YEAR(CURDATE()) - YEAR(`date_of_birth`) > 30;




    
    
# 4 Selezionare tutti i corsi del primo semestre del primo anno di una qualsiasi corso di laurea :
     - I corsi di Biologia molecolare del primo semestre del primo anno  sono 3, invece, in un corso di  Laurea qualisiasi sono 286.

    SELECT * 
    FROM `courses`
    WHERE `period` = 'I semestre' AND `year`= 1;

    SELECT * 
    FROM `courses`
    WHERE `period` = 'I semestre' AND `year`= 1 AND `degrees_id` = 2 ;

# 5 Selezionare tutti i corsi di laurea magistrale:
    - 38 corsi di Laurea Magistrale.

    SELECT *
    FROM `degrees`
    WHERE `level` = 'magistrale';

# 6 Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020:
    - Gli appelli d'esame dopo le 14 del 20/06/2020 sono 21.
    
    SELECT *
    FROM  `exams`
    WHERE `hour` > '14:00:00' AND `date` = '2020/06/20';

    <!-- oppure -->

    WHERE HOUR('hour') >= 14;

# Da quanti dipartimenti è composta l'università?:
    - L'università è composta da 12 dipartimenti.

    SELECT COUNT(*)
    FROM `departments`;

# Quanti sono gli insegnanti senza numero di cellulare?:
    - Gli insegnanti senza numero di cellulare sono 50.

    SELECT *
    FROM `teachers`
    WHERE `phone` IS NULL;
