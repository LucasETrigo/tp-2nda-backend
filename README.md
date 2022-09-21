// --- Pruebas productos --- //

# // Devolver todos los productos
GET http://localhost:8080/api/productos/ 
Content-Type: application/json

# // Devolver un producto por id
# GET http://localhost:8080/api/productos/:4 
# Content-Type: application/json

// Actualizar un producto
// Hay que dejar una linea vacia despues de content-type
# PUT http://localhost:8080/api/productos/:4 
# Content-Type: application/json

# {
#     "title": "Producto actualizado 1",
#     "price": 1000,
#     "thumbnail": "foto actualizada 1",
#     "descripcion": "pequeña descripcion del producto",
#     "codigo": "00-12-34",
#     "stock": 10
# }

// Agregar un producto
// Hay que dejar una linea vacia despues de content-type
# POST http://localhost:8080/api/productos/ 
# Content-Type: application/json

# {
#     "title": "Producto nuevo b",
#     "price": 3456,
#     "thumbnail": "foto nueva",
#     "descripcion": "pequeña descripcion del producto",
#     "codigo": "00-12-34",
#     "stock": 10
# }

// Borrar por producto por id
# DELETE http://localhost:8080/api/productos/:6 
# Content-Type: application/json

// Prueba 404 productos
# GET http://localhost:8080/api/productos/prueba/404 
# Content-Type: application/json

// --- Pruebas carrito --- //

// Crear carrito
# POST http://localhost:8080/api/carrito/ 
# Content-Type: application/json

// Borrar carrito
# DELETE http://localhost:8080/api/carrito/:3 
# Content-Type: application/json

// Agregar producto al carrito
# POST http://localhost:8080/api/carrito/:5/productos/:2 
# Content-Type: application/json

// Borrar producto del carrito
# DELETE http://localhost:8080/api/carrito/:3/productos/:4 
# Content-Type: application/json

// Listar productos en carrito
# GET http://localhost:8080/api/carrito/:3/productos 
# Content-Type: application/json

// Prueba 404 productos
# GET http://localhost:8080/api/carrito/prueba/404
# Content-Type: application/json