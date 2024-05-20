DBMS deadline : 5

Explaination:

The provided code is a Python script for a simple gift store management system. It includes functionalities for customers, vendors, and administrators to interact with the system.

Here's a breakdown of the script:

Imports: The script imports necessary modules such as datetime, time, and mysql.connector for database connectivity.

Database Connection: It establishes a connection to a MySQL database named "GIFTSTORE" with the provided credentials.

Functions:

view_orders: Displays orders for a given customer ID.
view_products: Displays all products available in the store.
filter_by_name: Filters products by name.
filter_by_rating: Filters products by rating.
filter_by_price: Filters products by price.
filter_by_refundable: Filters products by refundable status.
main_menu: Displays the main menu options.
customer_menu: Displays the customer menu options.
add_to_cart: Adds a product to the customer's cart.
view_cart: Displays the contents of the customer's cart.
remove_from_cart: Removes a product from the customer's cart.
manage_wallet: Allows the customer to manage their wallet balance.
view_profile: Displays the customer's profile information.
customer_login: Handles customer login functionality.
filter_menu: Displays filter options for product search.
view_wallet: Displays the customer's wallet balance.
add_money_to_wallet: Allows the customer to add money to their wallet.
add_product: Allows vendors to add new products to the store.
vendor_login: Handles vendor login functionality.
buy_from_cart: Allows the customer to buy products from their cart.
customer_signup: Allows customers to sign up for a new account.
Execution Logic:

The main_menu function is the entry point of the script. It displays options for customers, vendors, and administrators.
Depending on the chosen option, the script navigates to the respective menu or functionality.
Error Handling:

The script includes error handling for database operations, user input validation, and login attempts.
It also implements a locking mechanism for banning users who exceed login attempt limits.



triggers:

trigger: 1

This trigger is defined to execute after each insert operation on the person table (AFTER INSERT ON person).
It checks if the inserted email is invalid (does not contain '@').
If the email is invalid and has been inserted more than three times, it updates the banned column of the corresponding customer to 1, indicating that they are banned.
In the context of the customer_signup() function, after the insert operation is performed on the person table, this trigger would automatically execute and enforce the ban if necessary.

trigger: 2

This triggers checks if the insufficient_balance_count exceeds 3, indicating multiple insufficient balance attempts.
If the count exceeds 3, it proceeds to ban the account for 30 seconds.
The account ban is implemented using a table called LockedUsers, which presumably stores email addresses and the time until which they are banned.
When an account is banned, an entry is inserted into the LockedUsers table with the email address and the time until which the ban lasts.
The script then waits for 30 seconds to enforce the ban.
After the ban period elapses, the entry for the banned email is deleted from the LockedUsers table, effectively lifting the ban.
Finally, the insufficient_balance_count is reset to 0 after the ban is lifted.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Contribution:
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


Pritam Mitthal(2022373) - All worked equally.
Kshitij Sah(2022256) - All worked equally.
Sachin Maurya(2022424) - All worked equally.
Sarthak singh(2022457) - All worked equally.


