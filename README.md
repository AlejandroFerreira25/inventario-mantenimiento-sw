# Sistema de Inventario y Pedidos "El Sabor Tolimense"

Aplicación web para administrar el inventario y los pedidos de un negocio de comidas. Está hecha en PHP con MySQL y sigue el patrón Modelo, Vista y Controlador (MVC).

Proyecto usado en la Actividad 4 del módulo **Mantenimiento de Software** (Corporación Universitaria Iberoamericana) para practicar control de versiones con Git y GitHub.

## Módulos

| Módulo | Qué hace |
|---|---|
| Autenticación | Inicio de sesión con control de intentos y recuperación de contraseña por correo (PHPMailer). |
| Clientes | Registro, consulta y edición de clientes. |
| Proveedores | Registro y consulta de proveedores. |
| Productos | Registro, edición, búsqueda por nombre y reporte en PDF (Dompdf). |
| Pedidos | Registro y seguimiento del estado de los pedidos. |
| Trabajadores | Gestión del personal y de los usuarios del sistema. |

## Requisitos

- PHP 7.1 o superior con la extensión PDO MySQL (incluida en XAMPP).
- MySQL o MariaDB (incluido en XAMPP).
- Servidor web Apache (recomendado: [XAMPP](https://www.apachefriends.org/)).
- Navegador web actualizado.

Las librerías de PHP (PHPMailer y Dompdf) ya vienen dentro de `Vista/lib`, así que no hace falta instalar Composer.

## Estructura del proyecto

```
inventario-mantenimiento-sw/
├── index.php            # Punto de entrada: decide qué mostrar según ?accion=
├── configuracion.php    # Ajustes de la sesión
├── Controlador/
│   └── Controlador.php  # Coordina las acciones entre el modelo y la vista
├── Modelo/              # Clases de negocio y acceso a datos
│   ├── Conexion.php         # Conexión PDO a MySQL
│   ├── config.ejemplo.php   # Plantilla de configuración de la base de datos
│   ├── Gestor*.php          # Consultas por módulo (productos, pedidos, clientes...)
│   └── *.php                # Entidades (Producto, Pedido, Cliente...)
└── Vista/
    ├── html/            # Páginas del sistema
    ├── css/  js/  img/  # Estilos, scripts e imágenes
    └── lib/             # Librerías de terceros (Bootstrap, PHPMailer, Dompdf...)
```

## Historias de usuario implementadas

| ID | Historia | Rama | Responsable |
|---|---|---|---|
| HU-01 | Datos de conexión en un archivo local excluido del repositorio | `feature/hu01-configuracion-segura` | Carlos Ferreira |
| HU-02 | Registro de entradas de inventario | `feature/hu02-entradas` | Edwin Cuervo |
| HU-03 | Búsqueda de productos por nombre | `feature/hu03-busqueda-productos` | Carlos Ferreira |
| HU-04 | Alerta de productos con existencias bajas | `feature/hu04-alerta-stock` | Edwin Cuervo |
| HU-05 | Documentación del proyecto (este README) | `docs/hu05-readme` | Carlos Ferreira y Edwin Cuervo |

## Integrantes

- Carlos Alejandro Ferreira Giraldo ([@AlejandroFerreira25](https://github.com/AlejandroFerreira25))
- Edwin Alexander Cuervo Cómbita
