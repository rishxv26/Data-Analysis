# Liverpool

I will using available up to date data from FBREF website to analysis the current season(2024-2025) of Liverpool in the English Premier League.

Finding the total number of cleansheets for Liverpool in the season so far.
A clean sheet in football means the team did not concede any goals, so it can 
either be a win and the oppononent not scoring or a draw where the score is 0-0.

```sql
SELECT COUNT(Opponent) AS Cleansheet
FROM Liverpool_stats
WHERE (GF > 0 AND GA = 0)
   OR (GF = 0 AND GA = 0);
