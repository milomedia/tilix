---
layout: post
title: "HELL YES! I can still query relational databases"
date: 2017-1-12
draft: false
---
Today a friend asked me for help with writing a database query. SQL is one of my staples but it is not my strongest programming language. So I enjoy getting opportunities to increase my knowledge and experience in this area and was up for the challenge.

The story goes that ACME Energy Co has a number of customers that are disconnecting and reconnecting their prepayment services on a revolving basis. They collect raw data in their database and have some ideas about the management information they would like to extract from this.

Below you'll find more detail on the raw data (aka the input data), the business requirement and the desired output. Finally I give the _gist_ of the solution. As is not uncommon for programmers, I have not commented my code. That is left as an exercise for the reader ;-)

## The Input Data
In the input data (see table below) shows line entries for connecting disconnecting and reconnecting on the same or different days (-1 movement is for disconnection and 1 movement is for reconnection).

id | day | movement
|:--|:--|:--|
1 | 7834 | -1
1 | 7836 | 1
2 | 7526 | -1
2 | 7526 | 1
2 | 7682 | -1
2 | 7683 | 1
2 | 7793 | -1
3 | 7806 | -1
3 | 7813 | 1
4 | 7511 | -1
4 | 7529 | 1
4 | 8017 | -1
5 | 7526 | -1
5 | 7825 | 1
5 | 7862 | -1
5 | 7957 | 1


## The Business Requirement
**Can you write an SQL query to convert the input data (above) into the format in the table below?**

The rationale is that ACME Energy Co wants for each customer:

- the average time spent between each disconnection and reconnection
- the total number of disconnections
- the number of disconnections and reconnections on the same day
- max number of days a customer was disconnected

## The Deisred Output
Having the derived data in the table below is a big step towards achieving the result.

id | KPI
|:--|:--|:--|
1 | 2
2 | 0
2 | 1
2 | 43
3 | 7
4 | 18
5 | 299
5 | 95

# The Code
Loading the input data into SQLite was my starting point. Then I did some good old fashioned _interactive programming_ in DB Browser for SQLite. 

{% highlight sql %}
SELECT t1.id 
	,t1.day AS day1
	,MIN(t2.day) AS day2 
	,t2.day - t1.day as KPI
FROM input t1, input t2
WHERE t1.day <= t2.day
	AND t1.id = t2.id
	AND t1.movement = -1
	AND t2.movement = 1
GROUP BY t1.id, t1.day
ORDER BY t1.id ASC
{% endhighlight %}

FYI it was Stack Overflow which provided the initial inspiration for my solution: [Create a SQLite view where a row depends on the previous row](http://stackoverflow.com/questions/10003313/create-a-sqlite-view-where-a-row-depends-on-the-previous-row#10024388).
