# Tienda PHP con XAMPP y MySQL

Mini-inventario desarrollado en PHP que permite listar productos, agregar nuevos artículos y marcarlos como adquiridos o no adquiridos. Proyecto académico integrado con XAMPP, MySQL y publicado en GitHub.

## 📋 Requisitos

- Sistema operativo: Windows (probado en Windows 11 Pro)
- [XAMPP](https://www.apachefriends.org/index.html) instalado (versión que incluya Apache y MySQL)
- Navegador web moderno (Chrome, Firefox, Edge, etc.)
- Acceso a `phpMyAdmin` (incluido en XAMPP)
- Git (opcional, solo si deseas clonar o publicar en GitHub)

## ⚙️ Instalación

1. **Iniciar XAMPP**  
   - Abre el panel de control de XAMPP.
   - Inicia los módulos **Apache** y **MySQL**.

2. **Crear la base de datos**  
   - Abre tu navegador y ve a `http://localhost/phpmyadmin`.
   - Ejecuta el siguiente script SQL para crear la base de datos y la tabla:

     ```sql
     CREATE DATABASE tienda CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
     USE tienda;
     CREATE TABLE productos (
       id INT AUTO_INCREMENT PRIMARY KEY,
       nombre VARCHAR(120) NOT NULL,
       precio DECIMAL(10,2) NOT NULL,
       adquirido TINYINT(1) NOT NULL DEFAULT 0,
       creado_en TIMESTAMP DEFAULT CURRENT_TIMESTAMP
     );
     ```

3. **Copiar el proyecto**  
   - Crea la carpeta `tienda` dentro de `C:\xampp\htdocs\`.
   - Coloca el archivo `index.php` (incluido en este repositorio) dentro de esa carpeta.

4. **Acceder a la aplicación**  
   - Abre tu navegador y visita:  
     `http://localhost/tienda/`

## 🖥️ Uso

- **Agregar producto**: Completa los campos *Nombre* y *Precio* y haz clic en "Agregar".
- **Marcar como adquirido**: Haz clic en el botón **Toggle** junto a cualquier producto para alternar su estado entre *Sí* y *No*.
- Los productos se muestran ordenados por ID descendente.

## 📁 Estructura del proyecto



> Nota: Este proyecto no incluye autenticación ni medidas de seguridad avanzadas. Está pensado únicamente con fines educativos.

## 📸 Capturas (ver manual adjunto)

El manual entregable incluye:
- Capturas del código fuente comentado.
- Resultados de consultas SQL en phpMyAdmin.
- Ejemplos del funcionamiento en el navegador con al menos 3 productos y estados alternados.

## 📬 Autor

- Nombre del estudiante (Eithel Herrea Rojas)
- Curso: [Tecnologias y sistemas web III]
- Institución: [Tu institución]

---

✅ Proyecto desarrollado como parte de la práctica "PHP + XAMPP + MySQL + GitHub".