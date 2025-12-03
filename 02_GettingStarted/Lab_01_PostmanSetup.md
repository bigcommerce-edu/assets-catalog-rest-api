# Lab - API Account and Postman Setup

**Duration:** 30 minutes

In order to work with Catalog API, you must have a proper setup in Postman (or another REST client). This lab will walk you through the steps needed to activate a free Postman account, create an OAuth token for your storefront, and correctly set up an environment in Postman. 

### Prerequisites

* A BigCommerce [sandbox store](https://developer.bigcommerce.com/docs/start/about/sandboxes) or [trial store](https://www.bigcommerce.com/essentials/), or a full production store
* Basic knowledge of APIs
* [Postman](https://www.postman.com/) or a similar API client
* Access to a user account with Store Owner permissions


### In this lab, you will:

* Install Postman
* Create an OAuth token from your sandbox store's control panel
* Create a preset for request headers
* Create an environment in Postman for your sandbox store


## Getting Started with Postman

### Create a Postman Account

1. **Navigate** to [postman.com](https://www.postman.com/)
2. **Click** _Sign up for Free_
3. **Fill out** the form provided


## Create an OAuth Token

1. **Login** to your sandbox store
    <Callout type="info">
    Make sure you are logging in using the user account with Store Owner permissions. For more information, see the [Store API Accounts](https://support.bigcommerce.com/s/article/Store-API-Accounts) article in the support portal.
    </Callout>

2. **Navigate** to Settings > Store-level API Accounts
3. **Click** the Create API Account button
4. **Select** &quot;V2/V3 API token&quot; as the Token Type
5. **Type** a name for the API account
6. **Copy** the store hash from the API path
    <Callout type="info">
    The store hash is the alphanumeric string in the **API path** between /stores/ and /v3/. This string uniquely identifies this store when sending requests to `https://api.bigcommerce.com/`

    **Example:**  
    API Path: `https://api.bigcommerce.com/stores/abcd1234/v3/`  
    Store Hash: abcd1234

    The store hash can also be found in your **Control Panel URL**. 

    **Example:**  
    Control Panel URL: `https://store-abcd1234.mybigcommerce.com/`  
    Store Hash: abcd1234
    </Callout>

7. **Save** the store hash somewhere that you can access to complete later steps in this lab activity
8. **Configure** OAuth scopes by making the adjustments below: under Products, **click** the modify button
9. **Click** the Save button
10. **Copy** the Access Token and store it in a place you can access later

A .txt file containing the same credentials will (on most browsers) automatically download to your computer.

There is no way to re-display this pop-up after you select Done to dismiss it. So make sure you store your credentials &ndash; either by copying/pasting the contents of each field out of the pop-up, or by keeping the downloaded .txt file. Otherwise, you will need to repeat all the above steps to generate new credentials. 

From a security perspective, these credentials are sensitive &ndash; please treat them with the same caution that you would treat a private key or root password.

## Create an Environment in Postman

1. If it is not already open, **open** Postman
2. In the Workspace menu on the left side of the page, **click** the Environments tab
3. **Click** the + button to create a new environment
4. **Type** a name, such as "My Sandbox Store" into the Environment Name field
5. **Create** the following variables:

    **Environment Variables**
    | Variable | Type | Initial Value | Current Value |
    | --- | --- | --- | --- |
    | store_hash | Default | Paste your store hash | Paste your store hash |
    | v3_token | Default | Paste your Access Token copied from API account creation | Paste your Access Token copied from API account creation |

6. **Click** Save
7. Before you make a call, you must **assign** the new environment. Above the Save button, **click** the drop down arrow next to &quot;No Environment.&quot; **Select** your new environment to assign.


### Create a Preset for Request Headers

<Callout type="info">
Saving your request header information in a preset will allow you to quickly populate your request headers rather than having to re-enter this information.
</Callout>

1. **Open** Postman
2. **Navigate** to your workspace
3. **Click** + to open a new tab
4. **Click** on the Headers tab
5. **Click** on Presets
6. **Click** Manage Presets
7. **Click** Add
8. **Add** the following presets

    **Postman Presets**
    | Field | Value |
    | --- | --- |
    | Accept | `application/json` |
    | Content-Type | `application/json` |
    | X-Auth-Token | `{{v3_token}}` |

9. **Click** Add to save
10. Before you make a call, you must **assign** the headers. In the headers tab, **click** Presets, and Select your new presets to assign.

## Import Collection

Import the [Catalog API Labs collection](../Catalog%20API%20Labs.postman_collection.json).
