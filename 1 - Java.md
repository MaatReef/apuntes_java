JVM -> Máquina Virtual de Java
JVM + las Librerías = JRE (Java Runtime Environment) 

El JDK contiene al JRE, más unas herramientas, para generar el bytecode.
JDK = JRE + Herramientas de desarrollo

El JRE es para usuarios normales
El JDK es para programadores, con funcionalidades extras.

El JDK es el ambiente para ejecutar aplicaciones Java y además posee varias herramientas de desarrollo
    - El JDK son las herramientas de desarrollo (como el compilador) y también tiene el JRE incluido.

EL JRE es el ambiente para ejecutar una aplicación Java
    - Si solo queremos ejecutar una aplicación Java, el JRE (Java Runtime Environment) es suficiente.
    JRE = JVM + Librerías

----------------------------------------------------
5. Compilando Código

En un archivo txt..

public class Ejemplo {
    
    public static void main(String[] args) {
        System.out.prinln("Hola Mundo"); 
    }
}


* ¡Correcto! Aún no sabemos que significan todas esas palabras, pero tranquilo, va a quedar claro después. En este momento, solo nos basta saber que la entrada de una aplicación Java es siempre la función/método public static void main(String[] args)


El archivo a guardar debe ser el mismo nombre de la clase.
Ejemplo.java

Desde la consola hacemos
    javac Ejemplo.java  -> Para compilar el archivo y generar el bytecode para que lo interprete la máquina

Desde consola
    java Ejemplo        -> Vemos el hola mundo.

Los errores de compilación surgen con errores de sintaxis y demás


1ª Durante la compilación ocurre una verificación sintáctica del código fuente.
2ª En la compilación y ejecución pueden aparecer errores.
3ª La JVM ejecuta Bytecode.
4ª El compilador genera Bytecode en caso el código fuente no presente ningún error sintáctico.


En esta clase escribiste tu primer código Java y aprendimos:

Cuál es la diferencia entre JRE y JDK.
Cómo compilar el código fuente de Java desde la línea de comandos (javac).
Cómo ejecutar Bytecode en la línea de comando (java).
Un programa Java debe escribirse dentro de una clase (class).
Cada instrucción Java debe terminar con ;.
Para abrir y cerrar un bloque usaremos las llaves {}.
Un programa Java tiene una entrada que es una función (método) main.
Para imprimir algo en la consola, usamos la declaración System.out.println ().
----------------------------------------------------
6. Tipo Entero:

Usamos la palabra reservada int, solo entero

public class TipVariable{

    public static void main(String[] args) {
        System.out.println("Hola Mundo");
        
        int edad = 28;
        System.out.println(edad);
        
        edad = 28;
        System.out.println(edad);
        
        edad = 45 + 65;
        System.out.println(edad);
        
        edad = 30;
        System.out.println("Mi edad es " + edad);
    }

}

----------------------------------------------------
04. Tipo Double, para decimales

Se pueden sosbrescribir las variables.
Double para decimales, ya que tiene el doble de espacio en memoria que el tipo int, si necesitamos la precision de las decimales usar double.

public class TipVariable{

    public static void main(String[] args) {
        
        double salario  = 1250.50;
        System.out.println(salario);

        double edad = 28;
        double salarioMitad = salario/2;

        System.out.println(salarioMitad);
        
        int division = 1250 / 3;
        System.out.println(division);
    }

}


double peso = 4.0;
int cantidad = 10;
System.out.println (peso * cantidad);
Debería imprimir 40.0
Este código es correcto, cuando hacemos operaciones entre enteros y dobles, el resultado es double.

double precio = 5.5;
int tickets = 4;
System.out.println (precio * tickets);
Debe imprimir 22.0
Este código es correcto, cuando hacemos operaciones entre enteros y dobles, el resultado es double.

int dia = 4; 
int otroDia = 4 + dia;
System.out.println (otroDia);
Debe imprimir 8
Este código es correcto, no hay duda al sumar 2 números enteros.


----------------------------------------------------
8. Conversiones. 

public class TipVariable{

