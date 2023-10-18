<!--query n 1-->
SELECT COUNT(*) AS `enrolment_year`, YEAR(`enrolment_date`) AS `year` 
FROM `students` 
GROUP BY `year`;

<!--query n 2-->
SELECT COUNT(*) AS `teachers_number`, `office_address` 
FROM `teachers` 
GROUP BY `office_address`;

<!--query n 3-->
SELECT COUNT(`exam_id`) AS `exams_count`, AVG(`vote`) AS `average_vote` 
FROM `exam_student` 
GROUP BY `exam_id`;

<!--query n 4-->
SELECT COUNT(*) AS `degrees_count`, `department_id`
FROM `degrees`
GROUP BY `department_id`;


JOIN:

<!--join n 1-->
SELECT `students`.`name`, `students`.`surname`, `students`.`registration_number`, `degrees`.`name` AS `degree_name`
FROM `students`
JOIN `degrees` ON `degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

<!--join n 2-->
SELECT `degrees`.`name`, `degrees`.`level`, `departments`.`name` AS `department_name`
FROM `degrees`
JOIN `departments` ON `department_id` = `departments`.`id`
WHERE `departments`.`name` = 'Dipartimento di Neuroscienze';


<!--join n 3-->
SELECT `courses`.`name` AS `course_name`, `teachers`.`name` AS `teacher_name`, `teachers`.`surname` AS `teacher_surname`
FROM `course_teacher`
JOIN `courses` ON `course_id` = `courses`.`id`
JOIN `teachers` ON `teacher_id` = `teachers`.`id`
WHERE `teacher_id` = 44;