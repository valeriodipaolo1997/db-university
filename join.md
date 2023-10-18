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