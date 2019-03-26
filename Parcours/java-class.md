# Java
## Classes & Objects
Java est un language de programation orieter objet.  
Tout dans Java est une association de classes et d'objets avec des attributs et des methodes.  
Dans la vie réel, une voiture est un objet, sa taille et sa couleur sont ses attrbituts, et rouler tourner sont ses méthodes

#### Créer une classe
```
public class MyClass {
  int x = 5;
}
```
#### Créer un object
Le ```new``` permet de créer un nouvelle objet.
```
public class MyClass {
  int x = 5;

  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    System.out.println(myObj.x);
  }
}
```
Ca fonctionne aussi avec plussieurs objet faut juste un nom différent pour chaque nouvelle objet.
```
MyClass myObj1 = new MyClass();  // Object 1
MyClass myObj2 = new MyClass();  // Object 2
System.out.println(myObj1.x);
System.out.println(myObj2.x);
```
#### Avoir plussieur classe

MyClass.java
```
public class MyClass {
  int x = 5;
}
```
OtherClass.java
```
class OtherClass {
  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    System.out.println(myObj.x);
  }
}
```

NEXT https://www.w3schools.com/java/java_classes.asp