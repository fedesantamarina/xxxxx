# xxxxx
```mermaid
erDiagram
    CLIENTE {
        int ID_Cliente PK
        string Nombre
        string Teléfono
        string Email
        string Dirección
    }
    
    PRODUCTO {
        int ID_Producto PK
        string Nombre
        string Descripción
        float Precio
        int Stock
    }
    
    PEDIDO {
        int ID_Pedido PK
        date Fecha
        float Total
        int ID_Cliente FK
    }
    
    DETALLE_PEDIDO {
        int ID_Detalle PK
        int ID_Pedido FK
        int ID_Producto FK
        int Cantidad
        float Precio_Unitario
    }
    
    EMPLEADO {
        int ID_Empleado PK
        string Nombre
        string Cargo
        float Salario
    }
    
    CLIENTE ||--o{ PEDIDO : realiza
    PEDIDO ||--o{ DETALLE_PEDIDO : tiene
    PRODUCTO ||--o{ DETALLE_PEDIDO : está_en
    EMPLEADO ||--o{ PEDIDO : gestiona
```
