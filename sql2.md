## Business Problem:  
# The marketing team ran a campaign in June 2023 and wants to see how many new customers signed up during that period.    
Fields to Retrieve:  
1.PARTY_ID     
2.FIRST_NAME  
3.LAST_NAME  
4.EMAIL   
5.PHONE  
6.ENTRY_DATE  
## Solution

![Screenshot from 2025-03-08 00-55-03](https://github.com/user-attachments/assets/0ca60422-599f-4566-a932-ab6081fec9e9)


# Approach  
 To retrieve the list of new customers who signed up in June 2023:    
  1. Join PARTY and PERSON – Retrieves basic customer details like ID, first name, and last name.   
  2. Filter by CREATED_DATE – Ensures only customers created within June 2023 are included.  
  3. Join PARTY_ROLE – Filters to include only those with a CUSTOMER role.  
  4. Join PARTY_CONTACT_MECH and CONTACT_MECH – Fetches the email address of each customer.  
  5. Left Join TELECOM_NUMBER – Retrieves the phone number.

# QueryCost- 28436.11

![Screenshot from 2025-03-08 10-14-57](https://github.com/user-attachments/assets/9fe7f587-7b8c-4f83-a4c5-c33bb23083ef)

