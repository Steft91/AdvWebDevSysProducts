# SysProductCategory - Sistema CRUD con Docker (Angular + Spring Boot + MySQL)

Este proyecto implementa un sistema CRUD para **Productos** y **Categorías**, desarrollado con:
- **Frontend**: Angular
- **Backend**: Spring Boot (Microservicios Products y Categories)
- **Base de datos**: MySQL
- **Orquestación**: Docker Compose

---
## Acceso Público al Sistema
El sistema está desplegado en un servidor Linux con Docker y Docker Compose en **DigitalOcean**, accesible en la siguiente URL:

🔗 **[Abrir aplicación](http://167.172.30.93:4200)**

---

## Requisitos previos para el sistema localmente

Antes de ejecutar, tener instalado:
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/)

---

## Instrucciones de ejecución

1. **Clonar el repositorio**  
   ```bash
   git clone https://github.com/Steft91/AdvWebDevSysProducts.git
   cd AdvWebDevSysProductCategory
   ```
2. **Levantar todo con Docker Compose**  
   ```bash
   docker-compose up -d --build
   ```
   Contiene estos puertos:
   - MySQL (Puerto 3307)
   - Microservicio Products (Puerto 8081)
   - Microservicio Categories (Puerto 8083)
   - Frontend Angular (Puerto 4200)
cd SysProductCategory

3. **Acceso a la aplicación**  
   Frontend Angular → [http://localhost:4200](http://localhost:4200)  


4. **Arquitectura y Funcionamiento de los Servicios**  
   El proyecto está dividido en **dos microservicios** (`products-service` y `categories-service`) y un **frontend en Angular**.  
   Cada microservicio maneja la lógica de negocio y la conexión con la base de datos MySQL.

### CategoryServiceImpl (Microservicio de Categorías)
Maneja toda la lógica de negocio para **categorías**:
- `getAllCategories()` → Lista todas las categorías.
- `createCategory(category)` → Crea una nueva categoría.
- `updateCategory(id, updatedCategory)` → Actualiza una categoría existente pero esto no incluye la fecha ya que este queda con la creada desde el inicio.
- `deleteCategory(id)` → Elimina una categoría existente.

---

### ProductServiceImpl (Microservicio de Productos)
Maneja la lógica de negocio para **productos**:
- `getAllProducts()` → Lista todos los productos.
- `createProduct(product)` → Crea un nuevo producto.
- `updateProduct(id, product)` → Actualiza un producto existente.
- `deleteProduct(id)` → Elimina un producto existente.

---


