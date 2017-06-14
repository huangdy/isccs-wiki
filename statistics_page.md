Description: The statistics page has a summary section on the top of the page and histograms at the bottom of the page.[Statistic_Page.pdf](/uploads/a6add194a9d270db651b288ffb4caad9/Statistic_Page.pdf)
* API: 

For department/agency:
http://localhost:8080/isccs/api/query/statistics?type=department&list=1000,1001,1002,7000,7001,7002,7057

For facility:
http://localhost:8080/isccs/api/query/statistics?type=facility&list=7057:BA1,7057:BA10,7057:BA1000,7057:BA1001,7057:BA1002,0000:AAAA,1000:ZZZZ

* Overall layout
See page 1 of PDF

* Summary Section 
See page 2 of PDF.  There are two summaries based on type, department or facility.

* Histograms
See page 3 of PDF for a mockup.  
1. Each histogram represents each question in the Benchmark Document.
2. X-axis is the score of each of the question.  The scores are 0, 1, 2, 3, 4, 5.
3. Y-axis is the number of queried departments (or facilities) that answered the score in the X-axis.  User can eye-ball the result.  
4. Hovering over the short text that is above the graph will display a popup of the full-text of that question. **If possible, make this popup always appears very top right corner of the page so the actual histogram does not get covered over by the popup**
5. Hovering over a specific column of the histogram will display a popup of the actual number.  
**The name of the game is "make it looks good".**
