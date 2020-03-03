ASSESSMENT 7 EXERCISE
Overview: Within PGAdmin, create the following table and alter it as requested.
id first_name last_name rank weapon midichlorians
1 Obi-wan Kenobi Retired Jedi lightsaber 13400
2 Luke Skywalker Jedi lightsaber 14500
3 Darth Vader Sith Lord The Force 27700
4 Bobba Fett Bounty
Hunter
Blaster 1050
5 Han Solo Smuggler Millenium
Falcon
1050
6 Chewbecca Co Pilot Arms 7200
Submission:
In the space below, paste all SQL code necessary to complete this challenge, including the
statement to create the table. For each of the ten numbered bullets you should have some
SQL code. You do not need to submit the results of the queries, just the SQL code itself.
SQL Statements:
1. Construct a table named star_wars . star_wars has 5 columns.
○ id - serial, primary key
○ first_name - varchar 20
○ last_name - varchar 20
○ rank - varchar 30
○ weapon - varchar 30
2. Add the 5 people from above to the table.
3. Update the person with the id of 3 to have a last_name of Sidious .
4. Remove the person with the id of 4 .
5. Select all people that have a first_name of Skywalker .
6. Select all people with both the first_name of Han AND the last_name of Solo .
7. Select all people that have an id under 3 .
8. Select all people that do NOT have the weapon of lightsaber .
9. Get the lowest midichlorian count in the table
10. Get all of the characters with less than 10000 midichlorian
11. You have to have at least 7000 midichlorians to qualify for Jedi training. Get all potential
Jedi trainees
12. Update the person with the id of 5 to have a weapon of DL-44 Blaster .
13. Delete the contents from the database.