<!--
Posible prompt:
<prompt>
Tengo un cuestionario con preguntas sobre "Clases y Objetos". Debes tener en cuenta que los conocimientos previos que tengo (y por tanto tus respuestas deben ser adaptadas), son:
- C/C++ sin orientación a objetos.
- Temas de Java previos: ninguno.

Cada respuesta debe tener entre 2 - 4 párrafos de longitud (sin contar los trozos de código).

Por favor, escribe en impersonal las respuestas.

</prompt>
----
-->

# TEMA 1. Clases y objetos

## 1. ¿Cuáles son las cuatro características básicas de la programación orientada a objetos? Describe brevemente cada una

### Respuesta
Las cuatro características básicas de la programación orientada a objetos son estas:

1.Encapsulación: Consiste en ocultar los detalles internos de un objeto y exponer solo lo necesario. Los datos suelen ser privados y se accede a ellos mediante métodos (getters y setters), lo que protege la información y evita usos incorrectos.

2.Abstracción: Permite representar solo lo esencial de un objeto, ignorando los detalles irrelevantes. Se centra en qué hace el objeto y no en cómo lo hace, facilitando el diseño y la comprensión del sistema.

3.Herencia: Es la capacidad de crear nuevas clases a partir de otras, reutilizando sus atributos y métodos. La clase hija hereda comportamientos de la clase padre y puede ampliarlos o modificarlos.

4.Polimorfismo: Permite que un mismo método se comporte de distintas formas según el objeto que lo implemente. Esto se logra, por ejemplo, mediante la sobrescritura de métodos, haciendo el código más flexible y extensible.


## 2. Cita cuatro lenguajes populares que permitan la programación orientada a objetos

### Respuesta
Java, C++, Python, C#.

## 3. Los paradigmas anteriores a la POO, ¿Qué es la **programación estructurada**? y, todavía mejor, ¿Qué es la **programación modular**?

### Respuesta
La programación estructurada es un paradigma que organiza el código mediante estructuras de control claras, como secuencias, condicionales y bucles. Su objetivo es mejorar la legibilidad el mantenimiento de los programas, evitando saltos desordenados en el flujode ejecución.
La programación modular amplía esta idea dividiendo el programa en módulos independientes, cada uno encargado de una función concreta. Esto permite deaarrollar y mantener cada parte por separado, reduciendo la complejidad y facilitando la reutilización del código.

## 4. ¿Qué tres elementos definen a un objeto en programación orientada a objetos?

### Respuesta
Un objeto se define por tres elementos: Identidad, Estado y Comportamiento.

## 5. ¿Qué es una clase? ¿Es lo mismo que un objeto? ¿Qué es una instancia? ¿Todos los lenguajes orientados a objetos manejan el concepto de clase?

### Respuesta
Una clase es una plantilla o modelo que define los atributos y métodos que tendrán los objetos. Sirve como una descripción general de cómo serán y qué podrán hacer esos objetos.
Una clase no es lo mismo que un objeto. El objeto es la entidad concreta creada a partir de una clase, mientras que la clase es solo la definición.
Una instancia es precisamente ese proceso y resultado de crear un objeto a partir de una clase;es decir, un objeto es una instancia de una clase.
No todos los lenguajes orientados a objetos manejan el concepto de clase. Algunos, como Java o C++, están basados en clases, mientras que otros, como JavScript, utilizan un modelo orientado a objetos basado en prototipos en lugar de clases tradicionales.

## 6. ¿Dónde se almacenan en memoria los objetos? ¿Es igual en todos los lenguajes? ¿Qué es la **recolección de basura**? 

### Respuesta
En la mayoría de los lenguajes orientados a objetos, los objetos se almacenan en el heap mientras que las variables que los referencian suelen almacenarse en la pila. No obstante, no es igual en todos los lenguajes, ya que algunos permiten o requieren gestionar la memoria de forma distinta, como en C++.
La recolección de basuras es un mecanismo automático de gestión de memoria mediante el cual el sistema detecta los objetos que ya no se utilizan y libera el espacio que ocupan. Esto evita fugas de memoria y simplifica el trabajo del programador, ya que no es necesario liberar la memoria manualmente.

## 7. ¿Qué es un método? ¿Qué es la **sobrecarga de métodos**? 

### Respuesta
Un método es un bloque de código dentro de una clase que realiza una acción específica. Puede recibir parámetros y devolver un resultado, o no devolver nada. Los métodos permiten organizar y reutlizar el código.
La sobrecarga de métodos ocurre cuando una misma clase tiene varios métodos con el mismo nombre, pero diferente número o tipo de parámetros. Esto permite usar el mismo método de distintas formas según los datos que se le pasen.

