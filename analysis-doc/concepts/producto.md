Producto
======

### Definition
Producto es todo producto o servicio que puede ser *adquirido* a través de BE.

#### Description
En principio BE está pensado para manejar los siguientes produtos:
* Viajes de egresados
* Fiesta de egresados
* Otros eventos

Estos productos tienen una estructura de características denominadas [items](items-producto.md).
Cuando los items de un producto han sido seleccionados y votados por el grupo el producto se transforma en [paquete](paquete.md).
Los items de un producto pueden provenir de distintos [templates](templates.md) y puden ser excluyentes



Producto: Viaje de egresado
* Destino [1]

    * Nacional [1]
        * Bariloche [0,1]
            * Transporte [1]
                * Bus (0,1)
                * Tren (0,1)
                * Aereo (0,1)
                
            * Excursiones [0..N]
                * Lago Lacar (0,1)
                * Cerro Catedral (0,1)
                
            * Disco [0..N]
                * Cerebro (0..N)
                * Pachanga (0..N)
                
        * Córdoba [0,1]
        
    * Internacional [1]
        * Brasil
        * Europa
        * Transporte
            * Marítimo
            * Aereo
            
* Duración [1..N]
    * 7 días (0,1)
    * 10 días (0,1)
    * 15 días (0,1)
    
Puede haber comentarios sobre cada uno de los nodos.
[] Indica que el nodo no es votable y la cantidad de subnodos que se pueden elegir (es decir si son excluyentes o no)
() Indica que el nodo es votable y la cantidad de votos que puede tener


#### Attributes

### Processes related to this concept

### Relationships with other concepts
* Link to other concept 
* ...
* Link to other concept

### Examples 

Provide some concrete examples whenever possible
* Example 
* ...
* Example
