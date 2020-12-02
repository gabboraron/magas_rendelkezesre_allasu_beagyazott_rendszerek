## EA 3
Szeretnénk rendelkezésre állást biztosítani akkor is ha bizonyos részeszközök meghibásodnak. Hogyan eldönthető hogy melyik lesz a hibás?

Csak kettős párhuzamosítás esetén nehezen eldönthető, hogy melyiknek lesz igaza, hogy melyik jó, és melyik hibás. Hármas redundancia eetén van egy választó, szavazó áramkör ami megnézi, hogy a két kimeneti érték megegyezik és a harmadikkal is stimmel. A hármas redundancia esetén kettő már nem redundanciát képvisel ebből. => Négyes redundacia esetén jobb értéket kapunk, de többelt energiafogyasztás ([`Termonukleáris generátor`](https://hu.wikipedia.org/wiki/Termoelektromos_gener%C3%A1tor)) és többlet tömeg és hely.
**Mi van ha a választó áramkör hibásodik meg?** Nagyon egyszerű áramkör, tehát elvileg nem hibásodik meg, elvileg, legalábbsi kicsi a valószínűsége.

### Hogyan lehet megoldani, hogy ne fogyasszon sokat?
> Tartalék egységeket alkotunk, ami csak akkor kapcsol be ha szükséges. => a választó áramkörből visszajelzést küldünk az egységekhez => ha egy egység meghibásodik akkor azt letiltja, és a maradék, tartalék negyediket bekapcsoljuk. Ezzel még mindig nem oldottuk meg a hely és tömeg kérdését sem, valamint a választó áramkör egyre bonyolultabb és egyre nagyobb a meghibásodás esélye.

### Öndiagnosztizáló rendszer
> Két egységet egyként kezelünk, majd az abból alkult új egységeket párosítjuk és egy összehasonlító egységre kötjük, ebből egymás mellé teszünk hármat és azt kötjük be a választó áramkörbe. 
> Ugyanakkor ha beadjuk a pontosságát a rendszerbe, akkor már ki tudjuk válassztani, hogy melyik egységet szeretnénk használni.

## EA 4
> *watch dog* rendszer az mikor felügyeljük, hogy megfelelően működik-e az alkalmazott rendszer, ha például egy számlálót használunk amit minden ciklusban növelünk és időnként nullázzuk, ha nem nulláztuk túlcsordul, ha túlcsordult akkor hiba van, és reset kell.
**Hibrid redundáns rendszerek** 
Két vevőt alkalmazva szelektorral választunk köztük, de az egészet ki is hagyhatjuk, ha ügyesen tervezzük meg a rendszert.

# EA5
**Hibrid redundáns rendszerek vezérlő választása**
- lehet nem programozható hardware
- lehet egy programozható processzor, pl [FPGA](https://github.com/gabboraron/ujrakonfiguralhato_digitalis_aramkorok) vagy a kimeneteket konfigurálható áramkör.
Nem eldönthető, hogy melyik jobb vagyg rosszabb.

**Univerzális HW rendszerek**
CPU - CHIPSET - FPGA

https://es.scribd.com/doc/110301633/Asic-Smith

- az intel xeon is támogat FPGA kommunikációt: https://www.intel.com/content/www/us/en/programmable/solutions/acceleration-hub/overview.html
- ezzel csökkenthetőek a hibák
- két féle FPGA gyártás módszer:
  - a kapcsolat ott van, ha nem kell megszüntetjük -> nem érzékeny sugárzásra, viszont csak egyszer lehet átprogramozni, mert azokat a kapcsolatokat ami nem kell kiégeti véglegesen
  - a kapcsolat nincs ott de ha kell összekötjük  -> pl űrszonda esetében, vagy bármilyen más sugárzó környezet mellett nem használható
- analóg rendszereeknél [analóg programozható áramkörökkel - FPAA](https://en.wikipedia.org/wiki/Field-programmable_analog_array)val valósíthaó meg

**Hátrányt jelenthet a rednundancia**
- 2 magasan elhelyezett hajtóműves gépnél, ha leáll az egyik akkor egy irányba kezdhet forogni a gép
- 4 kis teljesítményű hajtómű a tömgeközéppont közelében 
- 2 nagy teljesítményű hajtóműnél 

# EA 6

https://www.tinkercad.com/ használata

# EA 7
https://github.com/gabboraron/magas_rendelkezesre_allasu_beagyazott_rendszerek/blob/master/redundacia.brd

## ZH kidolgozások
A **többségi elven működő redundáns egységek** egy időben működnek, de kimenőjeleik a szavazóegységbe kerülnek. A szavazóegység a bemenetére érkező információt kiértékelve a többségi elv alapján képezi a kimenőinformációt. E megoldás esetén a szavazóegység azt az információt adja ki a kimenetén, amely legalább két modulnál megegyezik a 8.1b ábra szerinti módon.
![8.1b ábra](https://regi.tankonyvtar.hu/hu/tartalom/tamop425/2011_0001_531_programirany/images/fgr_8_1.png)

