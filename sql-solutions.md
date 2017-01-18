




**EXERCISE**

Write a query that returns the day, month, year, species ID, and weight (in kg)
for individuals caught on Plot 1 that weigh more than 75 g.

**SOLUTION**

	SELECT
		surveys.day,
		surveys.month,
		surveys.year,
		species.species_id,
		surveys.weight / 1000.0
	FROM surveys
	JOIN species ON surveys.species_id = species.species_id
	WHERE surveys.weight > 75
	AND surveys.plot_id = 1;


**EXERCISE**

Write a query that returns day, month, year, species ID for individuals caught
in January, May and July.

 **SOLUTION**

	SELECT day, month, year, species_id
	FROM surveys
	WHERE month IN (1, 5, 7);




