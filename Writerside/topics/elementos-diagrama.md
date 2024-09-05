# Elementos de un diagrama de flujo

Los diagramas de flujo están compuestos por una serie de elementos que representan diferentes partes de un algoritmo o
proceso. Algunos de los elementos más comunes de un diagrama de flujo son:

1. **Inicio/Fin:**
    - Representa el inicio o fin de un algoritmo o proceso.
    - Se representa con un óvalo.
2. **Proceso:**
    - Representa una operación o acción que se realiza en el algoritmo.
    - Se representa con un rectángulo.
3. **Decisión:**
    - Representa una condición o pregunta que se evalúa en el algoritmo.
    - Se representa con un rombo.
4. **Conector:**
    - Representa la conexión entre diferentes partes de un diagrama de flujo.
    - Se representa con un círculo.
5. **Flecha:**
    - Representa la dirección del flujo de un proceso en el diagrama.
    - Se representa con una flecha.
6. **Entrada**:
    - Representa la entrada de datos en el algoritmo.
    - Se representa con un paralelogramo.
7. **Salida**:
    - Representa la salida de datos en el algoritmo.
    - Se representa con un documento.
8. **Para**:
    - Representa un bucle o ciclo en el algoritmo.
    - Se representa con un hexágono.
10. **Conector de página**:
    - Representa la conexión entre diferentes páginas de un diagrama de flujo.
    - Se representa con un círculo con una letra en su interior.
    - Se utiliza para indicar la continuación de un diagrama en otra página.
    - Se coloca en la parte inferior derecha de la página anterior y en la parte superior izquierda de la página
      siguiente.
    - La letra en el interior del conector indica la letra de la página siguiente.
    - Ejemplo: `(A)`.

Estos elementos son fundamentales para la creación y comprensión de un diagrama de flujo, ya que permiten representar de
forma clara y concisa la lógica y el flujo de ejecución de un algoritmo o proceso. Al utilizar símbolos gráficos y
conectarlos mediante flechas, se crea una representación visual que facilita la visualización y el análisis de un
algoritmo, lo que permite diseñar, analizar y documentar procesos de una manera efectiva y eficiente.

## Representación gráfica de los elementos

A continuación, se muestra la representación gráfica de los elementos de un diagrama de flujo:

<code-block lang="d2" layout="elk" theme="200" sketch="true">
    direction: down 
    "Inicio":{shape:oval; width:120; height:60}
    "Fin":{shape:oval; width:120; height:60}
    "Proceso":{shape:rectangle}
    "Proceso A":{shape:rectangle}
    "Proceso B":{shape:rectangle}
    "Decisión":{shape:diamond}
    "Conector":""{shape:circle; width:25; height:25}
    "Para": "inico; condicion; incremento"{shape:hexagon}
    "Entrada":{shape:parallelogram}
    "Salida":{shape:document}
    "Conector de página":A{shape:circle}
    "Inicio" -> "Proceso" -> "Decisión"
    "Conector" -> "Para"
    "Para"-> "Entrada" -> "Salida" -> "Fin"
    "Decisión" -> "Proceso A":Si
    "Decisión" -> "Proceso B":No
    "Proceso A" -> "Conector"
    "Proceso B" -> "Conector"
</code-block>
