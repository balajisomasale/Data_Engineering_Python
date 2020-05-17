# Data_Engineering_Python from Datacamp

API's used in this course:


        =>We saw how to split up a task and use the low-level python **multiprocessing.Pool** API to do calculations on several processing units. 
        =>It's essential to understand this on a lower level, but in reality, you'll never use this kind of APIs.
        => A more convenient way to parallelize an apply over several groups is using the **dask framework** and its abstraction of the pandas DataFrame,
        
        
        
 ETL +  postgresql (how to fetch from an API:
              
## Fetch from an API

import requests

 Fetch the Hackernews post
resp = requests.get("https://hacker-news.firebaseio.com/v0/item/16222426.json")

 Print the response parsed as JSON
print(resp.json())

 Assign the score of the test to post_score
post_score = resp.json()['score']
print(post_score)

## CapstoneProject :Ratings Recommendation
(ETL Approach: Extract first,Transform the data(cleaning,removing spaces amd all ) to make sense out of it and then load it) 
Goal: We have two tables with course and ratings for 3 users. Following things are to be done step by step to achieve The recommedations based onAverageRatings 
                
                1) Thinking for logic : Build(Dont Implement) a relation between two table: wirte sql query to group up the things 
                2) As we use ETL Approach : Extract the data first and then transform the data
                3) While Transforming; Just write the logic: 
                4) Load the data into postgre table to do Airflow job=> Sending Email daily based on the ratings of the courses
            
Check for the Capstone porject here => https://github.com/balajisomasale/Data_Engineering_Python/blob/master/Introduction%20to%20Data%20Engineering/1%20-%20Introduction%20to%20Data%20Engineering.ipynb
 
