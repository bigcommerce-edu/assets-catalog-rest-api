# Lab - Complex Rules

### Prerequisites:

* BigCommerce store (sandbox or live)
* Basic knowledge of APIs
* REST client (Postman)
* An existing Postman environment and collection as configured in previous labs

Try the following requests in the "Complex Rules" folder.

### Create Product Modifier

In preparation for the following requests related to complex rules, this request will create a brand new product modifier option.

* **Determine** the ID of the product with the previously created "Donate" modifier option (which should also contain variants).
* **Enter** the product ID for the `:product_id` query param.
* **Observe** the modifier response data.
* **Record** the 

### Create Complex Rule

* **Run** the "Get Product Modifiers" request in the "Variants and Modifiers" folder to retrieve the ID of the "Donate" modifier, as well as the ID of the "Yes" value for that modifier.
* **Enter** the product ID for the `:product_id` query param.
* In the Body tab, **enter** the appropriate modifier and value IDs. The first object in the `conditions` array should have the `modifier_id` corresponding with the "Donate" modifier option and the `modifier_value_id` corresponding with its "Yes" value. The second object should have the `modifier_id` corresponding with the "Receive a sticker" modifier and the `modifier_value_id` corresponding with its "Yes" value.
* **Observe** the complex rule response data.

### Create Complex Rule (Modifier + Variant)

* **Run** the "Get Variants" request in the "Variants and Modifiers" folder to retrieve the ID of a variant. (Make sure this is for the product that also contains a modifier option.)
* **Enter** the product ID for the `:product_id` query param.
* In the Body tab, **enter** the appropriate `variant_id`, as well as the `modifier_id` corresponding with one of the product's modifiers and the `modifier_value_id` corresponding with its "Yes" value.
* **Observe** the complex rule response data.

### Get Complex Rules

* **Enter** the product ID for the `:product_id` query param.
* **Observe** the complex rule response data.
