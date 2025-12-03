# Lab - Variants, Variant Options, and Modifier Options

### Prerequisites

* BigCommerce store (sandbox or live)
* Basic knowledge of APIs
* REST client (Postman)
* An existing Postman environment and collection as configured in previous labs

Try the following requests in the "Variants and Modifiers" folder.

### Create Product

For the subsequent requests dealing with variants and modifiers, this request first creates a new simple product.

* In the store control panel, **identify** the ID of a valid category.
* **Enter** the valid category ID in the Body tab.
* **Verify** that the new product exists in the store control panel.
* **Record** the product ID from the API response for following requests.

### Create Variant Option (Size and Color)

These two requests are pre-configured to create variant options called "Size" and "Color" with appropriate values.

* **Enter** the previously captured product ID for the `:product_id` path variable.
* **Record** the option and value IDs for following requests.

### Get Product Options

* **Enter** the previously captured product ID for the `:product_id` path variable.
* **Observe** the option response data and **verify** that the "Size" and "Color" options exist.

### Create Variant (Large/Medium Red/Blue)

These four requests are pre-configured to create variants for the possible combinations of the "Size" and "Color" options.

* **Enter** the previously captured product ID for the `:product_id` path variable.
* In the Body tab, **enter** appropriate option and value IDs.  Each object in the `option_values` array should have an `option_id` matching the appropriate option (e.g, the "Size" option) and an `id` matching the appropriate value (e.g., the "Large" value).
* **Verify** in the store control panel that the product has the expected variants.

### Get Variants

* **Enter** the previously captured product ID for the `:product_id` path variable.
* **Observe** the variant response data.

### Create Product and Variants

This request will create a new product and all its options/variants in one shot.

* In the store control panel, **identify** the ID of a valid category.
* **Enter** the valid category ID in the Body tab.
* **Verify** that the new product exists in the store control panel with all its variants.
* **Record** the product ID from the API response for following requests.

### Create Product Modifier

* **Enter** the ID of a product that also has variants for the `:product_id` path variable. (Having a product with both variants and a modifier will be important for later labs.)
* **Observe** the modifier response data.
* **Record** the modifier ID and the ID of the "Yes" value from the API response for the following requests.

### Update Product Modifier

* **Enter** the same product ID for the `:product_id` path variable and the modifier option ID for the `:modifier_id` path variable.
* In the Body tab, **enter** the ID of the "Yes" value.
* **Observe** the modifier response data.

### Get Product Modifiers

* **Enter** the same product ID for the `:product_id` path variable
* **Observe** the modifier response data and **verify** that the price adjustment is reflected.
