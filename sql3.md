## Orders from New York  
# Business Problem:  
 Companies often want region-specific analysis to plan local marketing, staffing, or promotions in certain areas—here, specifically, New York.  
 # Fields to Retrieve:  
   1. ORDER_ID  
   2. CUSTOMER_NAME  
   3. STREET_ADDRESS (or shipping address detail)  
   4. CITY  
   5. STATE_PROVINCE    
   6. POSTAL_CODE    
   7. TOTAL_AMOUNT    
   8. ORDER_DATE    
   9. ORDER_STATUS    
 
# Solution:
![Screenshot from 2025-03-08 01-49-14](https://github.com/user-attachments/assets/4d9055c9-d8fd-4754-817d-e70009911b1b)

 

#Query Explanation  
1.Retrieves order details, customer name, and shipping address for orders shipped to New York (NY).  
2.Joins order_contact_mech to get the shipping location (SHIPPING_LOCATION).  
3.Joins party_contact_mech to link the shipping address to the customer.  
4.Joins postal_address to fetch street, city, state, and postal code.  
5.Joins person to retrieve customer's first and last name.  
6.Filters only New York orders using pa.state_province_geo_id = 'NY'.  

