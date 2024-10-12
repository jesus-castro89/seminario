# Modelos SQL

Los modelos SQL (Structured Query Language) son modelos de bases de datos que utilizan un lenguaje de consulta
estructurado (SQL) para interactuar con la base de datos. Estos modelos se basan en tablas, donde cada tabla representa
una entidad y cada fila de la tabla representa una instancia de esa entidad. Los modelos SQL son adecuados para
representar relaciones de uno a uno, uno a muchos y muchos a muchos.

Los modelos SQL más representativos son:

### Modelo Jerárquico

El modelo jerárquico es un modelo de base de datos en el que los datos se organizan en forma de árbol, donde cada nodo
tiene un único padre y varios hijos. Este modelo es adecuado para representar relaciones de uno a muchos.

```plantuml
@startmindmap
* Modelo Jerárquico
** Ventajas
*** Estructura simple
*** Fácil de entender
** Desventajas
*** Dificultad para representar relaciones de muchos a muchos
*** Dificultad para representar relaciones complejas
@endmindmap
```

### Ejemplo de Modelo Jerárquico

```plantuml
@startuml
entity "Ventas" as ventas {
    + id
    --
    + fecha
    + total
}
entity "ProductoA" as productoA {
    + id
    --
    + nombre
    + precio
}
entity "ProductoB" as productoB {
    + id
    --
    + nombre
    + precio
}
entity "ProductoC" as productoC {
    + id
    --
    + nombre
    + precio
}
entity "ClienteA" as clienteA {
    + id
    --
    + nombre
    + dirección
}
entity "ClienteB" as clienteB {
    + id
    --
    + nombre
    + dirección
}
entity "ClienteC" as clienteC {
    + id
    --
    + nombre
    + dirección
}
ventas -- productoA
ventas -- productoB
ventas -- productoC
productoA -- clienteA
productoB -- clienteB
productoC -- clienteC
@enduml
```

### Modelo de Red

El modelo de red es un modelo de base de datos en el que los datos se organizan en forma de grafo, donde cada nodo puede
tener varios padres y varios hijos. Este modelo es adecuado para representar relaciones de muchos a muchos.

```plantuml
@startmindmap
* Modelo de Red
** Ventajas
*** Flexibilidad en la representación de relaciones
*** Capacidad para representar relaciones de muchos a muchos
** Desventajas
*** Complejidad en la estructura de datos
*** Dificultad para entender las relaciones
@endmindmap
```

### Ejemplo de Modelo de Red

```plantuml
@startuml
entity "Vendedor" as vendedor {
    + id
    --
    + nombre
    + dirección
}
entity "Cliente" as cliente {
    + id
    --
    + nombre
    + dirección
}
entity "Producto" as producto {
    + id
    --
    + nombre
    + precio
}
entity "Empleado" as empleado {
    + id
    --
    + nombre
    + dirección
}
entity "Venta" as venta {
    + id
    --
    + fecha
    + total
}
vendedor -- empleado
vendedor -- cliente
vendedor -- producto
empleado -- venta
cliente -- venta
producto -- venta
@enduml
```

### Modelo Entidad-Relación

El modelo entidad-relación es un modelo de base de datos en el que los datos se organizan en forma de entidades y
relaciones. Cada entidad tiene atributos que describen sus propiedades, y cada relación describe la forma en que las
entidades se relacionan entre sí.

```plantuml
@startmindmap
* Modelo Entidad-Relación
** Ventajas
*** Representación clara de las entidades y relaciones
*** Facilidad para entender la estructura de datos
** Desventajas
*** Dificultad para representar relaciones complejas
*** Limitaciones en la representación de datos
@endmindmap
```

### Ejemplo de Modelo Entidad-Relación

![e-r.png](..%2Fplantuml%2Fe-r.png){display=block}

![eer.png](..%2Fplantuml%2Feer.png){display=block}

### Modelo Relacional

El modelo relacional es un modelo de base de datos en el que los datos se organizan en tablas, donde cada tabla tiene
una clave primaria que identifica de forma única cada fila de la tabla. Este modelo es adecuado para representar
relaciones de uno a uno, uno a muchos y muchos a muchos.

```plantuml
@startmindmap
* Modelo Relacional
** Ventajas
*** Estructura simple y clara
*** Facilidad para representar relaciones
** Desventajas
*** Limitaciones en la representación de datos complejos
*** Dificultad para escalar a grandes volúmenes de datos
@endmindmap
```

### Ejemplo de Modelo Relacional

![er-example.png](..%2Fplantuml%2Fer-example.png){display=block}

```plantuml
@startuml
hide circle
skinparam linetype ortho
entity "Entity01" as e01 {
  e1_id : number <<generated>>
  --
  name : text
  description : text
}
entity "Entity02" as e02 {
  e2_id : number <<generated>>
  --
  e1_id : number <<FK>>
  other_details : text
}
entity "Entity03" as e03 {
  e3_id : number <<generated>>
  --
  e1_id : number <<FK>>
  other_details : text
}
e01 ||..o{ e02
e01 |o..o{ e03
@enduml
```

### Modelo Relacional Orientado a Objetos

El modelo relacional orientado a objetos es un modelo de base de datos que combina las características del modelo
relacional y del modelo orientado a objetos. En este modelo, los datos se organizan en tablas, pero cada tabla puede
contener atributos complejos, como listas o conjuntos.

```plantuml
@startmindmap
* Modelo Relacional Orientado a Objetos
** Ventajas
*** Capacidad para representar datos complejos
*** Facilidad para escalar a grandes volúmenes de datos
** Desventajas
*** Complejidad en la estructura de datos
*** Dificultad para entender las relaciones
@endmindmap
```

### Ejemplo de Modelo Relacional Orientado a Objetos

```plantuml
@startuml
entity "Persona" as persona {
    + id
    --
    + nombre
    + dirección
    + teléfono
    + email
}
entity "Producto" as producto {
    + id
    --
    + nombre
    + precio
    + cantidad
}
entity "Venta" as venta {
    + id
    --
    + fecha
    + total
}
entity "Cliente" as cliente {
    + id
    --
    + nombre
    + dirección
    + teléfono
    + email
}
entity "Empleado" as empleado {
    + id
    --
    + nombre
    + dirección
    + teléfono
    + email
}
persona -- cliente
persona -- empleado
producto -- venta
cliente -- venta
empleado -- venta
@enduml
```