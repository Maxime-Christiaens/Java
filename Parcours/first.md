# Lance toi
## Créer ton premier .java
Lance ton terminal
```
cd desktop/ // ou ton emplacement_favoris
mkdir java // crée un dossier java
cd java 
touch MyFirst.java // crée un fichier .java
code . // ouvre le dans ton IDE
```
Entre tes première ligne de code en Java
```
public class MyFirst {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```
Maintenant **Run** & va voir dans ton dossier 

Tu peu voir qu'il à crée tout seul un fichier .class qui porte le même nom que votre class global et qui est illisible dans votre IDE. et c'est celui la qui te renvoi Hello World.

## Tour d'horizon rapide

### Syntax
```
public class MyClass {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```
Très similaire au autre language du genre, ici attention car :
- Java est sensible à la case
- Une class commence toujours pas un ?? ( upperCase )
- Ton code doit toujours être dans une class
- et tes instruction se finise toujours pas un ;

``` 
public static void main(String[] args)
```
Ici la méthode ```main()``` toujours obligatoire dans votre .java  
La méthode ```System.out.println()``` permet d'afficher du texte à l'écran.

### Commentaires
Sur plusieurs lignes ```/* */```
```
/* The code below will print the words Hello World
to the screen, and it is amazing */
System.out.println("Hello World"); // end of method
```
Sur une ligne ```System.out.println("Hello World"); // This is a comment```

### Variables
#### Types de variable
- ```String ``` Pour du text
- ``ìnt`` Pour les nombres entiers
- ```float``` Pour les nombres à virgules
- ```char``` Pour les caractères uniques
- ```boolean``` true ou false

#### Créer des variables
```
String firstName = "John ";
String lastName = "Doe";
String fullName = firstName + lastName;
System.out.println(fullName);
```
### Condition
#### If else 
```
int time = 20;
if (time < 18) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening."
```
#### Switch
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
#### While
```
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
```
#### For
```
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```
#### Break/Continue
```
int i = 0;
while (i < 10) {
  System.out.println(i);
  i++;
  if (i == 4) {
    break;
  }
} 
```
```
int i = 0;
while (i < 10) {
  if (i == 4) {
    i++;
    continue;
  }
  System.out.println(i);
  i++;
} 
```
#### Arrays
```
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]);
// Outputs Volvo
```
#### Exceptions
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
```
public class MyClass {
  static void myMethod(String fname) {
    System.out.println(fname + " Refsnes");
  }

  public static void main(String[] args) {
    myMethod("Liam");
    myMethod("Jenny");
    myMethod("Anja");
  }
}
// Liam Refsnes
// Jenny Refsnes
// Anja Refsnes
```

NEXT https://www.w3schools.com/java/java_classes.asp