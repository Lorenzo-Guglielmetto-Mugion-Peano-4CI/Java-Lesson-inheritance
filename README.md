# Java-Lesson-inheritance
Ereditarieta' in Java

Il codice [MyCar.java](https://github.com/Prof-Matteo-Palitto-Peano/Java-Lesson-inheritance/blob/master/MyCar.java) vuole illustrare i concetti legati all'ereitarieta' in Java.

## Architettura del Codice
* La SUPER-CLASSE **Veicolo**
* La SOTTO-CLASSE **Auto** che eredita dalla classe **Veicolo** tutte le sue variabili e tutte i suoi metodi
* Nel **main** viene instanziato l'oggetto **myFastCar** di tipo **Auto**

## Concetti evidenziati
* Tutte le variabili e tutti i metodi della SUPER-CLASSE vengono ereditati dall SOTTO-CLASSE
* Le varibili PRIVATE della super classe NON sono accessibili direttamente dall SOTTO-CLASSE
* Le variabili non PRIVATE della SUPER-CLASSE sono accessibili alla SOTTO-CLASSE **solo** se appartengono allo stesso PACKAGE
* Le variabili PROTECTED sono accessibili direttamente dalle sotto-classi **anche** se SUPER classe appartiene ad un package differente.


# ESERCIZIO "CONTO BANCARIO"
SuperClasse **ContoBancario**
* Si vuole realizzare un classe **ContoBancario** che permetta di modellare un generico conto bancario.
* La suddetta classe deve:
  - Contenere un valore (**String**), per rappresentare il numero (alfanumerico) del conto.
  - Contenere un valore (**int**), per rappresentare il bilancio del conto corrente.
  - contenere un costruttore con un parametro che rappresenta il  numero del conto corrente. Il bilancio deve essere inizializzato con il valore 0.
  - contenere un costruttore con 2 parametri, che rappresentano rispettivamente il numero del conto corrente e il bilancio del conto.
  - permettere di conoscere il **numero** e il **bilancio** del conto corrente.
  - permettere di depositare e prelevare somme di denaro dal conto corrente --> Il prelievo puo' avvenire solo se il conto corrente presenta un bilancio sufficiente.
  
## SOTTO-CLASSE ContoEsteso

* Si vuole realizzare una classe **ContoEsteso** che permetta di modellare un conto bancario con un fido.
* La suddetta classe deve:
  - Estendere la classe **ContoBancario**
  - Contenere un valore (**init**) per rappresentare il valore del **fido**.
  - contenere un costruttore con un parametro che rappresenta il numero del conto corrente. Il **fido** viene inizializzato con il valore 1000.
  - Contienere un 2ndo contruttore con 2 parametri che rapprasentano rispettivamente il numero del conto corrente e il cilancio del conto. Il **fido** viene inizializzato con il valore 1000.
  - contenere un 3zo costruttore con 3 parametri che rappresentano rispettivamente il numero del conto corrente, il bilancio e il fido del conto.
  - permettere di conoscere il valore del **fido** 
  - permettere di creare un nuovo **fido**
  - ridefinire il metodo **preleva** della **super-classe** --> è possibile prelevare una determinata somma di denaro da un conto con **fido** solo se questo presenta un bilancio (incluso il **fido**) sufficiente .
  
## DESCRIZIONE DELLA PARTE TEORICA:

## EREDITARIETA':
* Che cos'è: la possibilità di creare una cosiddetta sottoclasse (o classe derivata) che erediti gli attributi e i metodi di una superclasse (o classe madre);
* A cosa serve: si utilizza per creare sottoclassi che possono includere nuovi metodi e attributi oltre a quelli già inseriti nella superclasse;
* Come è stato utilizzato: in questo specifico progetto abbiamo creato la classe "ContoEsteso" facendole ereditare i metodi e gli attributi della classe "ContoBancario".

## POLIMORFISMO:
* Che cos'è: Il meccanismo secondo cui, in una sottoclasse, si possono sovrascrivere e modificare con il comando "@Overload" i metodi ereditati dalla superclasse, ridefinendoli con set di parametri diversi ;
* A cosa serve: il polimorfismo si utilizza quando si vogliono ridefinire metodi già dichiarati nella superclasse da cui si ereditano, modificandone quindi il funzionamento;
* Come è stato utilizzato: In questo progetto è stato ridefinito, nella classe derivata ContoEsteso, il metodo "preleva", già presente nella classe ContoBancario;

## THIS:
* La parola chiave "this" è utilizzata, in Java, per specificare l'oggetto corrente, preso in considerazione durante il tempo di esecuzione (RunTime). Questo comando è seguito da un punto (.), che permette di inserire, in seguito, l'attributi o il metodo riguardante l'oggetto corrente.
