# Lab - Bulk Pricing Rules

### Prerequisites:

* BigCommerce store (sandbox or live)
* Basic knowledge of APIs
* REST client (Postman)
* An existing Postman environment and collection as configured in previous labs

Try the following requests in the "Bulk Pricing" folder.

### Add Bulk Pricing (Fixed amount off)

* **Enter** a valid product ID for the `:product_id` query param.
* **Record** the ID of the bulk pricing rule from the API response, for the following requests.
* **Verify** in the store control panel that the bulk pricing tier has been applied to the product.

### Get Bulk Pricing

* **Enter** the same product ID for the `:product_id` query param.
* **Observe** the bulk pricing response data.

### Update Bulk Pricing

* **Enter** the same product ID for the `:product_id` query param and the previously captured bulk pricing rule ID for the `:rule_id` query param.
* **Verify** in the store control panel that the quantity threshold of the bulk pricing rule has been updated accordingly.
