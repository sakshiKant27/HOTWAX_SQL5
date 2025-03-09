## Payment Captured but Not Shipped  
# Business Problem:    
Finance teams want to ensure revenue is recognized properly. If payment is captured but no shipment has occurred, it warrants further review.    
# Fields to Retrieve:  
    ORDER_ID      
    ORDER_STATUS      
    PAYMENT_STATUS      
    SHIPMENT_STATUS      

# Solution :  
![Screenshot from 2025-03-08 02-17-17](https://github.com/user-attachments/assets/c63a92c2-7a03-477e-93f2-e2d71bb99901)

#
1.Retrieves order details along with their payment and shipment statuses.  
2.Joins order_payment_preference (opp) to get the payment status for each order.  
3.Joins order_shipment (os) and shipment (s) to fetch the shipment status.  
4.Filters orders where:  
    The shipment is not yet shipped (s.status_id != 'SHIPMENT_SHIPPED'),   
    The shipment status is NULL (indicating no shipment yet), AND  
    The payment is settled (opp.status_id = 'PAYMENT_SETTLED').  

# Query Cost -60840.84

![Screenshot from 2025-03-08 10-40-49](https://github.com/user-attachments/assets/d8680f53-13f4-41a6-9d19-b2a31fe48441)



    
