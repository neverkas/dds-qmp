# Diagrama de clases

![diagrama de clases](./assets/diagrama-de-clases.png)

# Diagrama de secuencia

![diagrama de secuencia](./assets/diagrama-de-secuencia.png)

# Pseudocódigo

### Atuendo
Como un atuendo es una combinación de prendas que se tienen que usar juntas,
y como existen 4 categorías que engloban a las prendas. Entonces procedemos con
una clase que contiene acciones para elegir cada una de las categorías.

```
  abstract class Atuendo{
          +construirAtuendo() : Atuendo
          elegirParteSuperior()
          elegirParteInferior()
          elegirCalzado()
          elegirAccesorio()
  }
```

- - -

### Categorías de prendas
Cada categoría de prenda requiere que se elija un color(primario ó secundario), 
su material (cuero, tela, ...) y el tipo (pantalón, remera corta, ....)
Estas tareas se las delegamos a la prenda, y las reutilizaremos en construirPrenda() 

```
  abstract class Accesorio{
          +construirPrenda() : Prenda
          elegirColor()
          elegirMaterial()
          elegirTipo()
  }
  abstract class Calzado{
          +construirPrenda() : Prenda
          elegirColor()
          elegirMaterial()
          elegirTipo()
  }
  abstract class ParteSuperior{
          +construirPrenda() : Prenda
          elegirColor()
          elegirMaterial()
          elegirTipo()
  }

  abstract class ParteInferior{
          +construirPrenda() : Prenda
          elegirColor()
          elegirMaterial()
          elegirTipo()
  }
```

### Prendas

En este tramo final cada prenda puede elegir el color, material y tipo
de un tipo enum donde podremos agregar las distintas variantes

```
  class Prenda{
          +construirPrenda() : Prenda
          -elegirColor()
          -elegirMaterial()
          -elegirTipo()
  }
  
  enum Color
  enum Material
  enum Tipo
```
