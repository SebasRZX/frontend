# istema de Gestión de Ventas y Eventos Parroquiales

Este proyecto es una *aplicación web full-stack* desarrollada para la administración de ventas, inventario, eventos y turnos de personal en un entorno parroquial.  
Incluye control de cajas diarias, gestión de productos, asignación de roles y generación de reportes, con autenticación y autorización por roles.

---

# Tecnologías Utilizadas

*Frontend*
- [Next.js](https://nextjs.org/) (App Router, React 19)
- [Tailwind CSS](https://tailwindcss.com/) + clases personalizadas
- React Hooks (useState, useEffect, useParams, useRouter)
- Context API para manejo de autenticación
- Componentes reutilizables y modales con animaciones
- Consumo de API REST con fetch y credenciales incluidas (credentials: 'include')

*Backend*
- [Node.js](https://nodejs.org/) + [Express](https://expressjs.com/)
- MySQL 8 con consultas mediante mysql2
- Autenticación con JWT y cookies HTTP-only
- Middleware de verificación de token y control de acceso por rol (admin, coordinador, usuario)
- Subida de imágenes con multer
- Estructura MVC (Modelos, Controladores, Rutas)

*Base de Datos*
- MySQL alojado en Azure Database for MySQL
- Tablas principales:
  - usuarios
  - productos
  - categorias
  - ventas y detalle_venta
  - cajas
  - eventos
  - turnos y turno_usuarios

---

# Funcionalidades

*Autenticación y Roles*
- Login con validación en backend
- Cookies HTTP-only para mayor seguridad
- Verificación automática de sesión
- Control de acceso por rol a rutas protegidas

*Gestión de Productos*
- Alta, edición, eliminación suave y restauración de productos
- Asociación a categorías
- Subida de imágenes
- Listado de productos activos e inactivos

*Ventas*
- Registro de ventas con detalle de productos y cantidades
- Opción de venta "para llevar" con costo adicional configurable
- Formas de pago: efectivo y SINPE
- Cálculo de vuelto automático
- Asociación de ventas a evento y caja

*Cajas*
- Apertura y cierre de caja por usuario
- Registro de montos de apertura y cierre
- Resumen de ventas por forma de pago
- Diferencia entre monto esperado y contado
- Reporte de cajas abiertas y cerradas con filtros

*Eventos y Turnos*
- Creación y edición de eventos
- Gestión de turnos asociados a eventos
- Asignación de usuarios y roles a cada turno
- Listado interactivo con fechas y horas legibles

---

# Instalación y Configuración

### Clonar el repositorio
```bash
git clone https://github.com/usuario/repositorio.git
cd repositorio