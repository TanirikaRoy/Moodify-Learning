# Moodify-Learning

This is a virus simulator which tracks the the spread of a virus while considering 8 swaps per person
## The question:
![image](https://user-images.githubusercontent.com/81459933/113350207-c8302100-9356-11eb-8f91-0414bcbbd6c2.png)

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


## A possible set of Plots

![image](https://user-images.githubusercontent.com/81459933/113349866-4b04ac00-9356-11eb-8714-445842d5d33d.png)
![image](https://user-images.githubusercontent.com/81459933/113350276-e138d200-9356-11eb-8305-796869cf1a40.png)

