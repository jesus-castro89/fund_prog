# Ejemplo de Programa mediante menús de interacción

Dentro de Java el uso de los menús de interacción, tanto en formato de CLI como GUI, es una forma efectiva de presentar
opciones al usuario y permitirle seleccionar una acción específica. En este caso, se presentará un ejemplo de cómo
implementar un menú de interacción en Java utilizando ventanas emergentes `JOptionPane`.

## Problema

Se desea implementar un programa que permita la gestión de productos en un inventario a través de un menú de
interacción. Las opciones del menú serán las siguientes:

1. Agregar producto
2. Mostrar inventario
    * Deberás listar todos los productos en el inventario, mostrando su código, nombre, precio, cantidad y descripción.
    * Si el inventario está vacío, mostrar un mensaje indicando que no hay productos en el inventario.
    * Si el inventario no está vacío, mostrar un mensaje indicando la cantidad total de productos en el inventario.
    * Al finalizar la lista de productos, mostrar un mensaje indicando que se ha completado la lista y se mostrara el
      montón total de productos. (Sumatoria de (precio * cantidad) de cada producto)
3. Buscar producto
4. Actualizar producto
5. Eliminar producto
6. Salir

Además, cada producto tendrá los siguientes atributos:

- Código
- Nombre
- Precio
- Cantidad
- Descripción

## Solución

Para resolver este problema, se utilizará una clase `Producto` para representar los productos en el inventario. Luego,
se creará una clase `Inventario` que contendrá una lista de productos y métodos para realizar las operaciones de
agregar, mostrar, buscar, actualizar y eliminar productos.

A continuación, se muestra la implementación de las clases `Producto` e `Inventario`:

```java
class Producto {
    int codigo;
    String nombre;
    double precio;
    int cantidad;
    String descripcion;

    Producto() {
        this.codigo = Integer.parseInt(JOptionPane.showInputDialog(
                     "Ingrese el código del producto:"));
        this.nombre = JOptionPane.showInputDialog(
                     "Ingrese el nombre del producto:");
        this.precio = Double.parseDouble(JOptionPane.showInputDialog(
                     "Ingrese el precio del producto:"));
        this.cantidad = Integer.parseInt(JOptionPane.showInputDialog(
                     "Ingrese la cantidad del producto:"));
        this.descripcion = JOptionPane.showInputDialog(
                     "Ingrese la descripción del producto:");
    }
    
    getProductTotal() {
        return precio * cantidad;
    }
    
    @Override
    public String toString() {
        return """ 
               Código: %d
               Nombre: %s
               Precio: %.2f
               Cantidad: %d
               Descripción: %s
               """.formatted(codigo, nombre, precio, cantidad, 
               descripcion);
    }
}
```

De esta forma, se ha definido la clase `Producto` con los atributos mencionados y un constructor que solicita al
usuario los datos del producto a través de ventanas emergentes `JOptionPane`.

```java
import javax.swing.JOptionPane;
import java.util.ArrayList;

class Inventario {

    ArrayList<Producto> productos;

    Inventario() {
    
        productos = new ArrayList<>();
    }

    void agregarProducto() {
    
        productos.add(new Producto());
    }

    void mostrarInventario() {
    
        if (productos.isEmpty()) {
        
            JOptionPane.showMessageDialog(null, 
               "No hay productos en el inventario.");
        } else {
            double total = 0;
            for (Producto producto : productos) {
                JOptionPane.showMessageDialog(null, producto.toString());
                total += producto.getProductTotal();
            }
            JOptionPane.showMessageDialog(null, 
               "Cantidad total de productos en el inventario: " + productos.size());
            JOptionPane.showMessageDialog(null, "
               Monto total de productos en el inventario: " + total);
        }
    }

    void buscarProducto() {
    
        int codigo = Integer.parseInt(JOptionPane.showInputDialog(
                     "Ingrese el código del producto a buscar:"));
        for (Producto producto : productos) {
        
            if (producto.codigo == codigo) {
            
                JOptionPane.showMessageDialog(null, producto.toString());
                return;
            }
        }
        JOptionPane.showMessageDialog(null, "Producto no encontrado.");
    }

    void actualizarProducto() {
    
        int codigo = Integer.parseInt(JOptionPane.showInputDialog(
                     "Ingrese el código del producto a actualizar:"));
        for (Producto producto : productos) {
        
            if (producto.codigo == codigo) {
            
                producto = new Producto();
                return;
            }
        }
        JOptionPane.showMessageDialog(null, "Producto no encontrado.");
    }

    void eliminarProducto() {
    
        int codigo = Integer.parseInt(JOptionPane.showInputDialog(
                     "Ingrese el código del producto a eliminar:"));
        for (Producto producto : productos) {
        
            if (producto.codigo == codigo) {
            
                productos.remove(producto);
                return;
            }
        }
        JOptionPane.showMessageDialog(null, "Producto no encontrado.");
    }
}
```

