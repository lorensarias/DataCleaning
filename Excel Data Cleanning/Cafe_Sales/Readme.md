<h2><p font-size="18pt" color="Red" align="center"> Data Cleaning for the Dirty_cafe_Sales.Csv</p></h2>
<hr>

Preview of the Raw data : 
<img width="1283" alt="image" src="https://github.com/user-attachments/assets/c5e8a377-e81f-4736-82ec-8d33468d5eca" />

<B>Sheet dirty_cafe_sales - RAW Contains : </B>
</br>
<ul>
  <li>Transaction ID</li>
  <li>Items</li>
  <li>Price Per Unit</li>
  <li>Total Spend</li>
  <li>Payment Method</li>
  <li>Location</li>
  <li>Transaction Date</li>
</ul>

<h2>**Step taken: **</h2>

1. Duplicate the raw File  - dirty_cafe_sales_1.xls -- This will be our working file
2. Check for duplicates - No duplicates
3. Remove TXT from the transaction ID - Keep only the useful information that we can use to identify each transaction
   Use the right function to obtain only the transaction number.
<img width="1120" alt="image" src="https://github.com/user-attachments/assets/bcd8cafc-0700-49a3-93ad-4a324dbac9dd" />

4. Fill out Quantity based on the TotalPrice, Price per Item:
   
  - Quantity =  TotalPrice / Price
  - Price = TotalPrice / Quantity
  - TotalPrice = Quantity * Price

5. Fill out the Item based on observing the prices of each item:

- Coffee	2
- Cookie	1
- Juice	3
- Salad	5
- Tea	1.5

6. With PowerQuery, transform the date into 3 parts: day, month, and year. 

7. There are products with the same price :
   - Sandwich - 4
   - Smoothies - 4
   - Juice - 3 
   - Cake - 3
Given this situation, all products with prices 3 and 4 will be classified as N/A.

8. Remove all unnecessary data that has missing information:

- Remove rows with N/A -  Replace all UNKNOWN , ERROR WITH N/A 
- Remove rows with EMTPY Quantity, ITEM NAME, AND PRICE 
- Remote rows with N/A, ITEM NAME, NO QUANTY, NO TOTAL, ONLY PRICE PER ITEM
</hr>

<h2 aling="center">**Findings**</h2>

<p> - Bar Chart that shows the sales and number of items sold during 2023. Salads were the items that were sold the most and it the number of items sold was 3815.</p>
<img width="778" alt="image" src="https://github.com/user-attachments/assets/0ccc3d73-2c41-4007-bfc0-27c29bdc0cb3" />
</br>
<p> - Line Chart that shows months with the highest sales and lower sales. This can help the business to identify which months may need deals to bring more customers. This also shows how the sale fluctuates over the year. </p>
<img width="926" alt="image" src="https://github.com/user-attachments/assets/a6a27e4a-d69d-48d9-b2bd-42ba0d14fdf0" />
</br>
<p> - Line Chart that shows the top 3 products that sold the most in 2023. </p>
<img width="1251" alt="image" src="https://github.com/user-attachments/assets/9e27ca3b-e8b9-428c-b7f4-02e5d00dd16e" />
</br>
<p> - Line Chart that shows the 3 Items with the lower sales during 2023 , including N/A </p>
<img width="1208" alt="image" src="https://github.com/user-attachments/assets/8435bc5d-14ae-411b-82fa-6dd365c49e4e" />
</br>
<p> - Line Chart and Pie Chart that shows the Payment method and the number of transactions done during 2023. It also shows the percentages of payment methods classified as N/A for missing or unknown data. </p>
<img width="479" alt="image" src="https://github.com/user-attachments/assets/b12dcba7-2341-44af-ad4e-23428706fa06" />

<img width="471" alt="image" src="https://github.com/user-attachments/assets/e63828f8-6c08-435d-a02d-5dad2e861c54" />


