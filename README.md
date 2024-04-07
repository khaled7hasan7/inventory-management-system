# inventory-management-system
Assignment+No1-2024 web serves

<br><br>
Collection Resource (/Products)
| HTTP request (method URI) | Operation              | Description     |HTTP status codes |Request sample|Respose sample |
|---------------------------|------------------------|-----------------|-----------------|-----------------|-----------------|
| POST / Product            |Create                  | Create a new product   |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource. |{“id”: “55656 “,“name “:gaming mouse”,“Description “ :”Brand Redragon Color Black”,“Category “:“electronics”,“Price “:30}|HTTP/1.1 200 OK“Added successfully”|
|GET/ Product               | Read                   |Show a product and see its details by id .   |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|get /Product/8800 HTTP/1.1 ?id=55656Productget.com Authorization: Bearer your-access-token|{“id”: “55656 “,“name “:gaming mouse”,“Description “ :”Brand Redragon Color Black”,“Category “: “electronics”,“Price“:30}|
| PUT / Product             |Update/Replace          |Updates an existing product by id .    |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|Put /Product/8800 HTTP/1.1 Host: Productget.com Authorization: Bearer your-access-token{“name “:gaming mouse”,“Description “ :”Brand Redragon Color red”,“Category “: “electronics”,“Price “:35}|HTTP/1.1 200 OK “Update successfully”|
|PATCH/ Product             | Partial Update/Modify  |Partially updates an existing product by id .   |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|PATCH /Product/8800 HTTP/1.1 /id?=55656{ "price": 19.99, }|HTTP/1.1 200 OK {“name “:gaming mouse”,“Description “ :”Brand Redragon Color red”,“Category “: “electronics”,“Price “:19.99}|
|DELETE/ Product            |Delete                  | Delete Product by id    |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|DELETE /Product/55656|“Detele successfully”|
|DELETE/ Product            |Read Products info       | Retrieves information about a specific product identified by its ID.   |200 (OK) :The request succeeded.404 Not Found: The requested product does not exist. 403 Forbidden: The user does not have permission to access the resource.|GET /Products/55656 HTTP/1.1 Host: localhost.com Authorization: Bearer your_access_token|{“id”: “55656 “,“name“ gaming mouse”,“Description “ :”Brand Redragon Color Black”,“Category “: “electronics”,“Price“:30}| 






<br><br>
Collection Resource (/Products)
| HTTP request (method URI) | Operation              | Description     |HTTP status codes |Request sample|Respose sample |
|---------------------------|------------------------|-----------------|-----------------|-----------------|-----------------|
| POST / Product            |Create                  | Row 1, Col 3    |-----------------|-----------------|-----------------|
|GET/ Product               | Read                   | Row 2, Col 3    |-----------------|-----------------|-----------------|
| PUT / Product             |Update/Replace          | Row 3, Col 3    |-----------------|-----------------|-----------------|
|PATCH/ Product             | Partial Update/Modify  | Row 3, Col 3    |-----------------|-----------------|-----------------|
|DELETE/ Product            |Delete                  | Row 3, Col 3    |-----------------|-----------------|-----------------|
|DELETE/ Product            |Read Products info       | Row 3, Col 3    |-----------------|-----------------|-----------------|