    public static void main(String[] args) {
        
        double variable1 =  230.89;
        int variable1Entero = (int) variable1; // Cast
        System.out.println(variable1Entero);


        double resultado = variable1 + variable1Entero;
        System.out.println(resultado);
        
        // Con int perdemos precision, con decimal es usamos decimales.
        int resultado1 = (int) variable1 + variable1Entero;
        System.out.println(resultado1);
        
        // Para comentar 
        // Int soporta un valor de 32 bits; 2 a la 31 positivo y negativo.

        long prueba = 2032302930293023920L;
        // Para números más grandes usamos long, para 64 bits; 2 a la 63 prositivo y negativo.
        // Con una L mayúsucula al final

        short numeroPequeno = 13555;
        // Para números de a 2 a las 16;

        byte numeroAunMasPequeño = 15;
        // 8 bits, más usado par a procesar archivos

        float numeroDeciamalPequeno = 2.5F;
        // Más pequeño y le agregamos una F al final.

        // *Usaremos Más int y Double.

    }

}

----------------------------------------------------
02-  Caracteres y Strings

¡Correcto! Recuerda, un String se declara con comillas dobles " y puede tener cero o más caracteres. Un char se declara con comillas simples ' y solo puede usar un carácter.

public class TipVariable{

    // shurtcout con main
    public static void main(String[] args) {
        
        // Char soporta un caracter a la vez y numeros, tabla ASCI
        char caracter = 'a';
        
        System.out.println(caracter);
        
        caracter = 65;
        System.out.println(caracter); // Nos da la A, según la tabla ASCI

        caracter = 65 + 1;
        char segundoCaracter = (char) (caracter + 1); // Forzamos que la suma se exprese como Char, no como int
        System.out.println(segundoCaracter);   // Nos da C

        String palabra = "Maat Reef";
        System.out.println(palabra); // Obtenemos el string
        
        palabra = palabra + "2020";
        System.out.println(palabra); // Concatena los Strings



    }

}


----------------------------------------------------
05. Variables y memoria

public class TipVariable{

    // shurtcout con "main"
    public static void main(String[] args) {
        
        int numero1 = 5;

        int numero2 = 9;

        System.out.println(numero2);
        
        numero2 = numero1;              // 5
        System.out.println(numero2);    
        
        numero1 = 88;
        System.out.println(numero2);  
        // 5 se mantendrá, las variables en Java reciben el valorm, lo guardan en sí, no direcciones o punteros en memoria.
        
        

    }

}
----------------------------------------------------
02. Test If

public class TipVariable{

    // shurtcout con "main"
    public static void main(String[] args) {
        
        System.out.println();

        int edad = 8;
        int cantidad = 2;

        if (edad >= 18) {
            System.out.println("Usted puede entrar");
        } else {                // Sino
            if (cantidad >= 2) {
                System.out.println("Sip, sos menor pero venís acompañado");
            } else {
                System.out.println("Nop");
            }
        }



    }

}

----------------------------------------------------
05. Boolean .. Solo true o false

public class TipVariable{

    // shurtcout con "main"
    public static void main(String[] args) {
        
        System.out.println();

        int edad = 21;
        int cantidadPersonas = 2;

        boolean esPareja = cantidadPersonas > 1;
        boolean puedeEntrar = edad >= 18 && esPareja
        System.out.println("El valor de la condicion es: " + esPareja); // Es True

        if (puedeEntrar) {
            System.out.println("Usted puede entrar, sea bienvenido");
        } else {                // Sino
            System.out.println("No está permitida su entrada");
        }

    }

}

----------------------------------------------------
09. Scope e Inicialización

El Scope va dentro de las {}
Todo boolean por defecto es false..

Se declaran las variables, pero se deben inicializar.
----------------------------------------------------
02. Ciclo While

public class TipVariable{        
    public static void main(String[] args) {
        
        int contador = 0;
        while(contador <= 10) { // Mientras que (condicion)
            // Ejecuta esto
            System.out.println(contador);
            //contador = contador + 1;
            //contador += 1;
            contador++;
        }
    }
}

En la expresión condicional while es posible usar cualquier operador de comparación: < (menor), > (mayor), <= (menor o igual), >= (mayor o igual), == (igual a) y != (diferente de)) y cualquier operador lógico (&& (and), || (or)).
¡Eso es! Todos los operadores lógicos y de comparación son válidos en la expresión condicional while. ¡Úsalos sabiamente!

