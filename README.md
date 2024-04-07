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
Collection Resource (/supplier)
| HTTP request (method URI) | Operation              | Description     |HTTP status codes |Request sample|Respose sample |
|---------------------------|------------------------|-----------------|-----------------|-----------------|-----------------|
| POST / supplier            |Create                  |Creates a new supplier resource  |201 Created: The supplier resource was successfully created.401 Unauthorized: Authentication credentials were missing or invalid.500 Internal Server Error: An unexpected error occurred on the server. |POST /supplier HTTP/1.1 Host: example.com Content-Type: application/json Authorization: Bearer your_access_token|-----------------|
|GET/ supplier               | Read                   | Row 2, Col 3    |-----------------|-----------------|-----------------|
| PUT / supplier             |Update/Replace          | Row 3, Col 3    |-----------------|-----------------|-----------------|
|PATCH/ supplier             | Partial Update/Modify  | Row 3, Col 3    |-----------------|-----------------|-----------------|
|DELETE/ supplier            |Delete                  | Row 3, Col 3    |-----------------|-----------------|-----------------|
|DELETE/ supplier            |Read supplier info       | Row 3, Col 3    |-----------------|-----------------|-----------------|





















<br><br>
Collection Resource (/supplier)
| HTTP request (method URI) | Operation              | Description     |HTTP status codes |Request sample|Respose sample |
|---------------------------|------------------------|-----------------|-----------------|-----------------|-----------------|
| POST / supplier            |Create                  |Creates a new supplier resource  |201 Created: The supplier resource was successfully created.401 Unauthorized: Authentication credentials were missing or invalid.500 Internal Server Error: An unexpected error occurred on the server. |POST /supplier HTTP/1.1 Host: example.com Content-Type: application/json Authorization: Bearer your_access_token|-----------------|
|GET/ supplier               | Read                   | Row 2, Col 3    |-----------------|-----------------|-----------------|
| PUT / supplier             |Update/Replace          | Row 3, Col 3    |-----------------|-----------------|-----------------|
|PATCH/ supplier             | Partial Update/Modify  | Row 3, Col 3    |-----------------|-----------------|-----------------|
|DELETE/ supplier            |Delete                  | Row 3, Col 3    |-----------------|-----------------|-----------------|
|DELETE/ supplier            |Read supplier info       | Row 3, Col 3    |-----------------|-----------------|-----------------|


