Ahora analicemos cada método de la clase `Inventario`:

### Método `agregarProducto`

Este método permite agregar un nuevo producto al inventario. Al llamar a este método, se crea un nuevo objeto
`Producto` y se agrega a la lista de productos.

### Método `mostrarInventario`

Este método muestra todos los productos en el inventario, incluyendo su código, nombre, precio, cantidad y descripción.
Al finalizar la lista de productos, se muestra la cantidad total de productos en el inventario y el monto total de los
productos (precio * cantidad).

```java
void mostrarInventario() {
    if (productos.isEmpty()) {
        JOptionPane.showMessageDialog(null, "No hay productos en el inventario.");
    } else {
        double total = 0;
        for (Producto producto : productos) {
            JOptionPane.showMessageDialog(null, producto.toString());
            total += producto.getProductTotal();
        }
        JOptionPane.showMessageDialog(null, "Cantidad total de productos en el inventario: " + productos.size());
        JOptionPane.showMessageDialog(null, "Monto total de productos en el inventario: " + total);
    }
}
```

Podemos observar que se recorre la lista de productos con un foreach y se muestra la información de cada producto
utilizando el método `toString` de la clase `Producto`. Además, se calcula el monto total de los productos sumando el
resultado de `precio * cantidad` de cada producto y se almacena en la variable `total`. Al finalizar la lista de
productos, se muestran la cantidad total de productos en el inventario y el monto total de los productos.

### Método `buscarProducto`

Este método permite buscar un producto en el inventario por su código. Al ingresar el código del producto, se recorre
la lista de productos y se muestra la información del producto si se encuentra.

```java
void buscarProducto() {
    int codigo = Integer.parseInt(JOptionPane.showInputDialog("Ingrese el código del producto a buscar:"));
    for (Producto producto : productos) {
        if (producto.codigo == codigo) {
            JOptionPane.showMessageDialog(null, producto.toString());
            return;
        }
    }
    JOptionPane.showMessageDialog(null, "Producto no encontrado.");
}
```

Al recorrer la lista de productos, se compara el código del producto con el código ingresado por el usuario. Si se
encuentra un producto con el código ingresado, se muestra la información del producto. En caso contrario, se muestra un
mensaje indicando que el producto no fue encontrado.

> **Nota:** En este caso, se utiliza un bucle `for-each` para recorrer la lista de productos. Este tipo de bucle es
> útil cuando se desea recorrer todos los elementos de una colección sin necesidad de utilizar un índice explícito.

> **Nota:** El método `toString` se utiliza para representar un objeto como una cadena de texto. En este caso, se
> sobrescribe el método `toString` en la clase `Producto` para mostrar la información del producto de una forma
> legible.

> **Nota:** Se usa la palabra clave `return` para salir del bucle `for-each` una vez que se ha encontrado el producto
> buscado. Esto evita seguir recorriendo la lista de productos una vez que se ha encontrado el producto. Además de que
> se sale del método `buscarProducto` una vez que se ha encontrado el producto.

### Método `actualizarProducto`

Este método permite actualizar un producto en el inventario por su código. Al ingresar el código del producto, se
recorre la lista de productos y se crea un nuevo objeto `Producto` con los datos actualizados.

### Método `eliminarProducto`

Este método permite eliminar un producto del inventario por su código. Al ingresar el código del producto, se recorre
la lista de productos y se elimina el producto si se encuentra.

Finalmente, se implementará el menú de interacción principal del programa:

```java
public class MenuInteractivo {
    public static void main(String[] args) {
        Inventario inventario = new Inventario();
        int opcion = 0;

        do {
            opcion = Integer.parseInt(JOptionPane.showInputDialog(
                     "Menú de opciones
                     \n1. Agregar producto
                     \n2. Mostrar inventario
                     \n3. Buscar producto
                     \n4. Actualizar producto
                     \n5. Eliminar producto
                     \n6. Salir"));

            switch (opcion) {
                case 1:
                    inventario.agregarProducto();
                    break;
                case 2:
                    inventario.mostrarInventario();
                    break;
                case 3:
                    inventario.buscarProducto();
                    break;
                case 4:
                    inventario.actualizarProducto();
                    break;
                case 5:
                    inventario.eliminarProducto();
                    break;
                case 6:
                    JOptionPane.showMessageDialog(null, "Saliendo del programa");
                    break;
                default:
                    JOptionPane.showMessageDialog(null, "Opción inválida");
            }
        } while (opcion != 6);
    }
}
```