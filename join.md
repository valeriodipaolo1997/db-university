<!--query n 1-->

SELECT COUNT(*) AS `enrolment_year`, YEAR(`enrolment_date`) AS `year` 
FROM `students` 
GROUP BY `year`;