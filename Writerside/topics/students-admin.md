# Sistema de Administración de Calificaciones

## Objetivo

Implementar un sistema en Java que permita ingresar calificaciones de varios estudiantes, calcular el promedio y mostrar
un informe final que incluya el rendimiento de cada estudiante, utilizando diferentes estructuras de control de flujo.

## Descripción

Esta aplicación debe:

1. Permitir ingresar las calificaciones de varios estudiantes.
2. Calcular el promedio de calificaciones de cada estudiante.
3. Evaluar si un estudiante aprobó o reprobó según su promedio.
4. Permitir ver los datos de todos los estudiantes registrados y su estatus final (aprobado o reprobado).

### La clase `Student`

Para representar a cada estudiante, crearemos una clase llamada `Student` con los siguientes atributos:

- `name`: El nombre del estudiante.
- `grades`: Un arreglo de calificaciones del estudiante.
- `average`: El promedio de las calificaciones del estudiante.

La clase `Estudiante` también tendrá los siguientes métodos:

- `calculateAverage()`: Calcula el promedio de las calificaciones del estudiante.
- `isApproved()`: Determina si el estudiante aprobó o reprobó según su promedio.
- `toString()`: Devuelve una representación en cadena del estudiante y su estatus final.

Así mismo deberá de contar con un constructor que inicialice el nombre del estudiante y el arreglo de calificaciones.

### La clase `GradeManager`

La clase `GradeManager` será la encargada de gestionar los estudiantes y mostrar el informe final. Esta clase tendrá los
siguientes métodos:

- `addStudent(Student student)`: Agrega un estudiante a la lista de estudiantes.
- `showReport()`: Muestra el informe final con los datos de todos los estudiantes y su estatus final.
- `main(String[] args)`: Método principal que se encargará de interactuar con el usuario para ingresar los datos de los
  estudiantes y mostrar el informe final.
- `getStudentData()`: Método auxiliar para obtener los datos de un estudiante (nombre y calificaciones) desde la
  consola.
- `showMenu()`: Muestra un menú de opciones para el usuario.

## Solución

### `Student`

```java
class Student {

    String name;
    int[] grades;
    double average;

    Student(String name, int[] grades) {
        this.name = name;
        this.grades = grades;
        calculateAverage();
    }

    void calculateAverage() {
        int sum = 0;
        for (int grade : grades) {
            sum += grade;
        }
        average = (double) sum / grades.length;
    }
    
    String gradesToString() {
    
        StringBuilder sb = new StringBuilder();
        for (int i = 0; i < grades.length; i++) {
            sb.append(grades[i]);
            if (i < grades.length - 1) {
                sb.append(", ");
            }
        }
        return sb.toString();
    }

    boolean isApproved() {
        return average >= 60;
    }

    @Override
    public String toString() {
        return """
                -------------------------
                Nombre: %s
                Calificaciones: %s
                Promedio: %.2f
                Estatus: %s
                -------------------------
                """.formatted(name, gradesToString(), average, 
                isApproved() ? "Aprobado" : "Reprobado");
    }
}
```

### `GradeManager`

```java
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

class GradeManager {

    List<Student> students = new ArrayList<>();

    void menu(){
      String menu = """
                Seleccione una opción:
                1. Agregar estudiante
                2. Mostrar informe
                3. Salir
                """;
      while(true){
        int option = Integer.parseInt(JOptionPane.showInputDialog(menu));
        switch (option) {
            case 1 -> addStudent();
            case 2 -> showReport();
            case 3 -> System.exit(0);
            default -> System.out.println("Opción inválida. Inténtalo de nuevo.");
        }
      }
    }
    
    void addStudent(){
    
      String name = JOptionPane.showInputDialog("Nombre del estudiante: ");
      ArrayList<Integer> grades = new ArrayList<>();
      int option;
      while(true){
        String grade = JOptionPane.showInputDialog("Calificación: ");
        grades.add(Integer.parseInt(grade));
        option = JOptionPane.showConfirmDialog(null, "¿Desea agregar otra calificación?");
        if(option == JOptionPane.NO_OPTION){
          break;
        }
      }
      students.add(new Student(name, grades.toArray(new Integer[0])));
    }
    
    void showReport(){
    
      StringBuilder sb = new StringBuilder();
        for (Student student : students) {
            sb.append(student).append("\n");
        }
        JOptionPane.showMessageDialog(null, sb.toString());
    }

    public static void main(String[] args) {
        GradeManager gradeManager = new GradeManager();
        while (true) {
            gradeManager.menu();
        }
    }
}
```

Analicemos el código:

En la función `menu`, se muestra un menú de opciones al usuario y se utiliza un `switch` para manejar las diferentes
opciones. Si el usuario elige la opción `1`, se llama al método `addStudent` para agregar un estudiante. Si elige la
opción `2`, se llama al método `showReport` para mostrar el informe final. Si elige la opción `3`, el programa se
cierra.

En el método `addStudent`, se solicita al usuario el nombre del estudiante y sus calificaciones. Se utiliza un bucle
`while` para permitir al usuario ingresar múltiples calificaciones. Cada calificación se agrega a un `ArrayList` de
calificaciones. Cuando el usuario decide no agregar más calificaciones, se crea un nuevo estudiante con el nombre y las
calificaciones ingresadas y se agrega a la lista de estudiantes.

En el método `showReport`, se recorre la lista de estudiantes y se muestra la información de cada estudiante en un
`JOptionPane`.

En el método `main`, se crea una instancia de `GradeManager` y se inicia un bucle infinito que muestra el menú de
opciones al usuario.

Con esta solución, hemos implementado un sistema de administración de calificaciones en Java que permite ingresar
calificaciones de varios estudiantes, calcular el promedio y mostrar un informe final con el rendimiento de cada
estudiante. El programa utiliza diferentes estructuras de control de flujo, como bucles y condicionales, para lograr
este objetivo.

## Conclusión

En este tutorial, hemos aprendido cómo implementar un sistema de administración de calificaciones en Java utilizando
diferentes estructuras de control de flujo. Hemos creado clases para representar a los estudiantes y gestionar sus
calificaciones, así como métodos para calcular el promedio y determinar si un estudiante aprobó o reprobó. También hemos
utilizado bucles y condicionales para interactuar con el usuario y mostrar un informe final con los datos de los
estudiantes.