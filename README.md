# inventory-management-system
Assignment+No1-2024 web serves

<br><br>
Collection Resource (/Products)
| HTTP request (method URI) | Operation              | Description     |HTTP status codes |Request sample|Respose sample |
|---------------------------|------------------------|-----------------|-----------------|-----------------|-----------------|
| POST / Product            |Create                  | Create a new product   |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource. |{ “name “:gaming mouse”,“Description “ :”Brand Redragon Color Black”,“Category “:“electronics”,“Price “:30}|HTTP/1.1 200 OK“Added successfully”|
|GET/ Product               | Read                   |Show a product and see its details by id .   |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|get /Product/8800 HTTP/1.1 ?id=55656Productget.com Authorization: Bearer your-access-token|{“id”: “55656 “,“name “:gaming mouse”,“Description “ :”Brand Redragon Color Black”,“Category “: “electronics”,“Price“:30}|
| PUT / Product             |Update/Replace          |Updates an existing product by id .    |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|Put /Product/8800 HTTP/1.1 Host: Productget.com Authorization: Bearer your-access-token{“name “:gaming mouse”,“Description “ :”Brand Redragon Color red”,“Category “: “electronics”,“Price “:35}|HTTP/1.1 200 OK “Update successfully”|
|PATCH/ Product             | Partial Update/Modify  |Partially updates an existing product by id .   |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|PATCH /Product/8800 HTTP/1.1 /id?=55656{ "price": 19.99, }|HTTP/1.1 200 OK {“name “:gaming mouse”,“Description “ :”Brand Redragon Color red”,“Category “: “electronics”,“Price “:19.99}|
|DELETE/ Product            |Delete                  | Delete Product by id    |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|DELETE /Product/55656|“Detele successfully”|
|GET/Product/{id}             |Read Products info       | Retrieves information about a specific product identified by its ID.   |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|GET /Products/55656 HTTP/1.1 Host: localhost.com Authorization: Bearer your_access_token|{“id”: “55656 “,“name“ gaming mouse”,“Description “ :”Brand Redragon Color Black”,“Category “: “electronics”,“Price“:30}| 






<br><br>
Collection Resource (/supplier)
| HTTP request (method URI) | Operation              | Description     |HTTP status codes |Request sample|Respose sample |
|---------------------------|------------------------|-----------------|-----------------|-----------------|-----------------|
| POST / supplier            |Create                  |Creates a new supplier resource  |201 Created: The supplier resource was successfully created.401 Unauthorized: Authentication credentials were missing or invalid.500 Internal Server Error: An unexpected error occurred on the server. |POST /supplier HTTP/1.1 Host: example.com Content-Type: application/json Authorization: Bearer your_access_token  {"name": "Ahmad saleh Omar","phone": "052243665","city": "Ramallah","email": "Ahmad-5saleh@gmail.com","description": ""}|HTTP/1.1 200 OK“Added successfully”|
|GET/ supplier               | Read                   | Retrieves information about all suppliers.  |200 OK: The request was successful, and the response contains a list of suppliers.403 Forbidden: The user does not have permission to access supplier information.500 Internal Server Error: An unexpected error occurred on the server.|GET /supplier HTTP/1.1|HTTP/1.1 200 OK  [{"id":"555666","name": "Ahmad saleh Omar","phone": "052243665","city": "Ramallah","email": "Ahmad-5saleh@gmail.com","description": ""}]|
| PUT / supplier             |Update/Replace          | Updates an existing supplier resource identified by its ID.   |200 OK: The supplier resource was successfully updated.404 Not Found: The specified supplier does not exist.500 Internal Server Error: An unexpected error occurred on the server.|PUT /supplier/555666 HTTP/1.1  { "name": "Ahmad saleh Omar","phone": "052243665","city": "Ramallah","email": "Ahmad-5saleh@gmail.com","description": "Agent of Enco Electrical Tools Company"}|HTTP/1.1 200 OK “Update successfully”|
|PATCH/ supplier | Partial Update/Modify  |Partially updates an existing supplier resource identified by its ID.  |200 OK: The request was successful, and the response contains a list of suppliers.403 Forbidden: The user does not have permission to access supplier information.500 Internal Server Error: An unexpected error occurred on the server.|PATCH /supplier/555666 HTTP/1.1  { "phone": "052223321" } |HTTP/1.1 200 OK  { "name": "Ahmad saleh Omar","phone": "052223321","city": "Ramallah","email": "Ahmad-5saleh@gmail.com","description": "Agent of Enco Electrical Tools Company"} |
|DELETE/ supplier            |Delete                  | Deletes an existing supplier resource identified by its ID.   |200 OK: The request was successful. 400 Bad Request: The server cannot process the request due to a client error, such as malformed syntax or invalid parameters.404 Not Found: The requested resource could not be found at the provided URI.|DELETE /supplier/555666 HTTP/1.1 Host: example.com Authorization: Bearer your_access_token|successfully deleted|
|GET/supplier/{id}            |Read supplier info       |Retrieves information about a specific supplier identified by their ID.    |200 OK: Indicates that the request was successful, and the response contains the requested supplier information.404 Not Found: Indicates that the supplier with the specified ID does not exist.|{"id":555666}|HTTP/1.1 200 OK {"id":555666, "name": "Ahmad saleh Omar","phone": "052223321","city": "Ramallah","email": "Ahmad-5saleh@gmail.com","description": "Agent of Enco Electrical Tools Company"}|




































