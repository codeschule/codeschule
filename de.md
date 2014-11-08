
#Code Schule

## Zeichnen mit Roy
    clear
    fd 100
    lt 90
    fd 100
    rt 90
    fd 20

## Sequence – Viele Dinge auf einmal zeichen
    s [fd 100, lt 90]

## Repeat – Die gleiche Sache mehrmals wiederholen
    r 4 (s [fd 100, lt 90])

## Funktionen – Jetzt muss der Computer etwas lernen
    let step = s [fd 100, lt 90]
    let square = r 4 step
    square

## Parameter in Funktionen – Das gleiche tun, aber mit verschiedenen Werten
    let circle radius = repeat 45 (s [fd radius, lt 8])
    circle 2
    circle 4

## Rekursion – Funktionen, die sich selbst aufrufen
    let spiral x = if x == 0 then fd 0 else s [fd x/10, rt 10, spiral (x - 1)]
    spiral 100

## Noch mehr Beispiele

## Das Haus vom Nikolaus zeichnen
    lt 90
    fd 100
    rt 90
    fd 100
    rt 45
    fd 71
    rt 90
    fd 71
    rt 135
    fd 100
    lt 135
    fd 142
    lt 135
    fd 100
    lt 135
    fd 142

## ...und das Ganze noch mal als Funktion
    let haus = s [lt 90, fd 100, rt 90, fd 100, rt 45, fd 71, rt 90, fd 71, rt 135, fd 100, lt 135, fd 142, lt 135, fd 100, lt 135, fd 142]
## Eine Blume zeichnen
    let spirale x = if x == 0 then fd 0 else s [fd x/10, rt 10, spirale (x - 1)]
    let blume = r 6 (spirale 102)
    blume

## Noch mehr?

http://eraseallkittens.com/

http://scratch.mit.edu/