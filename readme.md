#  Instrucciones para el correcto funcionamiento

#### Cargar Productos y Carrito de Testing en la BD
- Setear el String de conexion a la BD el archivo se encuentra en la carpeta src/config/database.config.js
- Se puede optar por 2 opciones:
	MongoDB Compass
	MongoDB Atlas

- Acceder a la carpeta src
- Ejecutar el archivo testingCrear.js "node testingCrear.js" (Este archivo va a cargar los productos y carritos)
- Ejecutar el servidor "npm test".

####  Eliminar Productos  Carritos y usuarios de la BD 
-  Una vez termiando con las pruebas puede eliminar los productos de la BD
- Ejecutar el archivo testingEliminar.js "node testingEliminar.js".


### EndPoint User-
- http://localhost:8080 
- http://localhost:8080/login    
   - Registro de usuario.
   - Login Usuario Registrado Local.
   - Login Github.
- http://localhost:8080/profile 
- http://localhost:8080/products 
- http://localhost:8080/api/sessions/current 

------------
###EndPoint Products

GET Products
http://localhost:8080/api/products 
- acepta parametros opcioneales de busqueda:
	- limit: numerico
	- page: numerico
	- sort: 'desc' / 'asc'
	- query: string ( categoria el producto que desea buscar )

Get ProductById
- http://localhost:8080/api/products/:id
POST AddProduct
- http://localhost:8080/api/products
PUT UpdateProduct
- http://localhost:8080/api/products/:id
DEL DeleteProduct
- http://localhost:8080/api/products/:id

# EndPoint Carts
POST AddCart
- http://localhost:8080/api/carts/
POST AddProductToCart
- http://localhost:8080/api/carts/:cid/product/:pid
GET ProductCart
- http://localhost:8080/api/carts/:cid 
DEL DeleteProductCart
- http://localhost:8080/api/carts/:cid/product/:pid
DEL DeleteAllProductCart
- http://localhost:8080/api/carts/:cid
PUT UpdateProductsCart 
- http://localhost:8080/api/carts/:cid
PUT UpdateQuantityCartProduct 
- http://localhost:8080/api/carts/:cid/product/:pid

# View 

- http://localhost:8080/ 

- http://localhost:8080/products
	
- http://localhost:8080/carts/:cid
	
# Testing ( Coleccion Postman para realizar los testing a todos los EndPoint )
- En la carpeta src/test/postman/E-commerce Backend Server.postman_collection.js
- Podes importar la coleccion en POSTMAN y realizar los TEST a los endPoint

