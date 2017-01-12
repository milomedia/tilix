---
layout: post
title: "HELL YES! I can still write code"
date: 2017-1-12
draft: false
---
Today a friend asked me for help with some SQL. Its not my strongest language so I enjoy getting opportunities to increase my knowledge and experience.

ACME Energy Co has a number of customers that are disconnecting and reconnecting their prepayment services on a revolving basis.

## The Data
In the input data (see table below) shows line entries for connecting disconnecting and reconnecting on the same or different days (-1 movement is for disconnection and 1 movement is for reconnection).

id | day | movement
|:--|:--|:--|
1 | 7834 | -1
1 | 7836 | 1
2 | 7526 | -1
2 | 7526 | 1
2 | 7557 | -1
2 | 7557 | 1
2 | 7587 | -1
2 | 7587 | 1
2 | 7618 | -1
2 | 7618 | 1
2 | 7682 | -1
2 | 7683 | 1
2 | 7714 | -1
2 | 7715 | 1
2 | 7751 | -1
2 | 7751 | 1
2 | 7793 | -1
2 | 7836 | 1
2 | 7873 | -1
2 | 7878 | 1
2 | 7909 | -1
2 | 7927 | 1
2 | 8018 | -1
3 | 7806 | -1
3 | 7813 | 1
4 | 7511 | -1
4 | 7529 | 1
4 | 8017 | -1
5 | 7526 | -1
5 | 7825 | 1
5 | 7862 | -1
5 | 7957 | 1


## The Requirement
**Can you write an SQL query to convert the input data (above) into the format in the table below?**

The rationale is that ACME Energy Co wants for each customer:

- the average time spent between each disconnection and reconnection
- the total number of disconnections
- the number of disconnections and reconnections on the same day
- max number of days spent for each customer to reconnect

Having the derived data in the table below is a big step towards achieving the result.

id | KPI
|:--|:--|:--|
1 | 2
2 | 0
2 | 0
2 | 0
2 | 0
2 | 1
2 | 1
2 | 0
2 | 43
2 | 5
2 | 18
3 | 7
4 | 18
5 | 299
5 | 95

# The Code
Loading the input data into SQLite was the starting point. Then some good old fashioned _interactive programming_ in DB Browser for SQLite. 

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
