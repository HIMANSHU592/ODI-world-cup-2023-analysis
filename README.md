# ODI-world-cup-2023-analysis
#Top 10 highest runs of batsman
SELECT 
    batting, SUM(runs) AS total_runs,BATTING_TEAM as country
FROM
    ipl.batting
GROUP BY batting,country
ORDER BY total_runs DESC limit 10;

#Top 10 highest wickettaker bowler
SELECT 
    bowling, bowling_team, SUM(wickets) AS wickets
FROM
    ipl.bowling
GROUP BY bowling , BOWLING_TEAM
ORDER BY wickets DESC
LIMIT 10;
