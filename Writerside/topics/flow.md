# flow

## Description

The `flow` topic is used to create flow diagrams

## Example

```d2
    vars: {
      d2-config: {
        layout-engine: elk
        theme-id: 200
        sketch: true
        pad: 125
      }
    }
    direction: down 
    "Inicio":{shape:oval; width:120; height:60}
    "Fin":{shape:oval; width:120; height:60}
    "Proceso":{shape:rectangle}
    "Proceso A":{shape:rectangle; direction:left}
    "Proceso B":{shape:rectangle; direction:right}
    "Decisión":{shape:diamond}
    "Conector":""{shape:circle; width:25; height:25}
    "Para": |md
                i=1; i<10; i++
            |{shape:hexagon}
    "Entrada":{shape:parallelogram}
    "Salida":{shape:document}
    "Inicio" -> "Proceso" -> "Decisión"
    "Conector" -> "Para"
    "Para"-> "Entrada" -> "Salida" -> "Fin"
    "Decisión" -> "Proceso A":Si{style.stroke: blue}
    "Decisión" -> "Proceso B":No{style.stroke: red}
    "Proceso A" -> "Conector"
    "Proceso B" -> "Conector"
```

### Details

The `flow` topic is used to create flow diagrams. It uses the `d2` code block with the following configuration:

```d2
    vars: {
      d2-config: {
        layout-engine: elk
        theme-id: 200
        sketch: true
      }
    }
```