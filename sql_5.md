## Canceled Orders (Last Month)  
# Business Problem:
The merchandising team needs to know how many orders were canceled in the previous month and their reasons.  
# Fields to Retrieve:  
    TOTAL ORDERS  
    CANCELATION REASON  

# Solution:
![Screenshot from 2025-03-08 10-49-31](https://github.com/user-attachments/assets/39ad55de-cfe8-4fd8-865d-fb2c5fd5d983)  



# Query Explanation  
   1. Fetches canceled orders from the order_status table.  
   2. Filters orders from the previous month using DATE_FORMAT and CURDATE().     
   3. Counts total canceled orders using COUNT(order_id).  
   4. Groups results by cancellation reason (CHANGE_REASON).

# Query Cost- 11984.00  
![Screenshot from 2025-03-08 10-47-27](https://github.com/user-attachments/assets/abcf8de0-4268-4891-b5b5-a7b58729f3a0)



