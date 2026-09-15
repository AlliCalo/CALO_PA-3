# CALO_PA-3
This repository shows the use and function of panda in python. And sample problems are also provided for our Programming Assignment 3 in ECE2112



# I. Intended Learning Outcomes
At the end of this laboratory activity, the student should be able to:
1. load a CSV dataset into a Pandas DataFrame;
2. select rows and columns using positional and label-based indexing;
3. filter records using conditions on a DataFrame column; and
4. extract a well-defined subset of data without changing the source data.

# DATABASE

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

This code filters a Pandas DataFrame named ⁠cars⁠ in two steps to isolate specific rows and columns.

First, ⁠cars.iloc[5:10]⁠ extracts rows 6 through 10 (indices 5 to 9), utilizing Python’s zero-based indexing and exclusive upper bound. Storing this slice in ⁠cars_6_to_10⁠ and displaying it outputs those five records with all original columns intact.

Second, ⁠cars_6_to_10[['Model', 'mpg', 'cyl', 'hp', 'gear']]⁠ narrows the data by selecting only five specific attributes: car model, fuel efficiency, cylinder count, horsepower, and forward gears. The final display shows the same five vehicles in a clean, focused table stripped of extraneous metrics.

# B. MODEL LOOKUP

Use Boolean indexing on the Model column to answer both requests.
a. Display the complete row for Toyota Corolla.
b. For Pontiac Firebird, display only Model, mpg, hp, and wt.
Store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to
locate either model.


## CODE 

<img width="642" height="247" alt="image" src="https://github.com/user-attachments/assets/8042790c-d2ec-4fd0-9421-4db7f63d6be7" />

## EXPLANATION 

This code uses Pandas' ⁠.loc⁠ indexer to query vehicle records dynamically through boolean conditions rather than hard-coded row positions.

First, ⁠cars['Model'] == 'Toyota Corolla'⁠ matches the target model by value, retrieving its complete row across all attributes via the ⁠:⁠ column selector. Next, the script applies the same conditional logic to locate the ⁠'Pontiac Firebird'⁠, but supplies a list of column names—⁠['Model', 'mpg', 'hp', 'wt']⁠—instead of the full column slice. This dual-axis filtering extracts the exact vehicle and its four specified metrics in a single operation.


# C. MULTI-MODEL SUBSETTING

Create a DataFrame named selected
cars containing only the records for three models: Datsun 710,
Lotus Europa, and Ferrari Dino.
For these records, retain only Model, mpg, cyl, hp, and gear. Select the rows by their model values
rather than by row numbers. Display selected
cars and its shape.
Required check: The final DataFrame must contain exactly three rows and five columns


## CODE

<img width="891" height="210" alt="image" src="https://github.com/user-attachments/assets/0018a0de-b6a2-4153-99c3-70b77ca62ee1" />



## EXPLANATION

The code extracts three target car models Datsun 710, Lotus Europa, and Ferrari Dino, along with five specific attributes, but it fails to meet two core instructions.

First, it relies using ⁠cars.loc[[2, 27, 29]]⁠ instead of querying the ⁠Model⁠ column dynamically with ⁠.isin()⁠. Selecting the object via ⁠pd.DataFrame(...)⁠ to filter columns is also redundant. Second, the code checks ⁠selected_cars.size⁠, which returns the total cell count at 15, rather than ⁠selected_cars.shape⁠ to confirm the required (3, 5) row-and-column dimensions. While the printed table visually matches the goal, the implementation violates the prompt's explicit constraints.














