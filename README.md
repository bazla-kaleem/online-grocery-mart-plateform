# online-grocery-mart-plateform
A Database (MYSQL) project and DSA (data structure and algorithm) project in C++language


###  Customer Module
* **Secure Signup & Login:** Supports user registration with password validation requiring a minimum of 6 characters, at least 1 digit, and 1 uppercase letter.
* **Categorized Browsing:** Customers can navigate through 12 predefined categories ranging from Electronics and Clothing to Bakery Items and Fresh Produce.
* **Flexible Cart Additions:** Items can be added to the shopping cart using three distinct input modes:
  1. **Single Item:** By entering the exact product name.
  2. **Multiple Items:** Bulk adding via parsed string commands (e.g., `Keyboard 2, Mouse 3`).
  3. **By Index:** A safer, mistake-proof numerical selection method.
* **Real-time Checkout:** Dynamically calculates itemized subtotals, keeps track of adjusted quantities, and summarizes the final grand total before processing delivery and payment information.

### 🛠️ Admin Control Panel
* **Secure Administrative Access:** Protected by dedicated admin credentials[cite: 1].
* **Inventory Monitoring:** Full visibility to track stock limits and active pricing across the entire store[cite: 1].
* **Dynamic Product Updates:** Administrative privileges to inject new products (up to a maximum of 10 items per category), modify prices, and restock or mark products as out-of-stock[cite: 1].
* **Global Order Reports:** A central dashboard to review user purchase history, total amounts spent, and detailed shipping/payment information[cite: 1].

---

## Data Structures Implemented

To ensure optimal performance and standard design principles, the following structures were used:

* **Singly Linked List (`ItemNode` & `Category`):** Used to dynamically manage individual products within each category This keeps memory allocation fluid and enforces a strict structural cap of 10 items per category.
* **Hash Map (`std::unordered_map`):** Implemented for managing user accounts, facilitating $O(1)$ constant-time lookups during the login and registration processes
* **Balanced Map (`std::map`):** Leveraged for the customer shopping cart to automatically sort and maintain a unique list of selected products mapped to their quantities and base costs
* **Dynamic Array (`std::vector`):** Utilized to sequentially log successful orders and pass active category references efficiently throughout the application runtime
