**Data Cleaning for the Dirty_cafe_Sales.Csv 
**

Preview of the Raw data : 
<img width="1283" alt="image" src="https://github.com/user-attachments/assets/c5e8a377-e81f-4736-82ec-8d33468d5eca" />

**Step taken: **

1. Check for duplicates - No duplicates
2. Remove TXT from the transaction ID - Keep only the useful information that we can use to identify each transaction
   Use the right function to obtain only the transaction number.
<img width="1120" alt="image" src="https://github.com/user-attachments/assets/bcd8cafc-0700-49a3-93ad-4a324dbac9dd" />

3. Fill out Quantity based on the TotalPrice, Price per Item:
   
  - Quantity =  TotalPrice / Price
  - Price = TotalPrice / Quantity
  - TotalPrice = Quantity * Price

4. Fill out the Item based on observing the prices of each item:

- Coffee	2
- Cookie	1
- Juice	3
- Salad	5
- Tea	1.5

5. There are products with the same price :
   - Sandwich - 4
   - Smoothies - 4
   - Juice - 3 
   - Cake - 3
Given this situation, all products with prices 3 and 4 will be classified as N/A.

  



