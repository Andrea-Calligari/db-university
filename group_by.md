 # 1 . Contare quanti iscritti ci sono stati ogni anno

    - SELECT COUNT(*) AS `numero_studenti`, YEAR(`enrolment_date`) AS `anno`
      FROM `students`
      WHERE YEAR(`enrolment_date`)
      GROUP BY `anno`;

# 2 . Contare gli insegnanti che hanno l'ufficio nello stesso edificio

    - SELECT COUNT(*) AS  `insegnanti`, `office_address` AS `edificio`
      FROM `teachers`
      GROUP BY  `edificio`;

# 3 . Calcolare la media dei voti di ogni appello d'esame

    - SELECT AVG(`vote`) AS `media_voto`, `exams`.`address` AS `appello_d/esame`
      FROM `exam_student`
      INNER JOIN `exams`
      ON `exam_student`.`exam_id`= `exams`.`id`
      GROUP BY  `appello_d/esame`;

# 4 . Contare quanti corsi di laurea ci sono per ogni dipartimento
    - 