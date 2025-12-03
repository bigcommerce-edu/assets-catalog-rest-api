# Lab - Brands and Categories

### Prerequisites:

* BigCommerce store (sandbox or live)
* Basic knowledge of APIs
* REST client (Postman)
* An existing Postman environment and collection as configured in previous labs

Try the following requests in the "Brands and Categories" folder.

### Create Brand

* **Observe** the brand response data.
* **Record** the brand ID from the API response for the following requests.

### Update Product (Brand)

Use this request to assign a product to a brand. This is an "update product" request modifying only the brand assignment.

* **Enter** a valid product ID for the `:product_id` query param.
* In the Body tab, **enter** the previously captured brand ID.
* **Verify** in the store control panel that the product is assigned to the brand.

### Get Brands

* **Observe** the brand response data.

### Get Category Trees

* **Observe** the tree response data.
* **Record** the ID of the category tree corresponding with the desired storefront channel.

### Create Category

* If necessary, **change** `tree_id` in the Body tab to reflect the appropriate category tree ID.
* **Rrecord** the category ID for the following requests.
* **Verify** in the control panel that the new category exists.

### Update Category

* In the Body tab, **enter** the previously captured category ID.
* **Observe** the category response data and **verify** the updates are reflected.

### Update Product (Category)

Use this request to assign a product to a category. This is an "update product" request modifying only the category assignments.

* **Enter** a valid product ID for the `:product_id` query param.
* In the Body tab, **enter** the previously captured category ID.
* **Verify** in the store control panel that the product is assigned to the category.
