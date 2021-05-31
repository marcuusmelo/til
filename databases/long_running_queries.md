# Long Running Queries

The following SQL statement will return a list of long running quries

```
SELECT
  pid,
  now() - pg_stat_activity.query_start AS duration,
  query,
  state
FROM pg_stat_activity
WHERE (now() - pg_stat_activity.query_start) > interval '5 minutes';
```

Note that the queries in the IDLE state are not the problem. Active long running queries are the ones that may be the reason for a low database performance.

To cancel any queries you identified to be potentially problematic to you:
```
SELECT pg_cancel_backend({pid});
```

