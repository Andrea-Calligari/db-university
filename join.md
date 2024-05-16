# 1 . Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia :

    - SELECT  `degrees`. `name`, `students`.`name`
      FROM `degrees`
      INNER JOIN `students`
      ON `degrees`.`id` = `students`.`degree_id`
      WHERE `degrees`.`name`= 'Corso di Laurea in Economia';

    - 68

# 2 . Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze:

    - SELECT `departments`.`name`, `degrees`.`name`
      FROM `degrees`
      INNER JOIN `departments`
      ON `degrees`. `department_id` = `departments`. `id`
      WHERE `departments`.`name`= 'Dipartimento di Neuroscienze' AND `degrees`.`level` = 'magistrale';

      - 1

# 3 . Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44) :
    
    - SELECT * 
      FROM `courses`
      INNER JOIN `course_teacher`
      ON `courses`.`id`  = `course_teacher`.`course_id`
      INNER JOIN `teachers`
      ON `course_teacher`.`teacher_id` = `teachers`.`id`
      WHERE `teacher_id` = 44;

    - 11

# 4 .  Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome :

    - SELECT * 
      FROM `students`
      INNER JOIN `degrees`
      ON `students`.`degree_id` = `degrees`.`id`
      INNER JOIN `departments`
      ON `degrees`.`department_id`= `departments`.`id`
      ORDER BY `students`.`name`, `students`.`surname` ASC;

    - 5000

# 5 . Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti:

    - SELECT `degrees`.`name` AS `corso_di_laurea`, `courses`.`name` AS `nome_corso`,`teachers`.`name` AS `nome_insegnante`
      FROM `degrees`
      INNER JOIN `courses`
      ON `degrees`.`id`= `courses`.`degree_id`
      INNER JOIN `course_teacher`
      ON `courses`.`id` = `course_teacher`.`course_id`
      INNER JOIN `teachers`
      ON `course_teacher`.`teacher_id` = `teachers`.`id`;

    - 1317

# 6 . Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54):

    - 
    -