# Transition, transform & animation

## Transition - intro

Transition betyder att vi anger vad som ska hända när vi går från ett läge till ett annat. T.ex. när vi använder en hover:

```css
a{
    color: #fff;
}

a:hover{
    color: #000;
}

```

När vi hovrar i vanliga fall sker övergång snabbt och ryckigt. Vi kan dock släta ut övergången mellan färgerna med en `transition`:

```css
a{
    color: #fff;
    transition: all 1s ease; /* Duration: 1s with ease */
    /* transition: <property> <duration> <easing> */
}
a:hover{
    color: #000;
}
```

Detta kommer att ge en mycket långsammare övergång samt att övergången kommer att gå långsamt i början och sedan öka med `ease`-värdet. Här säger vi att vi ska göra en `transition` på samtliga egenskaper som ändras. I detta fall skulle vi enbart kunna välja egenskapen `color` men det kan vara lättare till en början att använda `all`.


## Transform - intro

Med egenskapen `transform` säger vi att något ska omvandlas från sin tidigare position eller hur elementet ursprungligen var.

```css

.box{
    width: 100px;
    height: 100px;
    background-color: red;
}
.box:hover{
    transform: translate(10px, 10px); /* translate(x,y);*/
}
```

Här ovan säger vi att när vi hovrar över elementet ska elementet flyttas `translate`: 10px, 10px. Alltså 10px längs x-axeln (till höger) samt 10px längs y axeln (nedåt).

Vi kan även använda en rad andra värden så som t.ex: `rotate` samt `scale`. Med `rotate` behöver vi dock ange hur mycket ett element ska rotera i form av grader: `deg`.

```css
.box{
    transform: rotate(30deg);
}

```

Här säger vi att elementet ska rotera 30 grader åt höger, men vi kan även använda minus-värden: `transform: rotate(-30deg)` för att rotera åt andra hållet. Minusvärden kan även användas för t.ex. `translate()`.

`scale` däremot tar ett värde från 0 och uppåt:

```css
.box{
    transform: scale(2);
}
```

Här säger vi att elementet ska skala till dubbla storleken.

Det finns en rad olika egenskaper men dessa är de mest användbara. Läs igenom första länken bland länkarna nedan för att få en bättre förståelse av `transition` och `transform`.

## Information om repot

I detta repo finns ett exempel på hur man kan lösa mobil navigation med hjälp av `transform` och `transition`. 

Oftast löser man mobila navigation med en hamburgarikon och genom att gömma navigationen utanför skärmen som jag gjort i detta exempel. Det finns dock väldigt många sätt och välj ett som passar just din grupps navigation. Fler exempel finns t.ex. på [http://bradfrost.github.io/this-is-responsive/patterns.html](http://bradfrost.github.io/this-is-responsive/patterns.html).

Läs länkarna nedan (speciellt första länken) för att försöka få en förståelse över hur `transition` samt `transform` fungerar. De viktigaste `transform`-egenskaperna är `translate`, `scale` samt `rotate`.

Använd koden i detta repo för att utforska `transitions` samt `transforms` genom att t.ex. ändra längden på olika `transitions` samt vilka `easing` de ska ha. Kom ihåg att man även kan animera `svg`-element. 

#### Inspektera transitions i webbläsaren

Man kan lätt ändra på `transitions` i t.ex. Chrome för att testa sig fram och se hur olika `easings` fungerar genom att trycka på den lila ikonen vid `transition`:

![Imgur](http://i.imgur.com/7vpvHSi.png)

Då borde man få upp en liten ruta där man kan testa sig fram hur de olika animationerna rör sig.

![Imgur](http://i.imgur.com/CJBZoCj.png)


## Länkar att läsa

* [http://css3.bradshawenterprises.com/](http://css3.bradshawenterprises.com/)
    - Interaktiv tutorial till allt som har med animering i CSS att göra.

* [https://robots.thoughtbot.com/transitions-and-transforms](https://robots.thoughtbot.com/transitions-and-transforms)
    - Ytterligare tutorial som går igenom alla egenskaper inom transition samt transform med kodexempel.

* [Google Developers - Inspect animation](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations)
    - Hur man inspekterar animationer i webbläsaren för att se hur olika element animeras. Man kan sakta ner animationerna för att se exakt vad som händer. Liknande funktioner ska finnas i alla webbläsare, iaf Firefox.


## Att tänka på

Väldigt många egenskaper kan animeras men de mest lättanimerade för browsern, alltså de animationer som är minst krävande att göra är följande:

* Position: använd `transform: translate()`
* Skala: använd `transform: scale()`
* Rotation: använd `transform: rotate()`
* Genomskinlighet: `opacity: 1`

Om man vill läsa mer om vad som är bäst att animera:

* [High Performance Animations](https://www.html5rocks.com/en/tutorials/speed/high-performance-animations/)
* [How to achieve 60 fps animations with CSS3](https://medium.com/outsystems-experts/how-to-achieve-60-fps-animations-with-css3-db7b98610108#.pa9a7ur3p)



