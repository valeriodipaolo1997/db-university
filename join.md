<!--query n 1-->
SELECT COUNT(*) AS `enrolment_year`, YEAR(`enrolment_date`) AS `year` 
FROM `students` 
GROUP BY `year`;

<!--query n 2-->
SELECT COUNT(*) AS `teachers_number`, `office_address` 
FROM `teachers` 
GROUP BY `office_address`;