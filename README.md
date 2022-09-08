
EDA OF TITANIC DATASET
![image](https://user-images.githubusercontent.com/111189874/189105855-c5d9ec00-bccd-469e-8161-845c81a3796c.png)








The Titanic or, in full, RMS Titanic was part of the one of the most iconic tragedies of all time. RMS Titanic was a British passenger ship that hit an iceberg while on its voyage from Southampton to New York City, and sank in the North Atlantic ocean, leaving hundreds of passengers to die in the aftermath of the deadly incident. Some of the passengers who survived till help arrived were rescued while many lost their lives helplessly waiting for help to arrive.

This project addresses the following Data Analysis topics:
* Requirements

Python , jupyter notebook.
Numpy, Pandas, seaborn and sklearn library.
Dataset(titanic.csv), added in the repository.

1. Data Exploration and Preparation

2. Data Representation and Transformation

3. Data Visualization and Presentation

4. Data Exploration and Preparation Learn about data: Are there missing data? Is it categorical? if not, min , max, avg values? if yes, what are the categories? distribution of variables Duplicate entry

5. Cabin
Cabin feature is little bit tricky and it needs further exploration. The large portion of the Cabin feature is missing and the feature itself can't be ignored completely because some the cabins might have higher survival rates. It turns out to be the first letter of the Cabin values are the decks in which the cabins are located. Those decks were mainly separated for one passenger class, but some of them were used by multiple passenger classes.
On the Boat Deck there were 6 rooms labeled as T, U, W, X, Y, Z but only the T cabin is present in the dataset
* A, B and C decks were only for 1st class passengers
* D and E decks were for all classes
* F and G decks were for both 2nd and 3rd class passengers
* From going A to G, distance to the staircase increases which might be a factor of survival

6. title
There are 5 classes of name_title, passengers with ‘Miss’, ‘Mrs’, ‘Master’, ‘Mr’ and the fifth class with all the remaining minority of titles like ‘Dr’, ‘Rev’.
* A steep spike in the probability distribution of passengers who did not survive in the 3rd class implies passengers with title ‘Master’ or younger boys had a lesser chance of surviving.

7. first letter in the name
* The most common surnames started with the following letters:
Maximum occurence of letters in surname beginning : [('S', 86), ('M', 74), ('B', 72), ('C', 69), ('H', 69)]

8. Ticket:
* Ticket number refers to the value printed on the ticket (in image above) as provided by the booking agent which could signify the date of booking. (Did not produce good results so not used) 
* We check the significance of the first letters in the ticket number and bin on the basis of that.

9. Family_Size is created by adding SibSp, Parch and 1. SibSp is the count of siblings and spouse, and Parch is the count of parents and children. Those columns are added in order to find the total size of families. Adding 1 at the end, is the current passenger. Graphs have clearly shown that family size is a predictor of survival because different values have different survival rates.

Family Size with 1 are labeled as Alone
Family Size with 2, 3 and 4 are labeled as Small
Family Size with 5 and 6 are labeled as Medium
Family Size with 7, 8 and 11 are labeled as Large
![image](https://user-images.githubusercontent.com/111189874/189106817-73b0ae7b-1e93-4457-be2e-d0fd8bcbdedf.png)

![image](https://user-images.githubusercontent.com/111189874/189106913-e2d19dca-5516-4e08-bc3a-9b41b251f2cf.png)


10. The categorical features (Pclass, Sex, Deck, Embarked, Title) are converted to one-hot encoded features with OneHotEncoder. Age and Fare features are not converted because they are ordinal unlike the previous ones.
![image](https://user-images.githubusercontent.com/111189874/189106132-a4d55293-2b07-42ad-a7f6-415682165cd2.png)


11. Transformation on dataframe: Droping some of the columns which many not contribute much to our machine learning model such as Name, Ticket, Cabin etc

12. Data Visualization and Presentation :
* Sex and Age using bar graph.
* Sex vs age using violin plot.
![image](https://user-images.githubusercontent.com/111189874/189106674-40a893f4-9a08-49d7-8325-3ea2160f0a55.png)

* Survived vs Age vs Pclass using bar plot.
