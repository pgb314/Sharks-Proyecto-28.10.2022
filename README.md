# Sharks-Proyecto-28.10.2022
Proyecto segunda semana
## Goals
Get a fully cleaned dataset with at least 6 thousand rows and consistend data types.
# Objective
Average Age of non-fatal/fatal shark attacks

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
# Objective
Average Age of non-fatal/fatal shark attacks

# Actual step results
1. After exploration two columns are clearly not functional to the data set ( Unnamed: 22 , Unnamed: 23  ) we will erase them.

![Null Graph 1 (pre-cleaning)](https://user-images.githubusercontent.com/114666478/198870742-686ada21-b971-4f10-b939-74fbc77dcabf.png)

2. After the drop, it becomes clear that the frequency of nan starts for all columns at  a certain row, we have to find that shape, to then decide the amount of rows we can remove
3. Above the high threshold of  equal more than 20 empty columns per row we drop the corresponding rows the shape of that threshold is (19414, 23) , we thus have around 6.3 thousand rows remaining.

![Null Graph 2](https://user-images.githubusercontent.com/114666478/198870797-14916828-9b46-40b1-b3b6-8e0ee81bd99a.png)


4. Clear up name inconsistencies, by removing spaces and any special symbols
5. All nan values in country are replaced by unknowns
6. All nan values in Object columns ('Type', 'Activity','Name','Sex','Age','Time','Fatal_bin','Species','Location','Area','Injury') are replaced by unknowns

![Null Graph 3](https://user-images.githubusercontent.com/114666478/198870807-80827486-96b6-4c4a-9632-4ae1ef638921.png)


7. Clean Type by substituting Boat and Boatomg by Boating
8. Creating a new mean age column by creating a def that looks for keywords and returns the corresponding value and looks for numbers and adds the mean value to the column
![Mean age code](https://user-images.githubusercontent.com/114666478/198870908-0ecfe4a3-d9fd-4f56-908c-74e0bc254d89.PNG)


9. Standardize Case Number
10. Clean any incongruences up in the Fatality column
11. Clean any incongruences up in the Sex column
12. Clean any incongruences up in the Case Number Column
13. Attempt to clear up Species by grouping by keyword, searching for subgroups and attributing keywword to main term. All invalid rows are removed due to them being cases of non shark attacks
14. Fill Year nulls with the corresponding year from the CaseNumber
15. Create Graph for Total Attacks,for deadly attacks and for non fatal attack, also create visualization for all three
# All Attacks
![First Distribution of Attacks](https://user-images.githubusercontent.com/114666478/198870934-2f1caf1d-2b31-4f59-be27-932f7320d8b7.png)
# Deadly Attacks
![Distribution of deadly Attacks](https://user-images.githubusercontent.com/114666478/198870969-24c5f45b-e3e2-4f04-b7f6-bf3945b9bd25.png)
# Non Deadly Attacks
![Distribution of non deadly attacks](https://user-images.githubusercontent.com/114666478/198871010-c5263a18-f67e-4ee8-b3c7-3de081dbe139.png)

16. Calculate stats for all three categories 
17. Sort by genders and calculate both the Total and Fatal mean ages for both genders, and the count


