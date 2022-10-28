# Sharks-Proyecto-28.10.2022
Proyecto segunda semana
## Goals
Get a fully cleaned dataset with at least 6 thousand rows and consistend data types.
# Steps
1. Explore Data and analyse possible issues
2. Erase columns with more than 80 % 
3. Explore columns with null values under threshold and decide course of action
4. Eliminate Duplicate rows
5. Clean Columns
6. Explore constant or low variance columns
7. Outliers
8. Collinearity
9. Upload clean Dataframe

# Actual step results
1. After exploration two columns are clearly not functional to the data set ( Unnamed: 22 , Unnamed: 23  ) we will erase them.
2. After the drop it becomes clear that the frequency of nan starts for all columns at certain row, we have to find that shape, to then decide the amount of rows we can remove
3. Above the high threshold of 21 empty columns per row we drop the corresponding rows the shape of that threshold is (17020, 23), we thus have around 8 thousand rows remaining.



