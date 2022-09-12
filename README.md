# kodetorsdag

Husk å kompilere koden før du kjører den:

```bash
javac Game.java
java Game
```
## 8. september / 15. september

```java
public class Player {
    public String name;
}
```

### Oppgave

Forsøk å kompilere og kjøre Player.java. Hvilken feilmelding får du?

Denne feilmeldingen får du fordi Player.java ikke har en main-funksjon. Men det har Game.java. 

```java
public class Game {

    public static void main(String[] args){

    }

}

```

La oss opprette et objekt av Player-klassen. Husk å kjøre i main-metoden i Game.java

```java
Player one = new Player();
```

Alle objekter av Player har de egenskapene som er beskrevet i klassen. Gi Player one et navn:

```java
one.name = "morpheus";
System.out.println(one.name + " just entered the game!");
```

Hva tror du skrives til terminal? Kompiler og test at koden kjører. 

Alle klasser har en funksjon som kjører når det opprettes et objekt, dette kaller vi for en konstruktør. Akkurat nå ser konstruktøren i klassen Player slik ut: 

```java
public Player(){
}
```

Vi kan skrive over konstruktøren slik at vi definerer noen oppstartsoperasjoner. I dette tilfellet vil vi at variabelen name skal få en verdi

### Oppgave
Skriv en konstruktør i klassen Player.java, slik at følgende kode kjøres fra Game.java. Kompiler og test at koden kjører. 

```java
Player one = new Player("morpheus");
```

### Oppgave
Nå når du vet hvordan du oppretter objekter fra Player.java, kan du lage et våpen til Player one? Kompiler og test at koden kjører. 

```java
public class Weapon {
    private int damage;
    private String type;
}
```

Gi variablene damage og type verdi fra Game.java

```java
Weapon stick = new Weapon();
stick.damage = 1;
stick.type = "wooden stick";
```

Kompiler og kjør koden. Hvilken feilmelding får du? Dette er fordi variablene er private og ikke kan nås utenfor klassen. 

### Oppgave
Lag en konstruktør til Weapon.java slik at følgende kode kjøres fra main-funksjonen i Game.java

```java
Weapon stick = new Weapon(1, "wooden stick");
```

### Oppgave
Lag beskrivende kommentarer på koden din. Om du får det til, lag et GitHub-repo som heter kodetorsdag og push koden dit. 