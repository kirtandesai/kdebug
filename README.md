# Log Analysis tool
## This tool generates three reports from the news db
### 1. What are the most popular three articles of all time?
### 2. Who are the most popular article authors of all time?
### 3. On which days did more than 1% of requests lead to errors?


## Prepare database for reports

At your vagrant shell prompt run the following :

```
psql -d news -f log_analysis.sql
```

Once above steps completes successfully, you can run reports with the following code.

```
psql -d news -f log_analysis.sql
```


## Sample output
### The code should generate output like this.

```


#########    TOP 3 ARTICLES    #########
"Candidate is jerk, alleges rival"   --   338647 views
"Bears love berries, alleges bear"   --   253801 views
"Bad things gone, say good people"   --   170098 views
#########    #########    #########




#########    TOP AUTHORS    #########
Ursula La Multa   --   507594 views
Rudolf von Treppenwitz   --   423457 views
Anonymous Contributor   --   170098 views
Markoff Chaney   --   84557 views
#########    #########    #########




#########    ONE PCT ERRORS    #########
2016-07-17   --   2.2626862468 % errors
#########    #########    #########


ALL REPORTS GENERATED!
```
