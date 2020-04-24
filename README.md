# mysql-slow-query-log-visualizer

A slow query log visualiser for slow MySQL queries. Forked from https://code.google.com/p/mysql-slow-query-log-visualizer/

It is live (no need to download yourself) thanks to githubs pages feature here: http://privatejava.github.io/mysql-slow-query-log-visualizer/

It supports for AWS Insight Logs of RDS as well.

** Sample Cloud Watch Logs Insights **

```
**CloudWatch Logs Insights**
region: us-east-2
log-group-names:  /aws/rds/cluster/db-cluster-1/slowquery, /aws/rds/cluster/db-cluster-1/general
start-time: 2020-04-23T20:28:00.999Z
end-time: 2020-04-23T20:31:00.000Z
query-string:
\`\`\`
fields @timestamp, @message
| sort @timestamp asc
| limit 10000
\`\`\`


-----------------------------------------------------------
| @timestamp   |   @message     |
-----------------------------------------------------------
| 2020-04-23 20:28:01.737 | # Time: 2020-04-23T20:28:01.737256Z # User@Host: rdsadmin[rdsadmin] @ localhost []  Id: 322915 # Query_time: 0.000248  Lock_time: 0.000141 Rows_sent: 1  Rows_examined: 1 SET timestamp=1587673681; SELECT SQL_NO_CACHE value FROM mysql.rds_heartbeat2;                                                                  |
```
