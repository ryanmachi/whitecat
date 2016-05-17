
Products
===

## Model

### PRODUCT_INFO_DICT

Name | Type | Description
---  | ---  | ---
productID | string |
name | string |
price|int|
title|string|
coverPic|string|
pic|string|
picNum|int|
sanbox|int|
description|string|
specialPrice|string|
coupon|int|
type|int|
shareurl|string|
color|string|
instock|int|
relatedproduct|[]string|
nextproduct|[]string|



## Get product info by id
```
GET /products/<id>
```

**URL Parameter**

none

**Response**

PRODUCT_INFO_DICT

## Get the productlist
```
GET /products/
```
Retrieve the product list 

**Parameter**


Name | Type | Description
---  | ---  | ---
productType | string | 
priceMin | int | 
priceMax |int|
query|string|
orderby|string|lowest price , expensive price,newest



**Response**

[]PRODUCT_INFO_DICT


