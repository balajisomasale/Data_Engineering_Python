# Data_Engineering_Python from Datacamp

API's used in this course:


        =>We saw how to split up a task and use the low-level python **multiprocessing.Pool** API to do calculations on several processing units. 
        =>It's essential to understand this on a lower level, but in reality, you'll never use this kind of APIs.
        => A more convenient way to parallelize an apply over several groups is using the **dask framework** and its abstraction of the pandas DataFrame,
        
        
        
 ETL (how to fetch from an API:
              
## Fetch from an API

import requests

# Fetch the Hackernews post
resp = requests.get("https://hacker-news.firebaseio.com/v0/item/16222426.json")

# Print the response parsed as JSON
print(resp.json())

# Assign the score of the test to post_score
post_score = resp.json()['score']
print(post_score)
