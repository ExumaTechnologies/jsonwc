# Exuma Web Connector 3.0.0 API Spec
**RESTful API redesign**
To get to know more about next, read the Wikipedia Article about [REST](https://en.wikipedia.org/wiki/Representational_state_transfer).

## Accept Headers
We avoid having multiple endpoints for XML and JSON by using accept headers before sending a request to the API. The accept header of the request defines the returned type of data. See [W3C Accept Headers Spec](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html), Wikipedia's [List of HTTP Header Fields](http://en.wikipedia.org/wiki/List_of_HTTP_header_fields) and jQuery's [API Docs for $.ajax](http://api.jquery.com/jQuery.ajax/).

For example:
```javascript
$.ajax({
  type: 'POST',
	url: 'http://w:1337/notify',
	dataType: 'json'
});
```

## Missing API Endpoints
These endpoints do not have a spec, yet:
* DirectHitXref
* GetQuantitfyOnHand

## Customers API
### List customers
List all customers. 
`GET /customers`
#### Parameters
tk Parameters which are returned in the valid JSON string.

### Get a single customer
`GET /customers/:id`

#### Parameters
tk Parameters which are returned, see above.

### Create a customer
`POST /customers
#### Input
tk Input sent to the server, mostly see "List customers".

### Edit (Replace) a customer
`PUT /customers/:id`
### Input
tk Input sent to the server, same as create plus an existing.

## Quantity API
**Note:** This specifies only available quantity. We need to get clear on the difference between available and onHand endpoints.

### Get available quantity
`GET /quantity/:location:/:item`
#### Parameters
tk Parameters which are returned.

**Note:** Are there any more operations one can do with quantity (1 out of 5 possible operations defined).

## Vendor API
### Get list of vendors
Get all vendors.
`GET /vendors`
### Parameters
tk

### Get a vendor by ID
`GET /vendors/:id`
### Parameters
See above.

**Note:** Are there any more operations one can do with vendors (2 out of 5 possible operations defined).

## Inventory API
**Note:** This is an educated guess, because I don't know yet how the inventory works.

### Get all inventory items
Get all inventory without respect to being on hand or when it was modified.
`GET /inventory`
#### Parameters
tk

### Get on hand inventory items by lastModified
`GET /inventory/:onHand/:lastModified`
#### Parameters
tk

### Get an inventory item by ID
`GET /inventory/:id`
#### Parameters
tk

## LMTicket API
**Note:** This is an educated guess, because I don't know yet how the LMTicket works.
### Get all LMTickets
`GET /lmtickets/:status/:operator/:location`
#### Parameters
tk

### Get a LMTicket by ID
`GET /lmtickets/:id`
#### Parameters
tk

### Create a LMTicket
`POST /lmtickets`
#### Input
tk

**Note:** Are there any more operations one can do with LMTickets (3 out of 5 possible operations defined).

## Operations API
Was `RetrieveLaunchOpertions`.

### Get all operations
`GET /operations`
#### Parameters
tk

### Get an operation by ID
`GET /operations/:id`
#### Parameters
tk

## Locations API
### Get all locations
`GET /locations`
#### Parameters
tk

### Get a location by ID
`GET /locations/:id`
#### Parameters
tk

**Note:** Are there any more operations one can do with Locations (2 out of 5 possible operations defined).

## Leads API
### Get all leads
`GET /leads`
#### Parameters
tk

### Get a lead by ID
`GET /leads/:id`
#### Parameters
tk

**Note:** Are there any more operations one can do with Leads (2 out of 5 possible operations defined).

## Order API
### Get all orders
`GET /orders`
#### Parameters
tk

### Get a orders by ID
`GET /orders/:id`
#### Parameters
tk

### Create an order
`POST /orders`
#### Input
tk

**Note:** Are there any more operations one can do with Orders (3 out of 5 possible operations defined).

## Parts API



