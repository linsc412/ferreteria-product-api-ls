# Ejercicio en clase

# Cómo correr los apis localmente?

1. Tener instalado Visual Code y nodejs
2. Bajar la aplicación en la computadora.
3. Abrir el proyecto (folder donde está la aplicación) en visual Code.
4. Abrir la terminal (menu View--> terminal)
5. En la terminal poner el siguiente comando: **npm install** para que se instalen las dependencias del app.
6. Para correr el app ejecutar en la terminal el siguiente comando: **npm start**
7. No cerrar la terminal, ni el Visual Code y acceder al api de products con la siguiente url: [http://localhost:3007/products](http://localhost:3007/products) y el api 

## Endpoints de los apis
| Endpoint | Método | Descripción | Input | Output | Ejemplo | Excepciones |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| GetAllProducts | GET | Retorna todos los productos almacenados |  | [{"productId": 2,"productName": "Garden Cart","productCode": "GDN-0023", "releaseDate": "March 18, 2019","price": 32.99,"description": "15 gallon capacity rolling garden cart","starRating": 5,"imageUrl": "assets/images/garden.jpg"}, {"productId": 5,"productName": "Hammer","productCode": "TBX-0048","releaseDate": "May 21, 2019","price": 8.9,"description": "Curved claw steel hammer","starRating": 4.6,"imageUrl": "assets/images/hammer.jpg"},{"productId": 7,"productName": "Drill","productCode": "PRX-095","releaseDate": "Sept 2nd, 2019","price": 32.9,"description": "","starRating": 3.2,"imageUrl": "assets/images/drill.jpg"} | http://localhost:3007/products | Si no hay productos se devuelve un [] | 
| GetAProduct | GET | Devuelve la información de un producto | productId | [{"productId": 5,"productName": "Hammer","productCode": "TBX-0048","releaseDate": "May 21, 2019","price": 8.9,"description": "Curved claw steel hammer","starRating": 4.6,"imageUrl": "assets/images/hammer.jpg"}] | http://localhost:3007/products/5 | Si no existe el producto consultado, se devuelve: {"success": "false", "message": "Product not found"} |
| DeleteProduct | DELETE | Elimina un producto | productId | [{"productId": 5,"productName": "Hammer","productCode": "TBX-0048","releaseDate": "May 21, 2019","price": 8.9,"description": "Curved claw steel hammer","starRating": 4.6,"imageUrl": "assets/images/hammer.jpg"}] | http://localhost:3007/products/5 | Si no existe el producto que se desea eliminar, se devuelve: {"success": "false","message": "The product does not exist. Specify a product that is already stored."} |
| InsertProduct | POST | Insertar un producto | {"productId": 11,"productName": "Big Hammer","productCode": "GDN-0030","releaseDate": "March 18, 2019","price": 60,"description":"Curved steel hammer","starRating": 3,"imageUrl": "assets/images/hammer.jpg"} | {"productId": 11,"productName": "Big Hammer","productCode": "GDN-0030","releaseDate": "March 18, 2019","price": 60,"description":"Curved steel hammer","starRating": 3,"imageUrl": "assets/images/hammer.jpg"} | http://localhost:3007/products/ |  |
| UpdateProduct | PUT | Actualizar un producto | {"productId": 11,"productName": "Big YELLOW Hammer","productCode": "GDN-0030","releaseDate": "March 20, 2022","price": 70,"description":"Steel hammer","starRating": 4,"imageUrl": "assets/images/hammer.jpg"} | {"productId": 11,"productName": "Big YELLOW Hammer","productCode": "GDN-0030","releaseDate": "March 20, 2022","price": 70,"description":"Steel hammer","starRating": 4,"imageUrl": "assets/images/hammer.jpg"} | http://localhost:3007/products/ | Si el prducto que desea actualizar no existe, se devuelve: {"success": "false","message": "The product does not exist. Specify a product that is already stored."} |

