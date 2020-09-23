## EA 2
Szeretnénk rendelkezésre állást biztosítani akkor is ha bizonyos részeszközök meghibásodnak. Hogyan eldönthető hogy melyik lesz a hibás?

Csak kettős párhuzamosítás esetén nehezen eldönthető, hogy melyiknek lesz igaza, hogy melyik jó, és melyik hibás. Hármas redundancia eetén van egy választó, szavazó áramkör ami megnézi, hogy a két kimeneti érték megegyezik és a harmadikkal is stimmel. A hármas redundancia esetén kettő már nem redundanciát képvisel ebből. => Négyes redundacia esetén jobb értéket kapunk, de többelt energiafogyasztás ([`Termonukleáris generátor`](https://hu.wikipedia.org/wiki/Termoelektromos_gener%C3%A1tor)) és többlet tömeg és hely.
**Mi van ha a választó áramkör hibásodik meg?** Nagyon egyszerű áramkör, tehát elvileg nem hibásodik meg, elvileg, legalábbsi kicsi a valószínűsége.

### Hogyan lehet megoldani, hogy ne fogyasszon sokat?
> Tartalék egységeket alkotunk, ami csak akkor kapcsol be ha szükséges. => a választó áramkörből visszajelzést küldünk az egységekhez => ha egy egység meghibásodik akkor azt letiltja, és a maradék, tartalék negyediket bekapcsoljuk. Ezzel még mindig nem oldottuk meg a hely és tömeg kérdését sem, valamint a választó áramkör egyre bonyolultabb és egyre nagyobb a meghibásodás esélye.

### Öndiagnosztizáló rendszer
> Két egységet egyként kezelünk, majd az abból alkult új egységeket párosítjuk és egy összehasonlító egységre kötjük, ebből egymás mellé teszünk hármat és azt kötjük be a választó áramkörbe. 
> Ugyanakkor ha beadjuk a pontosságát a rendszerbe, akkor már ki tudjuk válassztani, hogy melyik egységet szeretnénk használni.
