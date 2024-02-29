1. age: continuous. It denotes the age of the person.
2. workclass: It denotes the working class of the person. Sample values: Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked.
3. fnlwgt: continuous.
4. education: It denotes the educational qualification of the person. Sample values: Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool.
5. education-num: continuous. It denotes the quantitative values with reference to education.
6. marital-status: It denotes the marital status of the person. Sample values: Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse.
7. occupation: It denotes the occupation of a person. Sample values: Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces.
8. relationship: It denotes the people present in the family. Sample values: Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried.
9. race: It denotes the person’s origins. Sample values: White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other, Black.
10. sex: It denotes the person's gender. Sample values: Female, Male.
11. capital-gain: continuous. It denotes the monitory gains by the person.
12. capital-loss: continuous. It denotes the monitory loss by the person.
13. hours-per-week: continuous. It denotes the number of working hours per week by the person.
14. native-country: It denotes the country to which the person belongs. Sample values: United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands

15. - Open Jupyter Notebook ;
- Imported Neccessory Libraries for after uses ;
- Imported Libraries :
  
  • Pandas
  
  • Numpy
  
  • matplotlib.pyplot
  
  • seaborn
  
  • from sklearn import preprocessing
  
  • from imblearn.over_sampling import SMOTE
  
  • from sklearn.model_selection import train_test_split
  
  • from sklearn.linear_model import LogisticRegression
  
  • from wordcloud import WordCloud 

 
- Read the Income Datasets using pandas library;
- Checked Basic Information about the dataset (shape,info,columns,dtypes,null values,describe);  
- Renamed a column named 'nan' to 'Age' by using rename function ; 
- To Check for any missing values or any symbols printed unique of every Features by using a for loop ;
- There was symbol like '?' in this dataset so we replaced it with null values ;
- Took a sum of null values and visualised null values using heatmap in seaborn library ;
- Then Filled the null values by using ffill (Forward Fill - It replaces the NULL values with the value from the previous row (or previous column, if the axis parameter is set to 'columns' ) )
- Then Checked for duplicated values and found 24 dupicates and dropped those duplicates because it was a small amount of data;



- Then Started to visualise all the features one by one;
- first importing wordloud and plotted the wordcloud for occupation column
- Then plotted count plot. visualization of distribution of income,visualization of Income distribution by education level,visualization of Income distribution by occupuation,visualization of income distrubution by race,visualization of income distrubution by age,visualization of income distrubution by workclass,visualization of income distrubution by education,
- Then plotted data using hist
- Then classified data into two those who have greater than 50k into a variable and those who doesn't have into another ;
- Then plotted both of the data with a feature named 'workclass' using countplot ;
- Then used pie chart.
- Then used catplot and plotted box then found average income with age and also found some outliers ;
- After all the cleaning is done then saved the cleaned dataset into a new csv file;



- Started the Encoding
- First used LabelEncoder instance,( fits it to the provided categories, and then transforms the categories into integers in one line.)
- The datas were imbalanced and to balance the data we used SMOTE technique to create synthetic values ;
- Then Splitted the data for testing and training using train_test_split ;
- Then started to create a model using LogisticRegression ;
- Then predicted the values that have tested and checked accuracy,score,confusion_matrix and so on...;



- Open the cleaned excel file we worked in PowerBi
- Stacked Column Chart - count of income by sex
- Donut Chart - count of income by age,count of income by occupation,count of income by education
- Funnel Chart - count of income of marital-status
- Table - native-country,sex,education,income
- Cards :  Sum of education-num,sum of captial-loss,average of age
- Slicer - Income
