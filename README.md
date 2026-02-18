# Reto-2-diagramas-tipo-UML
Elija un problema de la vida real (sistema de gestión de biblioteca, negocio de compra-venta, automóvil, etc) que se pueda modelar a través de objetos y clases. Plantee las relaciones de clases, composiciones, propiedades y comportamientos del sistema en uno más diagramas tipo UML.

Respuesta: El problema se centrara en un sistema de compra-venta en una tienda de calzado, a paritr de un diagrama UML de clases elaborado usando Mermaid.

## Diagrama de clases

```mermaid
classDiagram

Cliente "1" --> "0..*" Producto : compra
Tienda "1" *-- "0..*" Producto

class Tienda {
    nombre : String
    venderProducto()
    actualizarMercancia()
}

class Cliente {
    nombre : String
    verProductos()
    mirarPrecio()
    comprarProducto()
}

class Producto {
    nombre : String
    precio : int
    talla : int
    color : String
    actualizarPrecio()
}

class Tenis {
    tipoSuela : String
}

class Tacones {
    alturaTacon : int
}

class Botas {
    tipoMaterial : String
}

Producto <|-- Tenis
Producto <|-- Botas
Producto <|-- Tacones
Producto <|-- Zapatos
```