<br><br>
Collection Resource (/store item)
| HTTP request (method URI) | Operation              | Description     |HTTP status codes |Request sample|Respose sample |
|---------------------------|------------------------|-----------------|-----------------|-----------------|-----------------|
| POST / store-item            |Create                  |Creates a new store item. |400 Bad Request: The request was malformed or contained invalid data.403 Forbidden: The user does not have permission to create a store item.|POST /store-items HTTP/1.1  {"productId": "10","storeId": "ram32","totalQuantity": 100}|successfully created|
|GET/ store-item               | Read                   |Retrieves information about store items.  |200 OK: The request was successful, and the response body contains the requested store item information. 403 Forbidden: The user does not have permission to access the resource.|GET /storeitem HTTP/1.1|[ {"id":1 ,productId": "10","storeId": "ram32","totalQuantity": 100},{"id":2 ,"productId": "11","storeId": "ram32","totalQuantity": 94}] |
| PUT / store-item             |Update/Replace          | Updates an existing store item   |200 OK: The store item was successfully updated.404 Not Found: The specified store item does not exist.|PUT /storeitem HTTP/1.1  {"id":1 ,productId": "10","storeId": "ram32","totalQuantity": 150}|HTTP/1.1 200 OK {"id":1 ,productId": "10","storeId": "ram32","totalQuantity": 150}|
|PATCH/ store-item             | Partial Update/Modify  |Partially updates an existing store item resource identified by its ID.   |200 OK: The store item was successfully updated. 400 Bad Request: The request was malformed or contained invalid data.500 Internal Server Error: An unexpected error occurred on the server.|PATCH /storeitem/1 HTTP/1.1  {"totalQuantity": 200}|    successfully updated   {"id":1 ,productId": "10","storeId": "ram32","totalQuantity": 200} |
|DELETE/ store-item            |Delete                  | Deletes an existing store item identified by its ID.   |204 No Content: The store item was successfully deleted.404 Not Found: The specified store item does not exist.|DELETE /storeitem/1 HTTP/1.1|"successfully deleted"|
|GET/ store-item /id           |Read Store-item info       |Retrieves information about a specific store item identified by its ID.   |200 OK: The request was successful, and the response contains the requested store item information. 404 Not Found: The requested store item with the specified ID does not exist.|GET /storeitem/1 HTTP/1.1|HTTP/1.1 200 OK  {"id":1 ,productId": "10","storeId": "ram32","totalQuantity": 200} |





















<br><br>
Collection Resource (/Store)
| HTTP request (method URI) | Operation              | Description     |HTTP status codes |Request sample|Respose sample |
|---------------------------|------------------------|-----------------|-----------------|-----------------|-----------------|
| POST / Store            |Create                  |Creates a new store. |201 Created: The store was successfully created.400 Bad Request: The request was malformed or contained invalid data.500 Internal Server Error: An unexpected error occurred on the server.|POST /store HTTP/1.1   {"id": "ram32","location": "Ramallah Al-Bireh Street under the traffic circle" ,"description":""}|HTTP/1.1 201 Created "uccessfully created" "id": "ram32","location": "Ramallah Al-Bireh Street under the traffic circle","description":""} |
|GET/ Store               | Read                   |Retrieves information about all stores.   |200 OK: The request was successful, and the response body contains the requested store information. 403 Forbidden: The user does not have permission to access the resource.|GET /store HTTP/1.1|HTTP/1.1 200 OK [ {"id": "ram32","location": "Ramallah Al-Bireh Street under the traffic circle","description":""}  {"id": "ram33","location": "Ramallah Al-Bireh Street ","description":""}] |
| PUT / Store             |Update/Replace          | Updates an existing store. |200 OK: The store was successfully updated. 404 Not Found: The specified store does not exist. 500 Internal Server Error: An unexpected error occurred on the server. |PUT /store HTTP/1.1  {"id": "ram33","location": "Ramallah Al-Bireh Street 56 ","description":""}|HTTP/1.1 200 OK   {"id": "ram33","location": "Ramallah Al-Bireh Street 56 ","description":""}|
|PATCH/ Store             | Partial Update/Modify  |Partially updates an existing store.    |200 OK: The store was successfully updated. 404 Not Found: The specified store does not exist.|PATCH /store HTTP/1.1  {"id": "ram33","description":"Your electronics store"} |HTTP/1.1 200 OK    {"id": "ram33","location": "Ramallah Al-Bireh Street ","description":"Your electronics store"}  "successfully updated"|
|DELETE/ Store            |Delete                  |Deletes an existing store.   |404 Not Found: The specified store does not exist.|ّ500 Internal Server Error: An unexpected error occurred on the server.|DELETE /store HTTP/1.1 {id}|"successfully deleted"|
|GET/ Store/id           |Read Store info       | Retrieves information about a specific store identified by its ID.    |Retrieves information about a specific store identified by its ID.  404 Not Found: The requested store with the specified ID does not exist. |GET /store/ram32 HTTP/1.1|HTTP/1.1 200 OK HTTP/1.1 200 OK {"id": "ram33","location": "Ramallah Al-Bireh Street 56 ","description":""} |





  {"id": "ram32","location": "Ramallah Al-Bireh Street under the traffic circle"}

  {"id": "ram33","location": "Ramallah Al-Bireh Street "}












