# ecommerse-site-data-analysis
requirement- python 3.8
packages- pandas
texteditor- jupyter notebook


How to import pandas->
import pandas as pd


pass csv file into pandas->
df=pd.read_csv("test.csv")

visualization tool used- Power bi

 Tasks:
 
![image](https://user-images.githubusercontent.com/61740462/160233788-6b652a40-4fec-4465-a50e-1dfaa1439179.png)

1.Products without prices- df = data[data['price_string'].isnull()]
2.Count of products without prices and with prices in each Product Type-arr = dff.product_type.unique()
for each in arr:
    print(dff['product_type'].value_counts())
    
 Category-arr = dff.product_type.unique()
for each in arr:
    print(dff['category'].value_counts())
    
 Level 1-arr = dff.product_type.unique()
for each in arr:
    print(dff['level_1'].value_counts()
    
3.Correct Product Prices in the correct format (eg: $56) wherever possible and separate them into currency and value column -
 1.dff.price_string = dff.price_string.replace({'\$':''}, regex = True)
 2. dff['price_string'] = '$' + dff['price_string'].astype(str)

4.List out the categories with average price of product.- dff.groupby('category')['price_string'].mean()




