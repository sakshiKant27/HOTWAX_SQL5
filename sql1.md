### 1.Newly Created Sales Orders and Payment Methods
 Business Problem:​Finance teams need to see new orders and their payment methods for reconciliation and fraud checks.<br>
Fields to Retrieve:   
●​ ORDER_ID    
●​ TOTAL_AMOUNT    
●​ PAYMENT_METHOD    
●​ Shopify Order ID (if applicable)<br>


  # Solution-
 ![Screenshot from 2025-03-08 00-44-44](https://github.com/user-attachments/assets/b4fba2bb-20d0-42de-82cf-028c5b352a84)


# Query Explanation 
Retrieves order details (order_id, TotalAmount, PaymentMethod, Shopify_Order_Id).<br>
Joins Order_Header with order_payment_preference on order_id.<br>
Filters orders that are newly created (ORDER_CREATED) and of type sales order (SALES_ORDER).<br>

# QueryCost-3100.78  (43 rows returned)
![Screenshot from 2025-03-08 10-11-58](https://github.com/user-attachments/assets/40da4531-0ab2-46a2-b197-42c37ced01fc)



