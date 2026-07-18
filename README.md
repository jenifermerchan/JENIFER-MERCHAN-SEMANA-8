# Sistema Restaurante App

**Estudiante:** Jenifer Estefania Merchan Jauregui
**Asignatura:** Programación Orientada a Objetos - Semana 8  

## Descripción del sistema
Se trata de un programa de consola desarrollado en Python con arquitectura modular. Su objetivo es administrar el 
registro de clientes, bebidas y productos en un restaurante bajo los principios de diseño SOLID.

## Estructura del proyecto
```text
restaurante_app/
│
├── modelos/
│   ├── __init__.py
│   ├── producto.py
│   ├── bebida.py
│   └── cliente.py
│
├── servicios/
│   ├── __init__.py
│   └── restaurante.py
│
├── main.py
└── README.md
```

## Responsabilidad de cada clase
Producto (modelos/producto.py): Modela la información general de cualquier platillo o artículo del restaurante y define 
cómo exponer sus datos.

Bebida (modelos/bebida.py): Deriva de la clase base para añadir propiedades particulares como el volumen y la 
presentación del envase.

Cliente (modelos/cliente.py): Define de forma autónoma los datos personales y de contacto de un usuario del establecimiento.

Restaurante (servicios/restaurante.py): Gestiona el almacenamiento interno, asegura que no existan registros repetidos y 
provee las listas de datos.

Main (main.py): Controla el flujo principal, despliega las opciones en pantalla, recibe las entradas del usuario y 
conecta con la lógica del servicio.

## Principios SOLID aplicados
Responsabilidad única (SRP): Cada componente tiene un rol único y claro; la interfaz visual, el control del negocio y 
los datos están totalmente separados.

Abierto/cerrado (OCP): El diseño admite nuevas especializaciones de productos usando herencia, evitando alterar el código 
base del servicio principal.

Sustitución de Liskov (LSP): Las bebidas actúan de forma equivalente a cualquier producto, logrando que el listado general 
las procese de manera idéntica y polimórfica.

## Reflexion
La importancia de diseñar proyectos mantenibles es que es una parte clave porque el software siempre cambia y crece con 
el tiempo. Al aplicar estructuras limpias y principios como SOLID, logramos que corregir errores, añadir nuevas funciones 
o mejorar el sistema sea un proceso rápido, seguro y sin el riesgo de dañar lo que ya funciona bien.