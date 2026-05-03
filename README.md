# X-balls-puzzle
The 12-Ball Problem: Logic Puzzle Solved for Any Number of Balls

Spiel erläutert für 12 Kugeln (Beispiel, andere Ablaufe auch möglich)

Begin immer 1. Wägung: 4 zu 4 Kugeln

## Szenario A) 4 zu 4 - Eine der Waagschalen bei der initialen 4 zu 4 Wägung ist schwerer

Damit sind 4 "potentiell schwerere", 4 "potentiell leichtere" und 4 "echte" identifiziert. 

Nächste Wägung:
1. Waagschale: 1 "potentiell leichtere", 2 "potentiell schwerere" ,
2. Waagschale: 1 "potentiell schwerere" und 2 "echte".

### A1) Ergebnis: 1. Waagschale schwerer:
Entweder ist eine von den 2 "potentiell schwereren" die Falsche und die ist schwerer, 
oder die "potentiell leichtere" ist die Falsche und ist leichter. 

Die weitere Wägung der beiden potentiell schwereren identifiziert diese eindeutig oder, wenn gleich, ist die andere die leichtere.

### A2) Ergebnis: Waagschalen im Gleichgewicht
Alle bisher geprüften Kugeln sind "echt" es bleibt noch eine, die ist die Falsche, eine Wägung mit einer "echten" zeigt, ob sie schwerer oder leichter ist.

### A3) Ergebnis: 2. Waagschale schwerer:
Entweder ist die "potentiell schwerere" in der 2 Waagschale die Falsche und schwerer,
oder die "potentiell leichtere" in der 1 Waagschale ist die Falsche und leichter.
Eine weiter Wägung einer der dieser Beiden mit einer "echten" zeigt das Ergebnis.

## Szenatrio B) 4 zu 4 - Gleichgewicht in der ersten Wägung

Damit sind 8 "echte" identifiziert.

Dann 2. Wägung mit: In der 1. Waagschale 1 der "echten", 2 der ungeprüften, andere Waagschale 2 der "echten", 1 ungeprüfte.

### B1) 2. Wägung Ergebnis: 1. Waagschale schwerer. 

Das heißt: Entweder eine der 2 ungeprüften in der schwereren  Waagschale ist schwerer oder die andere ungeprüfte in der anderen Waagschale ist leichter. Eine weitere Wägung mit je einer der 2 ungeprüften aus der schwereren Waagschale der 2. Wägung, nun in je einer Waagschale, zeigt as Ergebnis. Ist eine schwerer, dann ist die Kugel darin die falsche und sie ist schwerer, wenn die Waagschalen gleich stehen, ist die andere, die bei der 2. Wägung in der leichteren Waagschale war die Falsche und sie ist leichter.

### B2) 2. Wägung Gleichgewicht

Die 4. ungeprüfte ist also die Falsche! In einer weiteren Wägung mit einer "echten" kann ermittelt werden, ob diese schwerer oder leichter ist.

### B3) 2 Wägung Ergebnis: 2. Waagschale schwerer!

Symmetrischer Fall Wie A1, nur mit umgedrehten Vorzeichen:

Entweder eine der 2 ungeprüften in der leicheren  Waagschale ist leichter oder die andere ungeprüfte in der schweren Waagschale ist schwerer. Eine weitere Wägung mit je einer der 2 ungeprüften in der leichteren Waagschale, nun in je einer Waagschale. Ist eine leichter, dann ist die Kugel daran die Falsche und sie ist leichter, wenn die Waagschalen gleich stehen, ist die andere, die bei der 2. Wägung in der schwereren Waagschale war die Falsche und sie ist schwerer.

## Hypthesenansatz

Zur allgemeinen Lösung kommt man um ein Boolsches Konstrukt nicht herum, für jede Kugel gibt es 2 Hypothesen "leicht" und "schwer". Mit jeder Wägung kann man bestimmte Hypothesen ausschliessen. Theoretisch kann man alle möglichen Wägungen mit allen möglichen Ergebnissen analysieren und schauen, für welche Wägung man wieviele Hypthesen bei welchen Ergebnis (links, gleich, rechts) ausschliessen kann. Für jede mögliche Wägung ergeben sich, je nach Ergebnis, potentiell 3 Werte an Auschlüssen. Die Wägungen werden durch das Minimun dieser 3 Werte gewichtet. Die Wägung mit dem höchsten Gewicht wird gemacht, das Ergebnis eingesammelt und dann gibt es eine neue Grundmenge von Hypthesen, das Ganze geht von vorn los.
