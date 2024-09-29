# Estimación por Puntos de Función o Puntos Funcionales

## ¿Qué son los Puntos de Función?

Los **Puntos de Función** son una técnica de estimación de tamaño de software que se basa en la medición de las
funciones que un sistema de software proporciona a los usuarios. Esta técnica se utiliza para estimar el tamaño de un
sistema de software en función de las funciones que realiza y la complejidad de esas funciones.

Los Puntos de Función se utilizan para estimar el tamaño de un sistema de software en términos de la cantidad de
funciones que proporciona y la complejidad de esas funciones. Esta técnica de estimación se basa en la medición de las
funciones de un sistema de software, en lugar de la cantidad de líneas de código o el esfuerzo de desarrollo
necesario.

## ¿Cómo se calculan los Puntos de Función?

Los Puntos de Función se calculan utilizando una fórmula que tiene en cuenta varios factores, como el tipo de función,
la complejidad de la función y el número de funciones del sistema. La fórmula básica para calcular los Puntos de Función
es la siguiente:

```tex
\text{PF} = \text{UFP} \times \text{CF}
```

Donde:

- **PF**: Representa los Puntos de Función del sistema.
- **UFP**: Representa los Puntos de Función sin ajustar, que se calculan sumando los Puntos de Función de cada función
  del sistema.
- **CF**: Representa el factor de ajuste, que se utiliza para ajustar los Puntos de Función sin ajustar en función de
  varios factores, como la complejidad del sistema, la experiencia del equipo de desarrollo, etc.

## ¿Por qué son importantes los Puntos de Función?

Los Puntos de Función son importantes porque permiten estimar el tamaño de un sistema de software en función de las
funciones que proporciona y la complejidad de esas funciones. Esta técnica de estimación es útil para planificar y
controlar proyectos de desarrollo de software, ya que proporciona una medida objetiva del tamaño y la complejidad del
sistema.

Además, los Puntos de Función se utilizan para estimar el esfuerzo de desarrollo necesario para completar un proyecto de
software, lo que ayuda a planificar y asignar los recursos de manera eficiente. Esta técnica de estimación también se
utiliza para estimar los costos y el tiempo necesarios para completar un proyecto de software, lo que ayuda a garantizar
que el proyecto se complete dentro del plazo establecido y con los recursos disponibles.

## Proceso de Estimación por Puntos de Función

El proceso de estimación por Puntos de Función consta de los siguientes pasos:

1. **Identificar las funciones del sistema**: Definir claramente las funciones que el sistema de software proporcionará
   a los usuarios, como la creación de un nuevo usuario, la generación de informes, etc.
2. **Clasificar las funciones**: Clasificar las funciones identificadas en función de su complejidad y su impacto en la
   estimación de los Puntos de Función.
3. **Calcular los Puntos de Función sin ajustar**: Calcular los Puntos de Función sin ajustar sumando los Puntos de
   Función de cada función del sistema.
4. **Aplicar los factores de ajuste**: Aplicar los factores de ajuste para ajustar los Puntos de Función sin ajustar en
   función de varios factores, como la complejidad del sistema, la experiencia del equipo de desarrollo, etc.
5. **Calcular los Puntos de Función ajustados**: Calcular los Puntos de Función ajustados multiplicando los Puntos de
   Función sin ajustar por el factor de ajuste.
6. **Revisar y validar la estimación**: Revisar y validar la estimación de los Puntos de Función para garantizar su
   precisión y realismo.
    
## Ejemplo de Estimación por Puntos de Función

Para ilustrar el proceso de estimación por Puntos de Función, consideremos el siguiente ejemplo:

Supongamos que un equipo de desarrollo de software está estimando los Puntos de Función de un sistema de gestión de
inventario. El equipo ha identificado las siguientes funciones del sistema:

- Crear un nuevo producto en el inventario.
- Actualizar la cantidad de un producto en el inventario.
- Generar un informe de inventario.
- Realizar una búsqueda de productos en el inventario.
- 