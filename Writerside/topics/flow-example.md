# Ejemplo de Diagrama de Flujo

<code-block lang="d2" layout="elk" theme="200" width="50%" height="50%">
direction: down
            Inicio: {shape: oval}
            Proceso1: {shape: rectangle}
            Proceso2: {shape: rectangle}
            Proceso3: {shape: rectangle}
            Decisión: {shape: diamond}
            "": {shape: circle; width: 20; height: 20}
            Entrada: {shape: parallelogram}
            Salida: {shape: document}
            Final: {shape: oval}
            Inicio -> Entrada
            Entrada -> Proceso1
            Proceso1 -> Decisión
            Decisión -> Proceso2: Si
            Decisión -> Proceso3: No
            Proceso2 -> ""
            Proceso3 -> ""
            "" -> Salida
            Salida -> Final
</code-block>
