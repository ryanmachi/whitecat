Users
===

## Model

### USER_INFO_DICT

Name | Type | Description
---  | ---  | ---
accountName | string |
password | string |Md5 in mysql
appVersion|string|
phoneNumber|string|
location|string|
everPaid|string|
email|string|
facebookID|string|
deviceModel|string|



## Check Available
```
GET /users/available?...
```

**URL Parameter**

Name | Type | Description
---  | ---  | ---
facebookID | string |
accountName | string |

**Response**

HTTP 200

HTTP 404


## Get the user object of myself
```
GET /users/me
```
Retrieve the user information of the given api key. It will contain more sensitive data.

**Parameter**

None

**Response**

SELF_INFO_DICT


## Login 
```
GET /users/login
```
Let the user login with facebook auth or password

**Parameter**

Name | Type | Description
---  | ---  | ---
accountName | string | 
password | string | 
facebookID|string|

**Response**

SELF_INFO_DICT


## Update user
```
PATCH /users/me
```

**Multipart Parameter**

Name | Type | Description
---  | ---  | ---
accountName | string | 
password | string | 
location|string|(optional)
phoneNumber|string|(optional)
email|string|(optional)
appVersion|string|
deviceModel|string|

**Response**

HTTP 200

HTTP 404


## Register user
```
POST /users/?
```

**Multipart Parameter**

Name | Type | Description
---  | ---  | ---
accountName | string | 
password | string | 
location|string|(optional)
phoneNumber|string|(optional)
email|string|(optional)


**Response**

HTTP 200

HTTP 404
