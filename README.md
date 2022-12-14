# Arpi Tool API 

## REST API con CRUD para  operaciones ecommerce. 
## For installing the application to your local environment:
 Clonar repositorio a tu maquina.
 Abrí el directorio del proyecto e instala las dependencias -> "composer install".    
 Hace las conecciones en la base de datos en el archivo -> .env.
 Hacé las migraciones via -> "php artisan migrate".
 Instalá Laravel passport via -> "php artisan passport:install".
 Iniciá la aplicación -> "php artisan serve".

# Documentación API
## Endpoints:

 Registro de usuario:                     "/api/register"  
 Login de usuario:                        "/api/login"    
 Logout de usuario:                       "/api/logout"   

 Listar productos:                        "/api/products"
 Lista los productos de una categoria:    "/api/products/{category_id}"      
 Recuperar un solo producto:              "/api/single-product/{id}"
 Listar todas las categorias:             "/api/categories"
 Recuperar una sola categoria por id:     "/categories/{id}"

 Añadir nuevo producto:                   "/api/add-product"
 Añadir productos multiples:              "/api/add-products"
 Actualizar un producto:                  "/api/update-product/{id}"
 Eliminar un producto:                    "/api/delete-product/{id}"
 Añadir una categoria:                    "/api/add-category"
 Actualizar una categoria:                "/api/update-category/{id}"      
 Eliminar una categoria:                  "/api/delete-category/{id}"

## Los formato de información a enviar deben ser en Json con los siguientes:

## Data de registro:
{
    "name": "John Doe",
    "email": "john@doe.com",
    "password": "password",
    "c_password": "password",
    "role": "admin"
}

## Data de login:
{
    "email": "john@doe.com",
    "password":"password"
}

## Añadir y actualizar data de categoria:
{
    "name":"technolgy"
}

## Añadir y actualzia data de productos:
{
    "name": "sample product1",
    "category_id": "2",
    "price":"123",
    "description":"lorem ipsum dolor",
    "image":"www.imagelink.com"
}

## Añadir multiples productos con una ruta:
{   
   "products": [   
    {
    "name": "sample product1",
    "category_id": "1",
    "price":"123",
    "description":"lorem ipsum dolor",
    "image":"www.imagelink.com"
    },   
    {
    "name": "sample product2",
    "category_id": "2",
    "price":"123",
    "description":"lorem ipsum dolor",
    "image":"www.imagelink.com"
    },   
    {
    "name": "sample product3",
    "category_id": "1",
    "price":"123",
    "description":"lorem ipsum dolor",
    "image":"www.imagelink.com"
    }   
   ]
}