## 8. Ejemplo mínimo de clase en Java, que se llame Punto, con dos atributos, x e y, con un método que se llame `calculaDistanciaAOrigen`, que calcule la distancia a la posición 0,0. Por sencillez, los atributos deben tener visibilidad por defecto. Crea además un ejemplo de uso con una instancia y uso del método

### Respuesta
class Punto {
  int x;
  int y;
  double calcularDistanciaAOrigen(){
    return Math.sqrt(x*x + y*y);
  }
 }

 Ejemplo: 

 public class Main {
   public static void main(String[] args){
     Punto p = new Punto();
     p.x = 3;
     p.y = 4;
     double distancia = p.calcularDistanciaAOrigen();
     System.out.println("Distancia: " + distancia);
    }
  }

## 9. ¿Cuál es el punto de entrada en un programa en Java? ¿Qué es `static` y para qué vale? ¿Sólo se emplea para ese método `main`? ¿Para qué se combina con `final`?

### Respuesta
El punto de entrada de un programa en Java es el método main. Es el primer método que se ejecuta cuando se inicia el programa.
Static indica que el miembro pertenece a la clase y no a un objeto.
No, aunque main debe ser static porque Java lo llama sin crear un objeto, se puede usar static en cualquier método o atributo que quieras que pertenezca a la clase y no a sus objetos.
Final significa que el valor no puede cambiar. Combinado con static, crea constantes de clase.

## 10. Intenta ejecutar un poco de Java de forma básica, con los comandos `javac` y `java`. ¿Cómo podemos compilar el programa y ejecutarlo desde linea de comandos? ¿Java es compilado? ¿Qué es la **máquina virtual**? ¿Qué es el *byte-code* y los ficheros `.class`?

### Respuesta
Para compilar y ejecutar un programa en Java desde la línea de comandos:
1. javac HolaMundo.java
2. java HolaMundo

Java se compila a byte-code, un código intermedio queno se ejecuta directamente en el procesador.
La máquina virtual interpreta el byte-code y lo ejecuta en cualquier sistema operativo.
Los archivos .class contienen el byte-code generado al compilar los .java.

## 11. En el código anterior de la clase `Punto` ¿Qué es `new`? ¿Qué es un **constructor**? Pon un ejemplo de constructor en una clase `Empleado` que tenga DNI, nombre y apellidos

### Respuesta
En Java la palabra clave new crea un nuevo objeto en memoria.
Un constructor es un método especial de una clase que: 
1. Se llama automáticamente al crear el objeto
2. Tiene el mismo nombre que la clase
3. Sirve para inicializar los atributos del objeto
Ejemplo:
Empleado(String DNI, String nombre, String apellidos){
  this.DNI = DNI;
  this.nombre = nombre;
  this.apellidos = apellidos;
}

## 12. ¿Qué es la referencia `this`? ¿Se llama igual en todos los lenguajes? Pon un ejemplo del uso de `this` en la clase `Punto`

### Respuesta
En Java, this es una referencia al propio objeto actual.
No todos los lenguajes usan this;por ejemplo, en Python se utiliza self, y en C++ también se utiliza this pero con diferencias.
Ejemplo:

class Punto {
  int x;
  int y;
  Punto(int x, int y){
    this.x = x;
    this.y = y;
  }

## 13. Añade ahora otro nuevo método que se llame `distanciaA`, que reciba un `Punto` como parámetro y calcule la distancia entre `this` y el punto proporcionado

### Respuesta
double distanciaA (Punto otro) {
  int dx = this.x - otro.x;
  int dy = this.y - otro.y;
  return Math.sqrt(dx*dx + dy*dy);
}

## 14. El paso del `Punto` como parámetro a un método, es **por copia** o **por referencia**, es decir, si se cambia el valor de algún atributo del punto pasado como parámetro, dichos cambios afectan al objeto fuera del método? ¿Qué ocurre si en vez de un `Punto`, se recibiese un entero (`int`) y dicho entero se modificase dentro de la función? 

### Respuesta


## 15. ¿Qué es el método `toString()` en Java? ¿Existe en otros lenguajes? Pon un ejemplo de `toString()` en la clase `Punto` en Java

### Respuesta


## 16. Reflexiona: ¿una clase es como un `struct` en C? ¿Qué le falta al `struct` para ser como una clase y las variables de ese tipo ser instancias?


### Respuesta


## 17. Quitemos un poco de magia a todo esto: ¿Como se podría “emular”, con `struct` en C, la clase `Punto`, con su función para calcular la distancia al origen? ¿Qué ha pasado con `this`?

### Respuesta
