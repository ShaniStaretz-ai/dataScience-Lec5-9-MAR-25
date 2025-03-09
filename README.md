# dataScience-Lec5-9-MAR-25
Pandas
* add operator in Series:pd_1.add(pd_2, fill_value) -100+200
  * if there is a match by keys,add the values
  * else add NAN or fill_value to the value.
  * if not the same dtype, through exception
* dataFrame= 2d, size mutable data structure with labelled (rows and columns)
  * **can be considered as a list of Series with the same keys.**
  * create dataFrame:
    * example1:
    ```
    data=np.random.randint(1-101,(4,3))
    df=pd.DataFrame(data)
    print type(df)= DataFrame
    print df= prints as 2d array with inedexes ((0-len-1),(0-len-1))
    ```
    * example2:
    ```
    full_index=pd.DataFrame(data,index=my_rows,columns=my_cols
    ```
    ** my_rows and my_cols will replace the indexes of the 2d structure
    * must be same sizes of the data
    * access row:
      * full_index.loc['CA'],loc['NY':'AZ']= return Series with index value 'CA'
      * full_index.iloc[1],iloc[1:3],[::-1]= return Series with location 1
      ![img.png](img.png)
    * access column: 
      ```
      full_index['Jan']= return as a Series
      full_index[['Jan']]= return as a dataframe
      full_index[['Jan','Feb']]= return as a dataframe
      full_index.iloc[:]= return all dataframe
      full_index[:,1:3]= return dataframe with columns 1-3
      ```