El while siempre necesitará una expresión condicional que definirá cuándo se debe romper el ciclo.
¡Muy bien! Recuerda, esta expresión condicional deberá ingresarse entre los paréntesis del while y podrás usar cualquiera de los operadores de comparación y operadores lógicos aprendidos en el capítulo 6.





----------------------------------------------------
06. Scope Ciclos

public class TipVariable{        
    public static void main(String[] args) {
        
        int contador = 0;
        int total = 0;
        while(contador <= 10) { 
            total = total + contador;
            contador++;
        }
        System.out.println(total);     // Obtenemos 55 la suma de todos los numeros del 1 al 10
    }
}


----------------------------------------------------
Ciclo For

Usamos for cuando no vamos a necesitar la variable que será incrementada, fuera del contexto de while.

public class TipVariable{        
    public static void main(String[] args) {
                // variable     condicion        ejecutar al final        
        for (int contador = 0; contador <= 10 ; contador++){ 
            System.out.println(contador);
        }
    }
}
---------------------------------------------------- 
Ciclos Anexados:

public class TipVariable{        
    public static void main(String[] args) {

        for(int contador = 1; contador <= 10; contador++) {
        
            for(int multiplicacion = 0; multiplicacion <= 10; multiplicacion++) {

                System.out.print(contador * multiplicacion);
                System.out.print(" ");
                // System.out.println(contador * multiplicacion);
            }
            System.out.println();
        }

    }
}

Tabla de multiplicacion hasta el número 10
----------------------------------------------------
Ciclos Break:
Imprimir una matriz de 10*10
public class TipVariable{        
    public static void main(String[] args) {

        for(int fila = 0; fila <= 10; fila++){
            for(int columna = 0; columna <= 10; columna++){
                System.out.print("*");
                System.out.print("");
            }
            System.out.println();
            
        }

    }
}

System.out.print("*");  -> Con print solo imprimimos todo uno al lado del otro.
Para una matriz triangular

public class TipVariable{        
    public static void main(String[] args) {

        for(int fila = 0; fila <= 10; fila++){
            for(int columna = 0; columna <= 10; columna++){
                if (columna > fila){
                    break;
                }
                System.out.print("*");
                System.out.print("");
            }
            System.out.println();
            
        }

    }
}

*
**
***
****
*****
******
*******
********
*********
**********
***********

Lo mismo que decir

public class TipVariable{        
    public static void main(String[] args) {

        for(int fila = 0; fila <= 10; fila++){
            for(int columna = 0; columna < fila; columna++){
            
                System.out.print("*");
                System.out.print("");
            }
            System.out.println();
            
        }

    }
}

Para la ejecución del bucle más interno que contiene el comando break y continúa ejecutando los bucles más externos
¡Muy bien! El descanso solo interrumpirá el ciclo de repetición más interno que lo contiene.


En este ejercicio opcional, tu desafío es imprimir los factoriales del 1 al 10.

¿Recuerdas el factorial? ¿No? No hay problema, sigue las reglas:

El factorial de 0 es 1.
El factorial de 1 es (0!) * 1 = 1.
El factorial de 2 es (1!) * 2 = 2
El factorial de 3 es (2!) * 3 = 6
El factorial de 4 es (3!) * 4 = 24
El factorial de un número n es n * n-1 * n-2 ... hasta n = 1.
O sea:

El factorial de 4! = 1 x 2 x 3 x 4 = 24
El factorial de 6! = 1 x 2 x 3 x 4 x 5 x 6 = 720


class Factorial {

    public static void main(String[] args) {
        int factorial = 1;
        for (int i = 1; i < 11; i++) {
            factorial *= i;
            System.out.println("Factorial de " + i + " = " + factorial);
        }
    }

}


El factorial siempre es el producto de números enteros consecutivos de 1 hasta el propio número con el que estamos trabajando. Ejemplo: Factorial de 4 = 4 x 3 x 2 x 1 = 24. Es igual a decir que factorial de 4 = 4 x 3! = 24. Usando esta última lógica podemos resolver algunos problemas, pues vamos usando el número que tenemos multiplicado por el factorial del número anterior.
