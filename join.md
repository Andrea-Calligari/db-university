# 1 . Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia :
    - SELECT  `degrees`. `name`, `students`.`name`
        FROM `degrees`
        INNER JOIN `students`
        ON `degrees`.`id` = `students`.`degree_id`
        WHERE `degrees`.`name`= 'Corso di Laurea in Economia';
        
    - 68

# 2 . Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze:
    - 