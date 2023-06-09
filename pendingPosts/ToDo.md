# Create blog
https://dev.to/anuraggharat/how-to-create-a-blog-using-nextjs-and-markdown-3j9o
https://github.com/gregrickaby/nextjs-github-pages
https://dev.to/github/how-to-host-a-static-nextjs-site-on-github-pages-4pe0


# Data Engg interview
https://medium.com/python-in-plain-english/the-data-engineering-interview-guide-710b621f3ff1


# PYTHON:
https://mathspp.com/blog/pydonts/dunder-methods


# SQL
LISTAGG / STRING_AGG
INTERSECT
EXCEPT
cast ::
https://stackoverflow.com/questions/34627026/in-vs-any-operator-in-postgresql
EXISTS NULL case: https://www.postgresqltutorial.com/postgresql-tutorial/postgresql-exists/


MySQL:
DATE_ADD(date, INTERVAL value addunit): addunit same as above
DATEDIFF( )
DAYNAME( ), DAYOFMONTH( ), DAYOFWEEK( ), DAYOFYEAR( )
EXTRACT(_ FROM hiredate) | second, minute, hour, day, week, month, quarter, year, etc
     https://medium.com/analytics-vidhya/mysql-functions-cheatsheet-with-examples-3a08bb36d074
DATE_FORMAT(date, format)


Postgres:
date addn:
     SELECT date '2027-05-20' + integer '5';      -- 5 days
     SELECT date '2027-05-20' + interval '5 minute';
     SELECT date '2027-05-20' + time '05:45';
     SELECT date '2027-05-20' + interval '5 week';
     SELECT date '2027-05-20' + interval '5 month';
date difference:
     SELECT ('2015-01-12'::date - '2015-01-01'::date) AS days;
     DATE_PART('day', MAX(joindate) - MIN(joindate)) as date_diff
     select extract(day from 'DATE_A'::timestamp - 'DATE_B'::timestamp);
EXTRACT( __ FROM published_date) : 
TO_CHAR(NOW():: DATE, 'mm dd, yyyy');



## Window function:
https://www.postgresqltutorial.com/postgresql-window-function/
CUME_DIST	Return the relative rank of the current row.
DENSE_RANK	Rank the current row within its partition without gaps.
FIRST_VALUE	Return a value evaluated against the first row within its partition.
LAG	Return a value evaluated at the row that is at a specified phy,sical offset row before the current row within the partition.
LAST_VALUE	Return a value evaluated against the last row within its partition.
LEAD	Return a value evaluated at the row that is offset rows after the current row within the partition.
NTILE	Divide rows in a partition as equally as possible and assign each row an integer starting from 1 to the argument value.
NTH_VALUE	Return a value evaluated against the nth row in an ordered partition.
PERCENT_RANK	Return the relative rank of the current row (rank-1) / (total rows – 1)
RANK	Rank the current row within its partition with gaps.
ROW_NUMBER	Number the current row within its partition starting from 1.

# Airflow
Operator

# Terms
high cardinality
scd

# Optimization
explain plan
encoding and compression
performance stats

-- teradtaa:
SELECT q.QueryText,AMPCPUTime as CPU_consumption,
MaxAMPCPUTime,
Impact_CPU,
CAST(EXTRACT(HOUR FROM ((q.FirstRespTime - q.StartTime) HOUR(3) TO SECOND(6) ) ) * 3600
     + EXTRACT(MINUTE FROM ((q.FirstRespTime - q.StartTime) HOUR(3) TO SECOND(6) ) ) * 60
     + EXTRACT(SECOND FROM ((q.FirstRespTime - q.StartTime) HOUR(3) TO SECOND(6) ) ) AS DECIMAL(10,2)) AS response_secs
     ,response_secs/60.0  AS response_mins
	 from 
	 DBC.QryLogV q
-- Specify your user name and Query band
WHERE USERNAME = <USER_NAME>
AND QUERYBAND ='UUID=19c1ccc5-ff2a-4d2d-8114-1fb625ad44df;';

# architecture and design
- Twitter Snowflake: https://blog.twitter.com/engineering/en_us/a/2010/announcing-snowflake
- Career projects:
  Description: Media to look at for inspiration about career
  Playlist:
    - AWS Reinvent Use cases: https://www.youtube.com/playlist?list=PL2yQDdvlhXf8re22uN1Wp5zuvu96MtVbj
    - Demonware Lookup: https://www.activision.com/cdn/research/The_Road_to_Direct_Lookups.pdf
    - Discord:
      - https://www.youtube.com/watch?v=xynXjChKkJc
      - https://discord.com/blog/how-discord-stores-trillions-of-messages
      - https://discord.com/blog/how-discord-stores-billions-of-messages
    - AWS Lambda:
      - https://www.youtube.com/playlist?list=PL5KTLzN85O4KO0qEeUVvwTTcHFsdE6Dhx
      - https://www.youtube.com/@BeABetterDev/playlists
