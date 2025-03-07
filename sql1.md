### 1.Newly Created Sales Orders and Payment Methods
 Business Problem:​Finance teams need to see new orders and their payment methods for
 reconciliation and fraud checks.
Fields to Retrieve:
●​ ORDER_ID●​ TOTAL_AMOUNT
●​ PAYMENT_METHOD
●​ Shopify Order ID (if applicable)

  # Solution-
  select oh.order_id,
       oh.grand_total AS TotalAmount,
       opp.payment_method_type_id AS PaymentMethod,
       oh.external_id AS Shopify_Order_Id
       from Order_Header oh
      JOIN order_payment_preference opp on opp.order_id = oh.order_id
      where oh.status_id = 'ORDER_CREATED' and oh.order_type_id='SALES_ORDER';

# Query Explanation 
Retrieves order details (order_id, TotalAmount, PaymentMethod, Shopify_Order_Id).
Joins Order_Header with order_payment_preference on order_id.
Filters orders that are newly created (ORDER_CREATED) and of type sales order (SALES_ORDER).
