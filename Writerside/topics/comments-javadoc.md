# Los comentarios JavaDoc

Los comentarios JavaDoc son una forma de documentar el código en Java. Estos comentarios se utilizan para generar
documentación a partir del código fuente. Los comentarios JavaDoc comienzan con `/**` y terminan con `*/`. Los
comentarios JavaDoc pueden contener etiquetas que se utilizan para formatear la documentación.

### Ejemplo de Comentario JavaDoc

```java
/**
 * Esta clase representa un libro.
 */
class Libro {
    /**
     * El título del libro.
     */
    String titulo;
    /**
     * El autor del libro.
     */
    String autor;

    /**
     * Crea un nuevo libro con el título y autor especificados.
     *
     * @param titulo El título del libro.
     * @param autor El autor del libro.
     */
    Libro(String titulo, String autor) {
        this.titulo = titulo;
        this.autor = autor;
    }

    /**
     * Devuelve el título del libro.
     *
     * @return El título del libro.
     */
    String getTitulo() {
        return titulo;
    }

    /**
     * Establece el título del libro.
     *
     * @param titulo El título del libro.
     */
    void setTitulo(String titulo) {
        this.titulo = titulo;
    }

    /**
     * Devuelve el autor del libro.
     *
     * @return El autor del libro.
     */
    String getAutor() {
        return autor;
    }

    /**
     * Establece el autor del libro.
     *
     * @param autor El autor del libro.
     */
    void setAutor(String autor) {
        this.autor = autor;
    }
}
```

## Etiquetas JavaDoc

Las etiquetas JavaDoc se utilizan para formatear la documentación en los comentarios JavaDoc. A continuación se muestran
algunas de las etiquetas más comunes:

| Etiqueta      | Descripción                                                         |
|---------------|---------------------------------------------------------------------|
| `@param`      | Describe un parámetro de un método o constructor.                   |
| `@return`     | Describe el valor de retorno de un método.                          |
| `@see`        | Hace referencia a otra clase o método.                              |
| `@since`      | Indica desde qué versión está disponible un método o clase.         |
| `@deprecated` | Indica que un método o clase está obsoleto y se debe evitar su uso. |
| `@author`     | Indica el autor del código.                                         |
| `@version`    | Indica la versión del código.                                       |
| `@link`       | Crea un enlace a una clase o método.                                |
