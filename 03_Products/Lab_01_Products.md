# Lab - Working with Products

### Prerequisites

* BigCommerce store (sandbox or live)
* Basic knowledge of APIs
* REST client (Postman)
* An existing Postman environment and collection as configured in previous labs

Try the following requests in the "Products Basics" folder.

### Create Simple Product

* In the store control panel, **identify** the ID of a valid category.
* **Enter** the valid category ID in the Body tab.
* **Verify** that the new product exists in the store control panel.
* **Record** the product ID from the API response for following requests.

### Get All Products

* **Observe** the product response data.
* **Try out** using the `include` query param to add variants or images to the response data.
* **Try out** using the `include_fields` query param to specify which fields should be returned.
* **Try out** using the `exclude_fields` query param to specify fields that should _not_ be returned.
* **Try out** pagination using the `limit` and `page` query params.
* **Try out** using the `name` query param to filter based on a product name.

### Get Product Channel Assignments

* **Observe** the product/channel response data.

### Update Product

* **Enter** the previously captured product ID for the `:product_id` path variable.
* **Verify** in the store control panel that the product data is updated.

### Delete Product

* **Enter** the previously captured product ID for the `:product_id` path variable.
* **Verify** in the store control panel that the product has been deleted.


