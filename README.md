# pandas-challenge

 Analyze the data for the fantasy game Heroes of Pymoli:
 
 In order to work on project ensure to import the correct dependecies
 Determine the correct file path for pandas to retrieve data.
 Using pd.DataFrame convert the files to a Pandas DataFrame

PLAYER COUNT

    Using the .loc() function, focus on the 'Gender','Age','SN' columns to determine the total number of players and using the .drop.duplicates function to clean the data set

PURCHASING ANALYSIS (Total)

    Determine the number of unique items using the unique function
        len(pd.unique(purchase_data_df['Item Name']))
    Determine the average price using the mean function focusing on the price column
        purchase_data_df["Price"].mean()
    Determine the total number of purchases using groupby() function looking through the purchasing column with a focus on the SN column for a proper output
        len(purchase_data_df.groupby("Purchase ID")["SN"].count())
    Determine the total revenue using the sum function focusing on the price column
        purchase_data_df["Price"].sum()

GENDER DEMOGRAPHICS
    
    In order to determine the total number of players in my data set I used the .value_counts() while simultaneously getting rid of my duplicates to get a more accurate output. I focused on "Gender" and "SN" to clean out the data set with the following equation
        total= purchase_data[["Gender", "SN"]].drop_duplicates().Gender.value_counts()
    Using the same data parameters and dropping duplicates I changed the format of my output to give me a percent value for my table

PURCHASING GENDER ANALYSIS

    Inorder to determine the purchase count I used .value counts() with a focus on "Gender"
    Inorder to get the average purchase price the .groupby() function was used finding the mean of the "Price" column and renaming the column
    For total revenue per gender, I applied the same code with the change of deriving the sum of the "Price" column
    Taking the previously calculated total revenue an purchase count I divided them to get an average price per person per gender
    
AGE DEMOGRAPHICS

    Created a variable for the bins and labesl then use pd.cut to categorize the existing players.
