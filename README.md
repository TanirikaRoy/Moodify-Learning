# Moodify
- [x] Week 1
- [x] Week 2
- [x] Week 3
- [x] Week 4
- [x] Week 5-8 Implementation


## Week 1

Made a virus simulator which tracks the the spread of a virus while considering 8 swaps per person
### The question:
* Create a two-dimensional matrix of dimention 100 * 150 containing 15,000 entries with value 0. Set the entry (50,75) to be 1.
* 8 random entries swap with another set of 8 random entries
* If 13 is the selected entry, 7,8,9,12,14,17,18,19 are 1st neighbours and 1,2,3,4,5,6,10,11,15,16,20,21,22,23,24,25 are 2nd neighbours.
* 1st neighbours of an entry containing 1 each have a 0.25 probability of getting converted to 1.
* 2nd neighbours of an entry containing 1 each have a 0.08 probability of getting converted to 1.
* Each entry has an independent probability of getting converted to 1 depending upon its relative position to an entry containing 1.
* Note that it is not mandatory for one of the neighbours to be converted into 1.
* Keep repeating the process till every entry becomes 1.
* Plot 1: Number of ones in the matrix vs Number of iterations
* Plot 2: Change in number of ones in each iteration vs Number of iterations
* Print the peak value in Plot 2. Make sure you label the axes in both the plots


### A possible set of Plots

![image](https://user-images.githubusercontent.com/81459933/113351209-27426580-9358-11eb-847e-2c3ff941cfa2.png)
![image](https://user-images.githubusercontent.com/81459933/113351230-30333700-9358-11eb-9c5b-f0bf12716bd9.png)

## Week 2

### Problem 1:

#### Conclusions
##### Challenge 1:

1. -Min AveMonthSpend = 22
   -Max AveMonthSpend = 176
   -Mean AveMonthSpend = 72.39
   -Median AveMonthSpend = 68
   -SD AveMonthSpend = 27.26
2. More customers have not bought bikes.
3. Median yearly income is as follows: Management > Professional > Skilled Manual > Clerical > Manual Occupation
4. Customers with no children at home have a lower median AvgMonthSpend values than customers with one or more children at home.
5. Married customers have a higher median AvgMonthSpend than single customers.
6. Male customers have a higher median AvgMonthSpend than female customers.
7. Male customers are more likely to buy bikes than female customers.
8. Median yearly income is higher for customers who bought a bike.
9. The code for this project is in Problem-1.ipynb
10. The values of AveMonthSpend that I get by running my model on the test dataset is there in Problem-1.csv. <br/>
## Problem-2
Trained the model and used the test data to test it.


# Week 3
Watched video lectures and made a detailed report on the google ML standardisation course. Learnt Aabout ML, error loss, etc.

# Week 4
* Learnt logistic and linear regression.
* Poblem 1 was without using any standard models or pre exisitng codes, to make an entire pricing model.
Problem 2: we could use library functions which were inbuilt in Keras and Tensorflow. hence making training and Test set wasnt an issue. Plots were also basic and simpler.
Also basic principles of Data frames and making CSV files were also learnt which came in very handy in the later half of the project.
 
# Week 5-8: Music API
This was the implementation part of the project. 
We were divided into teams:
1. Music API
2. Music Clustering
3. Facial Recognition
4. App Development

I was a part of the Music API Team. 
* In the subsequent weeks, we first worked on making a pipeline for continuous fetching of songs and made a test set of 600 songs based on mood. We also hand picked the 16 features for our model ranging from danceability, energy, tone, pitch,duration etc.
* After picking out the features, we prepared a code to first generate the access token for the user and then another code to fetch the songs with their feature data using the song ids
* We enabled user authorization using Client ID and Client Secret and generated token
* We Fetched songs dataset with features such that they can be further classified based on mood 
* We scraped through API calls using sptotipy which is the python spotify Library.
* Found a dataset or api that contains songs and the moods associated with them.
* Came up with an algorithm where in we had the song features and sampled out songs from a large chunk of song database that matched best with the obtained features. This was a very crucial part since these are the songs that would be suggested to the user.
* For the final step and here we faced so many issues with the WEB API and the coding integration with python in general with the USER AUTH PART. We had to:
  - Authenticate User  
  - Find User’s song history
  - Fetch song features
  - Make a playlist in spotify

We tried our best to complete these assigned tasks and I was assisted by my subteam mate, Dhawal Singh. 
