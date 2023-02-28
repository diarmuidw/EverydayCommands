### MYSQL datetime rounding to nearest whatever#

This is handy for grouping events into buckets

~~~
select *, 

 DATE_ADD(
        DATE_FORMAT(datetime, "%Y-%m-%d %H:00:00"),
        INTERVAL IF(MINUTE(datetime) < 30, 0, 1) HOUR
    ) AS rounded_hour
    ,
    
    FROM_UNIXTIME(FLOOR(UNIX_TIMESTAMP(datetime)/300)*300) as 5_min_bucket
    
 from table 

~~~
