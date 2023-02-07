# Activitats:

## Activitats debug:

### Factorial:

El factorial d'un nombre és el resultat de multiplicar el número per ell mateix -1 tantes vegades com  siguin necessàries fins arrivar a 1.

Per exemple el factorial de 5 és:

5 * 4 * 3 * 2 * 1

![image](https://user-images.githubusercontent.com/110727546/206031980-55e59610-42bb-4cc6-9b5f-039d7f67e185.png)

Fes una funció factorial que rebi un número com paràmetre i retorni el seu factorial.

Es demana:

- Codi del programa.
```
public class factorial {
    public static void main(String[] args) {
        System.out.println("El factorial és:" + factorial(4));
    }
    public static int factorial(int numero){

        if (numero > 1){
            return numero * factorial(numero-1);
        }
        return numero;
    }
}
```
- Captura de pantalla amb un punt d'interrupció que deixi veure totes les crides a la funció (agafeu un valor menor a 10).
![imatge](https://user-images.githubusercontent.com/114901284/217346460-edafb55e-11e2-4dec-893c-17c7ffdcd5dd.png)

### Taula de multiplicar:

Fes un programa que crea una matriu de números del 1 al 10.
Aquest programa rep per argument d'entrada un número sencer i retorna per terminal la taula de multiplicar d'aquest número multiplicant el argument per cada valor de la matriu.

Es demana:

- Codi del programa.
```
import java.util.Arrays;

public class multiplicar {
    public static void main(String[] args) {
        System.out.println(Arrays.toString(multiplicar(2)));
    }
    public static int[] multiplicar(int argument){
       int[] taula = new int[]{1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
        for (int i = 0; i < taula.length; i++) {
            taula[i] = taula[i] * argument;
        }
        return taula;
    }
}

```
- Captura de pantalla de com li passeu a IntelliJ com argument del programa un número. (Mireu exemple findAverage).
![imatge](https://user-images.githubusercontent.com/114901284/217346853-4dd822be-7ae2-42af-bb95-fea320fed61a.png)

- Captura de com feu un punt d'interrupció al bucle de creació de la matriu i mostreu els valors de la matriu.

No he fet un bucle, he creat la matriu directament

- Captura de punt d'interrupció al bucle de multiplicació i com modifiqueu a ma els valors de la matriu de números per a que l'execució retorni el número 1 10 vegades quan l'argument d'entrada era 1.
No se que he de posar aqui
