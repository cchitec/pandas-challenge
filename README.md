# pandas-challenge

 Analyze the data for the fantasy game Heroes of Pymoli:
 
 In order to work on project ensure to import the correct dependecies
 Determine the correct file path for pandas to retrieve data.
 Using pd.DataFrame convert the files to a Pandas DataFrame

PLAYER COUNT
Using the .groupby() function, focus on the 'SN' column to determine the total number of players

PURCHASING ANALYSIS (Total)
    Determine the number of unique items using the unique function
        len(pd.unique(purchase_data_df['Item Name']))
    Determine the average price using the mean function focusing on the price column
        purchase_data_df["Price"].mean()
    Determine the total number of purchases using groupby() function looking through the purchasing column with a focus on the SN column for a proper output
        len(purchase_data_df.groupby("Purchase ID")["SN"].count())
    Determine the total revenue using the sum function focusing on the price column
        purchase_data_df["Price"].sum()
