<h2><p font-size="18pt" color="Red" align="center"> Data Cleaning for the Dirty_cafe_Sales.Csv</p></h2>
<hr>

Preview of the Raw data : 
<img width="1283" alt="image" src="https://github.com/user-attachments/assets/c5e8a377-e81f-4736-82ec-8d33468d5eca" />

Sheet dirty_cafe_sales - RAW Contains 
<table>
   <th>Columns</th>
   <tr>Transaction ID</tr>
   <tr>Items</tr>
   <tr>Price Per Unit</tr>
   <tr>Total Spend</tr>
   <tr>Payment Method</tr>
   <tr>Location</tr>
   <tr>Transaction Date</tr>
</table>

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

5. With PowerQuery, transform the date into 3 parts: day, month, and year. 

6. There are products with the same price :
   - Sandwich - 4
   - Smoothies - 4
   - Juice - 3 
   - Cake - 3
Given this situation, all products with prices 3 and 4 will be classified as N/A.

![alt text](image.png) 

7. Remove all unnecessary data that has missing information:

- Remove rows with N/A -  Replace all UNKNOWN , ERROR WITH N/A 
- Remove rows with EMTPY Quantity, ITEM NAME, AND PRICE 
- Remote rows with N/A ,ITEM NAME, NO QUANTY, NO TOTAL, ONLY PRICE PER ITEM

