# Enunciat:

Per als tres problemes de Caixa negra que ja heu fet genereu les proves unitàries de partició equivalent i de valors límits amb Junit i comproveu que funcionen.

## Exemple Pizzeria Pepe:

### Codi programa:

```
public class pizzeriaPepe {

    public static boolean potCarregar(int pizzes){
        boolean pot = false;
        if(pizzes <=10 && pizzes >= 1){
            pot = true;
        }
        return pot;
    }
}
```

### Codi programa de test:

```
import org.junit.jupiter.api.*;


class pizzeriaPepeTest {

 
    @Test //Valor entre els límits
    void prova1() {
        boolean pot = pizzeriaPepe.potCarregar(3);
        Assertions.assertTrue(pot);
    }
    
    @Test //Valor superior al límit superior
    void prova2() {
        boolean pot = pizzeriaPepe.potCarregar(11);
        Assertions.assertFalse(pot);
    }


    @Test //Valor inferior al límit inferior
    void prova3() {
        boolean pot = pizzeriaPepe.potCarregar(-2);
        Assertions.assertFalse(pot);
    }
    
    
    @Test//Valor no és un número
    void prova4() {
        Exception exception = Assertions.assertThrows(NumberFormatException.class, () -> {
            pizzeriaPepe.potCarregar(Integer.parseInt("cinc"));
        });
}
```
## Jean Cloud
### Test
```

import org.junit.jupiter.api.*;

public class JeanCloudTest {
    @Test
        //Valor entre els límits
    void prova1() {
        int pot = JeanCloud.potPortar(600,600);
        System.out.println(pot);
    }

    @Test //Valor superior al límit superior
    void prova2() {
        int pot = JeanCloud.potPortar(1000,800);
        System.out.println(pot);
    }


    @Test
        //Valor inferior al límit inferior
    void prova3() {
        int pot = JeanCloud.potPortar(200,100);
        System.out.println(pot);
    }


    @Test //Valor no és un número
    void prova4() {
       int pot = JeanCloud.potPortar(Integer.parseInt("hios"),Integer.parseInt("uia"));
        System.out.println(pot);
    }
}

```
## Control Temperatura
### Test

```
import org.junit.jupiter.api.Assertions;
import org.junit.jupiter.api.Test;

public class controlTempTest {
    @Test
        //Valor entre els límits medidor > termostat
    void prova1() {
        int pot = controlTemperatura.modificadorTemperatura(40, 20);
        System.out.println(pot);
    }

    @Test
        //Valor Valor entre els límits medidor < termostat
    void prova2() {
        int pot = controlTemperatura.modificadorTemperatura(20, 40);
        System.out.println(pot);
    }

    @Test
        //Valor superior al límit superior medidor > termostat
    void prova3() {
        int pot = controlTemperatura.modificadorTemperatura(200, 100);
        System.out.println(pot);
    }

    @Test
        //Valor superior al límit superior medidor < termostat
    void prova4() {
        int pot = controlTemperatura.modificadorTemperatura(100, 200);
        System.out.println(pot);
    }

    @Test
        //Valor inferior al límit inferior medidor > termostat
    void prova5() {
        int pot = controlTemperatura.modificadorTemperatura(-10, -20);
        System.out.println(pot);
    }

    @Test
        //Valor inferior al límit inferior medidor < termostat
    void prova6() {
        int pot = controlTemperatura.modificadorTemperatura(-20, -10);
        System.out.println(pot);
    }

    @Test
        //Valor no és un número
    void prova7() {
        int pot = controlTemperatura.modificadorTemperatura(Integer.parseInt("ijd"), Integer.parseInt("hsd"));
        System.out.println(pot);
    }
}

```
