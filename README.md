# Pandas1

## 1 Problem 1 : Make a Pandas DataFrame with two-dimensional list	(	https://www.geeksforgeeks.org/make-a-pandas-dataframe-with-two-dimensional-list-python/)
<br>
data=  [['Geek1', 'Reacher', 25],
['Geek2', 'Pete', 30]]
columns=['FName', 'LName', 'Age']
df=pd.DataFrame(data, columns=columns)
print(df)

## 2 Problem 2 :Big Countries	(	https://leetcode.com/problems/big-countries/ )
<br>
import pandas as pd

def big_countries(world: pd.DataFrame) -> pd.DataFrame:
    df=world[(world['population']>=25000000) | (world['area']>=3000000)]
    return df[['name', 'population', 'area']]

## 3 Problem 3 :Recyclable and Low Fat Products	(	https://leetcode.com/problems/recyclable-and-low-fat-products/ )
<br>

import pandas as pd

def find_products(products: pd.DataFrame) -> pd.DataFrame:
    df=products[(products['low_fats']=='Y') & (products['recyclable']=='Y')]
    return df[['product_id']]


## 4 Problem 4 :Customer Who Never Order	(	https://leetcode.com/problems/customers-who-never-order/  )
<br>
import pandas as pd

def find_customers(customers: pd.DataFrame, orders: pd.DataFrame) -> pd.DataFrame:
    df=customers[~(customers['id']).isin(orders['customerId'])]
    return df[['name']].rename(columns={'name': 'Customers'})

