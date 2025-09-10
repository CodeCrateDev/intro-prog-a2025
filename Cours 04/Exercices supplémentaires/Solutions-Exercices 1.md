# Exercices Java : Conditions IF/ELSE

Voici trois exercices progressifs (facile → moyen → difficile) utilisant les conditions en Java.  
Chaque exercice est suivi de sa solution complète.

---

## 🔹 Exercice 1 : Facile  
**But** : Vérifier si un nombre est pair ou impair.  

**Énoncé** :  
Écris un programme qui demande à l’utilisateur d’entrer un nombre entier.  
- Si le nombre est pair, affiche : *"Le nombre est pair"*.  
- Sinon, affiche : *"Le nombre est impair"*.  

### ✅ Solution
```java
import java.util.Scanner;

public class Exo1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Entrez un nombre entier : ");
        int nombre = sc.nextInt();

        if (nombre % 2 == 0) {
            System.out.println("Le nombre est pair");
        } else {
            System.out.println("Le nombre est impair");
        }

        sc.close();
    }
}
```

---

## 🔹 Exercice 2 : Moyen  
**But** : Vérifier la catégorie d’âge.  

**Énoncé** :  
Écris un programme qui demande à l’utilisateur d’entrer son âge.  
Le programme doit afficher :  
- *"Enfant"* si l’âge est entre 0 et 12 ans,  
- *"Adolescent"* si l’âge est entre 13 et 17 ans,  
- *"Adulte"* si l’âge est entre 18 et 64 ans,  
- *"Sénior"* si l’âge est 65 ou plus.  

### ✅ Solution
```java
import java.util.Scanner;

public class Exo2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Entrez votre âge : ");
        int age = sc.nextInt();

        if (age >= 0 && age <= 12) {
            System.out.println("Enfant");
        } else if (age >= 13 && age <= 17) {
            System.out.println("Adolescent");
        } else if (age >= 18 && age <= 64) {
            System.out.println("Adulte");
        } else if (age >= 65) {
            System.out.println("Sénior");
        } else {
            System.out.println("Âge invalide");
        }

        sc.close();
    }
}
```

---

## 🔹 Exercice 3 : Difficile  
**But** : Trouver le plus grand de trois nombres.  

**Énoncé** :  
Écris un programme qui demande trois nombres à l’utilisateur.  
Le programme doit afficher :  
- *"Le plus grand nombre est : X"*, où X est le plus grand des trois.  
⚠️ Attention : il faut gérer le cas où deux ou trois nombres sont égaux.  

### ✅ Solution
```java
import java.util.Scanner;

public class Exo3 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Entrez le premier nombre : ");
        int a = sc.nextInt();
        System.out.print("Entrez le deuxième nombre : ");
        int b = sc.nextInt();
        System.out.print("Entrez le troisième nombre : ");
        int c = sc.nextInt();

        if (a >= b && a >= c) {
            System.out.println("Le plus grand nombre est : " + a);
        } else if (b >= a && b >= c) {
            System.out.println("Le plus grand nombre est : " + b);
        } else {
            System.out.println("Le plus grand nombre est : " + c);
        }

        sc.close();
    }
}
```
