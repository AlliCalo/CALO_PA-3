# CALO_PA-3




I. Intended Learning Outcomes
At the end of this laboratory activity, the student should be able to:
1. load a CSV dataset into a Pandas DataFrame;
2. select rows and columns using positional and label-based indexing;
3. filter records using conditions on a DataFrame column; and
4. extract a well-defined subset of data without changing the source data.

## DATABASE

<img width="506" height="763" alt="image" src="https://github.com/user-attachments/assets/f9a36f9f-9097-4219-bded-6201c6756540" />



# A. POSITIONAL AND LABEL-BASED SLICING

After loading cars, complete the following operations.
a. Display the shape and complete list of column names of cars.
b. Using positional slicing, create cars_6_to_10  containing rows 6 through 10 of the dataset, where the first data row is row 1.
From cars_6_to_10,  display only the columns Model, mpg, cyl, hp, and gear, in that order.
Requirement: The row selection in part (b) must use iloc; the column selection in part (c) must
use column labels.

## CODE 
<img width="794" height="439" alt="image" src="https://github.com/user-attachments/assets/a1913ced-c838-483b-a560-0c57b6836bd4" />

## EXPLANATION


# B. MODEL LOOKUP

Use Boolean indexing on the Model column to answer both requests.
a. Display the complete row for Toyota Corolla.
b. For Pontiac Firebird, display only Model, mpg, hp, and wt.
Store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to
locate either model.


## CODE 

<img width="642" height="247" alt="image" src="https://github.com/user-attachments/assets/8042790c-d2ec-4fd0-9421-4db7f63d6be7" />

## EXPLANATION 



# C. MULTI-MODEL SUBSETTING

Create a DataFrame named selected
cars containing only the records for three models: Datsun 710,
Lotus Europa, and Ferrari Dino.
For these records, retain only Model, mpg, cyl, hp, and gear. Select the rows by their model values
rather than by row numbers. Display selected
cars and its shape.
Required check: The final DataFrame must contain exactly three rows and five columns


## CODE

<img width="859" height="206" alt="image" src="https://github.com/user-attachments/assets/3017c329-d7d2-4e84-9605-dbfe38ea6bf9" />


## EXPLANATION
















