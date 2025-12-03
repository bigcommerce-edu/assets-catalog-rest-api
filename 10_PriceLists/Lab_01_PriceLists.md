# Lab - Price Lists

### **Prerequisites:**

* BigCommerce store (sandbox or live)
* Basic knowledge of APIs
* REST client (Postman)
* An existing Postman environment and collection as configured in previous labs
* At least one **customer group** created in the store control panel.

Try the following requests in the "Price Lists" folder.

### Create Price List

* **Observe** the price list response data.
* **Record** the ID of the new price list for following requests.

### Assign a Price List

* In the Body tab, **enter** the previously captured price list ID, a valid customer group ID, and a channel ID. (The channel ID can be 1 for the default storefront channel, or you can enter the ID of a different channel if desired.)
* **Observe** the assignment response data.

### Get Price Lists

* **Observe** the price list response data.

### Update Price List

* **Enter** the previously captured price list ID for the `:price_list_id` query param.
* **Observe** the price list response data.

### Price List Record (by Variant/Currency)

* **Run** the "Get Variants" request in the "Variants and Modifiers" folder to retrieve the ID of a valid variant.
* **Enter** the previously captured price list ID for the `:price_list_id` query paramm and the variant ID for the `:variant_id` param.
* If necessary, **replace** the value of the `:currency_code` query param with a valid currency code for your store.
* **Observe** the price response data.

### Get Price List Records

* **Enter** the previously captured price list ID for the `:price_list_id` query param.
* **Observe** the price response data.

### Get Price List Record by Variant

* **Enter** the previously captured price list ID for the `:price_list_id` query param and the previously captured variant ID for the `:variant_id` query param.
* **Observe** the price response data.
