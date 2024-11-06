#pandas cmds for cleaning data

To read a file from the system -
pd.read_csv(r" Copy the Path of the CSV file")

To read a file in specific Data Frame-
df pd.read_csv(r" Copy the Path of the CSV file")
df


Filtering and Ordering:

To get the inoformation from the data-
df.info()


To display the info of the file-
df.info()


To display the last number of rows-
df2.tail(number)


To display the first few rows-
df2.head(number)


To display all the columns in the given file-
df.columns


To ddisplay what are the columns needed from the original data-
df = df [['column_name', 'column_name']]
df


To drop the columns-
new_data_frame = df.drop(columns = ['column_name'])
new_data_frame


To display the single volume data of a column-
df["column_name"][number]


To display the rows of a df -
pd.set_option('display.max.rows', enter the no of rows)


Setting one of the column as Index-
df.set_index('Column Name')
df


To Rename the columns-
df_new_column_names = []
for i in df1.columns:
    df_new_column_names.append(i.capitalize())
print(df1_new_column_names) 


To find the duplicate values-
df.duplicated().sum()


To display count of duplicate values of columns- 
df.isna().sum()


To find if we have null values once data is cleaned-
df1.isna().sum().sum()


Using filter can display particular data of the columns-
df.filter(items = ['Column Name', 'Column Name'])


Here by using LIKE we can filter specific data from the column -
df.filter(like = 'Any specific data name', axis=0)


Sorting a df of particular column
df[df['Column Name'] <10].sort_values(by='Column Name')   // df[df['Rank'] <10].sort_values(by=['Continent', 'Country'], ascending = False)]]



Using replace() to change the data in a specific column-
df1["column_name"].str.replace("$","").str.replace(".","")



Using apply() method - if a column has true or false values to convert them into binary as 1/0- 
df["column_name"] = df1["column_name"].apply(lambda x:1 if x == True else 0)


Using round() to round off a values for particular columns-
df1["Product_price"].apply(lambda x:round(x))
