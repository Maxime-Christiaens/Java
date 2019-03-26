# Lance toi
## Créer ton premier .java
1) Lance ton terminal
```
cd desktop/ // ou ton emplacement_favoris
mkdir java // crée un dossier java
cd java 
touch MyFirst.java // crée un fichier .java
code . // ouvre le dans ton IDE
```
2) Entre tes première ligne de code en Java
```
public class MyFirst {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```
3) Sauvegarde ton MyFirst.java
```
javac MyFirst.java // compile en fichier MyFirst.class
jaca MyFirst.java // Hello World
```
**Va voir dans ton dossier** 
Tu peu voir qu'il à crée tout seul un fichier .class qui porte le même nom que votre class global.

## Tour d'horizon rapide

### Syntax
Très similaire au autre language du genre, ici attention car :
- Java est sensible à la case
- Une class commence toujours par un "upperCase"
- Ton code doit toujours être dans une class et tes instruction se finise toujours pas un ";"
```
public class MyClass {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```
Décorticon un peu ce code

``` 
public static void main(String[] args)
```
La méthode ```main()``` est toujours obligatoire dans votre .java  
```System.out.println()``` permet d'afficher du texte à l'écran.

### Les Commentaires
Sur plusieurs lignes ```/* */```
```
/* The code below will print the words Hello World
to the screen, and it is amazing */
System.out.println("Hello World"); // end of method
```
Sur une ligne  
```System.out.println("Hello World"); // This is a comment```
### Les types de datas
En Java il faut toujours spécifier le Type de data de votre variable
```
int myNum = 5;               // Integer (whole number)
float myFloatNum = 5.99f;    // Floating point number
char myLetter = 'D';         // Character
boolean myBool = true;       // Boolean
String myText = "Hello";     // String
```

| Type          | Usage        |
|---------------|--------------|
| ```String ``` | Pour du text |
| ``ìnt`` | Pour les nombres entiers |
| ```float``` | Pour les nombres à virgules |
| ```char``` | Pour les caractères uniques |
| ```boolean``` | true ou false |

### Les Variables


#### Créer des variables
Pour créer une variable rien de plus simple 
```type variable = value;```

```
String firstName = "John ";
String lastName = "Doe";
String fullName = firstName + lastName;
System.out.println(fullName); // John Doe
```
**Ne pas oublier de spécifier le type*
### Les Conditions
#### if else    
Vous pouvez avoir un seul **If**, comme vous pouvez avoir **if** suivi d'un **else**.  
Et encore avoir des **elseif** entre votre **if** et **else**.  
```
int time = 20; // déclarer sa variable
if (time < 18) { // Si time plus petit que 18
  System.out.println("Good day.");
} else { // Sinon
  System.out.println("Good evening.");
}
// Outputs "Good evening."
```
#### Switch
Un rappel sur les bases
| Type          | Usage        |
|---------------|--------------|
| ```case``` | Case à comparer avec l'args passer dans le switch |
| ```break ``` | Stop le switch |
| ``default`` | Code executer par defaut |

```
int day = 4;
switch (day) {
  case 6:
    System.out.println("Today is Saturday");
    break;
  case 7:
    System.out.println("Today is Sunday");
    break;
  default:
    System.out.println("Looking forward to the Weekend");
}
// Outputs "Looking forward to the Weekend"
```
#### Les boucles
#### While
Boucle qui s'éxécute temp que la condition est true.

```
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
```
Existe aussi mais peu utilisé le **do while**
```
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
```
#### For
Boucle qui parcours le tableau pour autand d'objet qu'il contient
```
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```
#### Break/Continue
##### Break
Le ```break``` permet de sortir de la boucle, autend dire de la stopper.
```
for (int i = 0; i < 10; i++) {
  if (i == 4) {
    break;
  }
  System.out.println(i);
} 
```
##### Continue
Le ```continue``` permet de passer à l'itération suivante
```
for (int i = 0; i < 10; i++) {
  if (i == 4) {
    continue;
  }
  System.out.println(i);
} 
}
```
#### Arrays
Comment faire un tableau en Java  

```type[] variable = {"elem1", "elem2", "elem3"}```
```
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]); // Volvo
```
#### Exceptions
Permet de retourner une erreur en cas d'erreur dans le bout de code.
| Type          | Usage        |
|---------------|--------------|
| ```try``` | Le code est tester |
| ```catch ``` | Exécuter si aucune erreur durant le ```try``` |
|```finally```| Exécuter après le ```try & catch```|
**Attention le ```try``` et le ```catch``` sont de pair l'un ne s'utilise pas sans l'autre.*
```
public class MyClass {
  public static void main(String[] args) {
    try {
      int[] myNumbers = {1, 2, 3};
      System.out.println(myNumbers[10]);
    } catch (Exception e) {
      System.out.println("Something went wrong.");
    } finally {
      System.out.println("The 'try catch' is finished.");
    }
  }
}
```

#### Methods
##### Créer une méthode
Une méthode est un block de code qui se run que quand il est appeler.
On peut lui passer des *données* et des *paramètres*.
```
public class MyClass {
  static void myMethod() {
    // code to be executed
  }
}
```
Code explain : 
```myMethod()``` est le nom de la méthode.  
```static``` le paramètre d'accès à la méthode.  
```void``` spécifie qu'on utilise pas de return dans notre méthode.
##### Appeler une méthode
```
public class MyClass {
  static void myMethod() { // On créer la méthode
    System.out.println("I just got executed!");
  }

  public static void main(String[] args) { // On appelle la méthode
    myMethod(); // I just got executed!
  } 
}
```
##### Ajouter des paramètres à une méthode
```méthode(paramètre)```
```
public class MyClass {
  static void myMethod(String fname) { // Définir le type(String) et le nom de l'args(fname)
    System.out.println(fname + " Refsnes");
  }

  public static void main(String[] args) {
    myMethod("Liam"); // Liam Refsnes
    myMethod("Jenny"); // Jenny Refsnes
    myMethod("Anja"); // Anja Refsnes
  }
}

```
*Rappel ```void``` car on utilise pas de ```return```  
Définir le type de donnée passer en paramètres ex: ```String```*


