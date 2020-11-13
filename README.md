# TOPSIS-Sunidhi-101983052
With this you can calculate the TOPSIS score and RANK of the data provided in '.csv' format.
- Input file:
  - contain three or more columns
  - contain five rows
  - First column is the object/variable name.
  - From 2nd to last column contain numeric values only

# Overview
  - You can check intermediate steps as well as the final score as I described below- normalized matrix, weight normalized decision matrix , ideal best worst, euclidean distance, topsis score and rank.

## Usage

In the following paragraphs, I am going to describe how you can get topsis score and rank and use TOPSIS for your own projects.

### Getting it
To download TOPSIS, either fork this github repo or simply use Pypi via pip.

    $ pip install TOPSIS-Sunidhi-101983052

### Using it
TOPSIS was programmed with ease-of-use in mind. Just, import topsis from TOPSIS-Sunidhi-101983052

    from TOPSIS-Sunidhi-101983052 import topsis


## topsis


### normalized_matrix
First we make normalized matrix. This is done by first squaring the first column value and then add them, suppose we put the value in variable sum and then we divide the column wise elements by the varible sum. This is done upto the last column. We implement this using for loop. 

### weight-normalized
In this we multiply the column by the corresponding weight value. No. of weights should be equal to the no. of columns(from 2nd to last column). 

### ideal_best_worst
Impact should either be "+" or "-" and should be separated by ",". No. of impacts should also be equal to the no. of columns(from 2nd to last column). It makes two lists: one with ideal best values and the other with ideal worst values corresponding to every column.

### euclidean_distance
It makes two list :
  1) Euclidean distance from ideal best
  2) Euclidean distance from ideal worst
 
### topsis_score and rank
Topsis score is calculated by dividing the ideal_worst_list by the sum of list obtained in fourth step. And according to this rank is calculated and two more columns named 'Topsis Score' and 'Rank'are added into the csv file.



