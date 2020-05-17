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
                3) While Transforming; Just write the logic: group up the things as follows 
                
                
                # Complete the transformation function
                def transform_avg_rating(rating_data):
                  # Group by course_id and extract average rating per course
                        avg_rating = rating_data.groupby('course_id').rating.mean()
                  # Return sorted average ratings per course
                        sort_rating = avg_rating.sort_values(ascending=False).reset_index()
                        return sort_rating

                # Extract the rating data into a DataFrame    
                rating_data = extract_rating_data(db_engines)

                # Use transform_avg_rating on the extracted data and print results
                avg_rating_data = transform_avg_rating(rating_data)
                print(avg_rating_data) 
 
