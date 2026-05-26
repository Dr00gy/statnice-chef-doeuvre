# Předmluva
V tomto docu se jedná o přípravu na státnice ve formě sekvenčních deep-dives do individuálních pojmů a jejich linkování s několika disciplínami z okruhů. Jde o způsob, jak si efektivněji vytvořit souvislosti a obecně zlepšit memory. Cílem je si nejen zapamatovat "perly", ale také nějakým způsobem porozumět dané látce. Focus na relace zejména, jelikož je to pro náš ročník 2026 jakýmsi hyperfixačním bodem v komisích... AI je použito jen pro ušetření práce s formátováním tabulek / toku myšlenek z matematických definic nebo pro psaní příkladů k vysvětlivkám, ale kontroluju ho. Zbytek je all human cognitive work. Ofc využívám prezentací od našich profesorů, jakékoliv slidy nejsou moje tvorba. Text je psán v čengliš, v malých částech bez diakritiky, abych nějak rychle spleskal dohromady vše podstatné, budu editovat později.

# Značení
číslo) Kapitola <br />
písmenko. Podkapitola <br />
písmenko.římské: Podpodkapitola <br />
🔴 Nejasnosti a hnusy (hlavně u otázek)<br />
🔵 Přímo otázky <br />
🟣 Perly <br />

## Matematiky-logická část
**POZOR!!!** Zde najdete i mentions k určitým praktických záležitostem, např. propojení relací s databázema, rekurence k FPR. Samozřejmě pak bude topic databází nebo funkcionálního programa linked pro quick jumps na čtení.

Upe základní chujovinky jako co je přímka nebo realný číselný obor tu vysvětlený nebude, jen tu hodím Bouchalu na začátek xd Nejzákladnější items, kterým se budu věnovat, jsou vektorové prostory, báze, množiny, funkce v kontextu topics LA, DIM, MA (příklady lin. zobrazení, surjekce, derivace) a další... Avšak nic z prezentací zde nemissnu. Focus je na matiku, přičemž na ni v individuálních kapitolách navazuji i na logiku. UTI bude trochu oddělenější, ale s referencema a linkama tam, kde je to relevantní, pokud vubec.

Pokud se setkáte s termínem "horní / dolní" část realného čísla, jedná se o zaokrouhlování. <br />
![image](https://hackmd.io/_uploads/Skb3JDqJzg.png) <br />
![image](https://hackmd.io/_uploads/Bks3Jvcyfl.png) <br />

### 1.1) Axiomy a dokazování / indukce
#### A. Axiomy a dokazování, kousek začátku VL logiky
##### AXIOMY
##### LOGIKA_START
[Aplikace teorie v DB](#####DATABAZE_TEORIE_NORMALOVE_FORMY) <br />
![image](https://hackmd.io/_uploads/BJcaGJ91Mg.png) <br />
**Axiomy, které třeba platí v lineární algebře. IMPORTANT SI JE ZAPAMATOVAT, CO JE CO, zrovna na toto neodkazuju neustále při každém mention.**

K dokazování něčeho potřebujeme věty, tady je pevně spjatá logika a matematika. V matice **P -> D**, kde **P** jsou **přesně formulované předpoklady**, za kterých **platí** nějaké **tvrzení D**. Ekvivalentní terminologie disciplín
* **Tvrzení = argument = výrok**
* **Předpoklady = podmínka = premise**

**Logika** je **věda o správném usuzování**. Je to **nástroj**, který **ověřuje platnost argumentů**. Na **základě předpokladů / premis** můžeme **usoudit**, zda je **závěr pravdivý**. **Závěr je nutně pravdivý, když jsou všechny premisy pravdivé.** **Zabýváme se** **deduktivně platnými úsudky**. Logické vyplývání závěru: P1 ... Pn ⊨ Z

**Závěr** bude **logicky vyplývat**, **pokud v úsudku nikdy nebudou pravdivé všechny předpoklady a zároveň nepravdivý závěr = správná logická forma.** Pro **správnou logickou formu** taktéž **potřebujeme**, aby **všechny nutné předpoklady byly uvedené:** <br />
![image](https://hackmd.io/_uploads/B1CcERKyGe.png) <br />

Podrobný **postup**, jak **z předpokladů odvodit tvrzení** věty nazýváme **důkaz**. V tomto odstavci popisujeme čistě matematický důkaz, kdy: **Krok za krokem** bereme v potaz nějaký **axiom** relevantní k naši **current matematické teorii** (diskrétka, geometrie, ...), v**e které hledáme** daný **důkaz**. **Spolu s axiomem dbeme na předpoklad / podmínku**, **na kterou** se **vymezíme**, pak nás zajímá také **výrok odvozený z předchozích kroků**, **ten je užitý na** některém z **pravidel**. Tvrzení, jejichž důkaz spočívá v dosazení do definice považujeme
za „zřejmá" tvrzení a důkaz se neuvádí.

DIM axiomy odvozené z Peam. axiomů, geometrie z Eukleda. <br />
![image](https://hackmd.io/_uploads/ByxnWycJMg.png) <br />
![image](https://hackmd.io/_uploads/HkMC-19yMe.png) <br />
![image](https://hackmd.io/_uploads/BJB_fJc1zg.png) <br />
![image](https://hackmd.io/_uploads/SJ8uzeqyfl.png) <br />
**Poslední screen poukazuje na strukturu, abychom nedokazovali pro parametr do nekonečna.** <br />
WIP skok na algoritmy <br />

![image](https://hackmd.io/_uploads/H1-7Wg5kfg.png) <br />
**PAMATOVAT SI, nelinkuju toto.** <br />
[Dopředný skok na relace protoze unarni a binarni op.](#####RELACE) <br />

**Dokazování v nejzákladnější logické teorii (výroková) rozumíme takto:** <br />
![image](https://hackmd.io/_uploads/BJbtrCYJfg.png) <br />
**Spojitost mezi log. vyplýváním a platností:**
**Logické vyplývání (pravda, nepravda)** můžeme **dokazovat přes platnost úsudku.** **Úsudek** je **platný**, **pokud** je **formule pravdivá**, ale může být **také platný, pokud závěr a jedna premisa** je **nepravdivá**. **Neplatný úsudek se skládá z nepravdivého závěru, jen tehdy, když jsou všechny premisy pravdivé.**

**VL analyzuje způsoby skládání jednoduchých výroků do výroků složených pomocí logických spojek. Výrok je tvrzení, o němž má smysl prohlásit, zda je pravdivé či nepravdivé. Výrok nemůže být otázka ani rozkaz. Avšak ne všechny oznamovací věty jsou výroky (Francouzský král je holohlavý - nemá smysl se nad tímto zamýšlet, když fracouzský král ani neexistuje).**

**Výroky dělíme na:**
* **Jednoduché - žádná vlastní část jednoduchého výroku již není výrokem.**
* **Složené - výrok má vlastní část(i), která je/jsou výrokem. Obsahuje logické spojky a závorky.**

**Význam jednoduchých výroků redukuje VL na pravdu (1) a nepravdu (0). Výroková logika je tedy algebrou pravdivostních hodnot. Příklady složených výroků:**
* V Praze prší a v Brně je hezky.
* Není pravda, že v Praze prší. (negace)

[Boolean algebra související s pravdivostními hodnotami](#####BOOLEAN) <br />

Zde pokračování ke zbytku teorie týkající se výrokové logiky + důkazové techniky, které jsou mentioned ve screenu below, ale v kontextu logiky. <br />
[SKOK NA ZBYTEK VYROKOVE LOGIKY](#####LOGIKA) <br />

![image](https://hackmd.io/_uploads/H1A1fl9yzg.png) <br />
![image](https://hackmd.io/_uploads/Hy4K9X51Ml.png) <br />
![image](https://hackmd.io/_uploads/Sk25qX9yMl.png) <br />
"Handshaking problem: V mistnosti je n lidi, nekteri si podali ruce. Ukazte, ze alespon dva lide podali ruku stejnemu poctu lidi... priklad problemu." <br />

### 1.2) Množiny
##### MNOZINY
[Aplikace v databázích](#####DB_START) <br />
**Množina** je **soubor rozlišitelných prvků** a je **svými prvky plně určena**; množinu s prvky a, b, c značíme: {a, b, c}.
**Prvkem množiny může být opět množina. Množina také nemusí mít žádné prvky: ∅. NIKOLIV PRAZDNY SYMBOL VE SLOZENYCH ZAVORKACH!!!**

Příklady množin výčtem prvků (taxativně):
**∅ , {a,b}, {b,a},{a,b,a}, {{a,b}}, {a,{b,a}}, { ∅ , { ∅ },{{ ∅ }}}**
Množiny **zadáváme taky** nějakou společnou vlastností, matematickým zápisem / **charakteristickou vlastností: N = {x : x ∈ N, x > 5}**

**Množiny jsou identické, právě tehdy a jen tehdy, když mají stejné prvky (princip extenzionality).** Množiny jako takové se značí velkým písmenem. <br />
[Funkce dopředně](#####FNCE) <br />
![image](https://hackmd.io/_uploads/HyboFCKJfe.png) <br />
**ALTERNATIVA:
A je podmnožinou B, jestliže pro každé a ∈ A je také a ∈ B.**

**Note k potenční množině, v podstatě obsahuje všechny podmnožiny A. Dvojka umocněné A, protože když máme 3 prvky v A, např. a,b,c, tak individuálně a v párech máme 8 výstupů spolu s prázdnou množinou a také a,b,c v tuplu. Jedná se vlastně o systém množin, neboli množina množin, ale takhle tomu prý nemáme říkat, lepší je říct systém. Značí se jako T podmnožina dvojka umocněné A. Operace rozdíl není komutitativní ani asociativní, distributivní jen ve special případech. Distributivnost, asoc. a komutativ. ve sjednocení a průniku. Univerzum obsahuje všechny možné prvky, a pro nějaké A obsahuje i jeho doplněk, tedy to, co není v A, ale je třeba v M, tak jak ze screenu.** <br />
![image](https://hackmd.io/_uploads/ryCKT0YyGg.png) <br />
[ODKAZ NA LOGIKU KVULI POJMU UNIVERZA](#####LOGIKA) <br />

**PAMATUJ CO JE KARTEZSKY SOUCIN!!! bude relevantní v další kapitole, budu linkovat zpátky k němu až později, ale stejně je to pro nás dost kritická záležitost, kterou bychom měli znát.**
#### A. Kartézský součin
##### KARTEZ
[Kartéz. relevance v DB relacích](#####DOTAZ_RELAC) <br />
![image](https://hackmd.io/_uploads/By2TaAt1fg.png) <br />
![image](https://hackmd.io/_uploads/Skac0AYkzg.png) <br />
![image](https://hackmd.io/_uploads/HJcsAAtkfg.png) <br />
#### B. Inkluze a exkluze
##### INKLUZE_EXKLUZE
Inkluze a exkluze se využívá v kombinatorice a pravděpodobnosti, v databázích, aby se nepočítali dvakrát lidi, co umí jak matiku, tak češtinu, když se například řeší, kdo se naučil alespon na jeden predmet na maturitu. **Kongruence je speciální tvar inkluze a exkluze, kde průniky stejně velkých množin se v modulo aritmetice “ruší” (počítají se jen podle parity výskytu prvků, i.e. sudost či lichost).** <br />
[Kongruence mentioned, jump here](#####KONGRUENCE) <br />
[Dopředně na kombinatoriku](#####KOMBI) <br />
[Aplikace v databázi](#####DOTAZ_RELAC) <br />
[Teorie na relacích v databázi](#####DATABAZE_TEORIE_NORMALOVE_FORMY) <br />

### 1.3) Vektory, vektorový prostor, báze, souřadnice, funkce, zobrazení, transformace, relace
##### VEKTORY
#### A. Vektory, vektorový prostor a báze
**(1,n) - řádkový vektor
(m,1) - sloupcový vektor
Počet složek ve vektoru je dimenze. Když máme stejnou dimenzi a velké složky, tak jsou dva vektory rovné.** **Operace sčítání, odečítání a násobení skalárem (basically čti "číslem", zastupuje ho) jsou asoc., komut. i distrib.**
WIP skok na matice násobení <br />
[Rovnou k funkcím](#####FNCE) <br />

Někdy je výhodné nad vektory uvažovat jako o směru, nějaké šipce, ale ne pořád, někdy je lepší se nad ním zamyslet, jako o bodě. Doporučuju nad tím tak přemýšlet, pokud vyloženě nezmíním směr.

**Vektorový prostor: reálný** nebo **komplexní - R, C** prostor, kde **platí již výše zobrazené axiomy lin. algebry** týkající se **sčítání a násobení vektorů skalárem.** Také platí to, že **existuje** něco jako **nulový vektor** nebo **negativní / opačný vektor**. **Odečteme tedy od sebe "v" a "-v", což nám dá nulový vektor.

Lineární obal neboli "span" (pokud koukate na anglicke materialy) encompassuje všechny vektory, které lze poskládat za pomocí sčitání a násobení vektorů.**

**Báze** se značí epsilony a jinými řeckými písmeny, zjednodušeně se **jedná o vektory**, které jsou **na sobě lin. nezávislé**, tudíž **nejde z toho jednoho vektoru nijak poskládat ten druhý přes + nebo násobek**, **nejčastěji 0,1 a 1,0.** **Báze** nám v podstatě **definuje systém souřadnic pro** náš **prostor**. **Počet vektorů báze je tedy roven počtu lin. nezávislých vektorů nějaké dimenze "V".** **Nekonečně-rozměrnému prostoru rozumíme jako prostor bez báze.**
WIP SKOK NA POKROCILE VECI S BAZEMA PO MATICICH VE SPEKTRALU

### !!! INSANELY IMPORTANT PRO 2026 !!!
#### B. Relace
##### RELACE
[Schéma databází, neboli praxe k relacím](#####SCHEMA_DB) <br />
**Relace je základ pro funkce, uspořádání, ekvivalence.** <br />
![image](https://hackmd.io/_uploads/r1vM_ycyfx.png) <br />
![image](https://hackmd.io/_uploads/B1wVdyqkMl.png) <br />
**Pro představu, ternární relace by byla A x B x C. Unární relace by se děla jen na "A", např. "být sudý". Příklad binární relace z DB: "Má stejné pole pro přijmení". Homo nebo hetero je asi jasná z toho, zda máme stejné písmenka a nebo odlišné v zápisu.** Další příklady relací máme v logických symbolech výše. <br />
![image](https://hackmd.io/_uploads/S1RKdy9kzl.png) <br />
**Příklady k definici:** <br />
* "být příbuzný" - reflexivní, sym., tranzitivní
* "dorozumět se" - symetrické
* "být nadřízený" - antisym. a tranzitivní
**Dělitelnost je reflexivní, tranzitivní a antisym. Ekvivalence to samé, ale symetrická.** Reflexivita, antisym., tranzitivita jsou znázorněné v matice symboly rovnosti a menší než. Symetrie symbolem rovnosti. <br />

[Dopředně na kombinatoriku](#####KOMBI) <br />
[Dopředně na kongruence](#####KONGRUENCE) <br />

![image](https://hackmd.io/_uploads/BJbo3JckGe.png) <br />
**i.e. rozdělení na kousky, co se nepřekrývají, ale spolu dají dohromady celou množinu, rozkouskované záznamy v DB.** <br />

![image](https://hackmd.io/_uploads/B11_akc1Mg.png) <br />
Relace je na mnozine castecne usporadani, pokud plati: <br />
![image](https://hackmd.io/_uploads/H16nay9kGl.png) <br />
**NOTE zde menší rovno má být symbol podmnožiny!!** <br />
**Když částečné uspořádání nemá neporovnatelné prvky, okamžitě se z něho stává uplne / lineární uspořádání, kde jde vše porovnat.** <br />

![image](https://hackmd.io/_uploads/Bky8ke5kze.png) <br />
#### C. Funkce
##### FNCE
**NOTE: funkce, zobrazení, transformace beru taktéž jako ekvivalentní pojmy, i když transformaci je lepší chápat jako "movement" v textu... Relace lowkey beru jako skoro ekvivalentní k funkcím, simplisticky to stačí.** <br />
![image](https://hackmd.io/_uploads/ByKAgeqyze.png) <br />
Funkce dle analýzy: <br />
![image](https://hackmd.io/_uploads/H1EjQus1fl.png) <br />
![image](https://hackmd.io/_uploads/BJfmNujyMg.png) <br />
![image](https://hackmd.io/_uploads/HkdDI_syfe.png) <br />

**Co je to ten obraz?** <br />
**Máme zobrazení A : U -> V (operátor), případně
A : U -> U (lineární transformace, ale taky může být do V)** <br />
**Při zobrazení platí pravidla již zmíněné pro vektory - asoc., komut. a distib. pro sčítání, násobek se skalárem. Dále obecně pro zobrazení máme definovanou "nulu" a zobrazení opačné / negativní... A(0) = 0, A(-v) = A(v).** 
**Když** lin. **transformujeme**, tak **zachováváme polohu originu** a také to, že **čáry zustanou čárami**, **paralelní a rovnoměrně odsazené**, **platí i pro "diagonály"** v prostoru. Toto čarování s čárama je právě **ilustrováno** těmi **pravidly**. Diky tomu muzeme mit **transformovane bazove vektory + nejaky vektory**, ktery **chceme taky transformovat** a **zachova se stejna linearni kombinace**.

Take se s **pomoci tech bazovych** da **zobecnit** pro **jakykoliv jiny vektor** - **obrazy báze určují lin. Zobrazení definované na prostorech konečné dimenze, NE ve smyslu limity, ale spíš ovlivnuje "směrem" se budou body transformovat.** Kdyz reverse engineerujeme tranformaci z matice pomocí aplikace transformace na ty basis vectors, a jsou pak v obraze linearne dependent, tak se prostor squishne z 2D na caru 1D tech vektoru.

**Derivace je lineární transformace / operace funkce.** <br />
![image](https://hackmd.io/_uploads/B19vub9yGe.png) <br />
[Hop na limity](#####LIMITY) <br />
[Hop na derivace](#####DERIVACE) <br />

**V případě zobrazování a transformování funkcí se potkáme s U -> R. Pro některé funkce platí stejné pravidla**, **ale ne pro všechny. Příklad pro y = ax, kde f(2) + f(2) by bylo to samé, jako f(2+2), ale toto neplatí pro funkci <br />
f: y = 2x + 1, když dosadíme za "x".** <br />
NOTE: Při další zmínce pravidel pro sčítání a násobek skalárem předpokládejte, že dál referuju na vlastnosti asoc., distib. atd. Také nebudu klarifikovat, co myslím "nulou" nebo "opakem", to by mělo být pak už jasné.

**Prosté lin. zobrazení**, když **existuje jádro N = {0}.** <br />
**Jádro** nebo také **defekt** je **název** pro **nulový prostor N(A)**, jedná se o **množinu vzorů 0**, i.e. **vektory, které se při nějakém zobrazení / transformaci zobrazí na nulu a geometricky se ztratí ten směr, defekt je podprostor U.**

**Obor hodnot H(A) je množina všech obrazů**, **říká se** tomu **i hodnost**, což je podprostor V, to pak **referuje na matice**. Odsud budu referovat na matici A, a na obraz *A*.

**Btw, H(A) = H(*A*).**

**Pro vektor x z podmnožiny R mocněné na m,1 platí: *A*(x) = Ax... *A*(x) doporučuju číst jako efekt transformace na (vektor) x.** <br />
[Zpět na vektory](#####VEKTORY) <br />
WIP skok na matice <br />

**Příklad: pro matici A : x |-> Ax, ve které máme lineární soustavu, má řešení, když pravá strana spadá do oboru hodnot. Jediné řešení existuje, když N(*A*) = 0, d(*A*) = 0 == H(A) = n, kde n je počet neznámých.**

Jediný vektor "jdoucí" na nulu je nulový... kdyby jich bylo víc, tak musí být i víc řešení reflektované i na hodnosti v podmínce, žádné směry se neztratí a žádné dva vstupy neskončí stejně. <br />
WIP skok na soustavy lin. rovnic <br />

**NOTE: písmenko za hranatou závorkou neznačí násobení, pokud nenapíšu "krát"...** <br />
**Lineární transformace blíže:** <br />
**Konečné U,V a báze E, F k nim respectively. Zobrazení *A* : U -> V, vektory matice A(e1,...,em) jsou v zobrazení vyjádřené jako lin. kombinace f1 až fm s koeficienty "a" pro každý vektor, abychom z toho zobrazení dostali čísla v prostoru V. Dostaneme tak matici, kde jsme vyjádřili její vektory z báze E v bázi F. == [A]E,F".** Zobrazili jsme směrem k nějaké bázi:<br />
**Obecně platí [A(x)]F = [A]E,F krát [x]E**, i.e. souřadnice obrazu *A*(x) v bázi F dostanu tak, že matici zobrazení vynásobím souřadnicemi v bázi F.

**Jestli to nedává smysl, zamysli se nad tím, že NEpřevádíme bázi E na F, ale měníme "měřítko".** Kdyby byly báze a prostory ekvivalentní, napíšeme jen [A]E,E, případně [A]E.

***A* : U -> U, *B* : U -> U lin. transformace, pak složené *AB* : U -> U vypadá jako (*AB*)(x) = (*A*(*B*(x))... [AB]E = [A]E[B]E**

**Matice** dané **lin. transformace** v **ruznych bázích** jsou **podobné.** **Charakteristiky** jako **hodnost** a **defekt** pro **lineární transformace** absolutně **nejsou závislé na bázi prostoru.** Prostě a jednoduše **obrazy** mají **podobné charakteristiky**, což **souvisí se změnou báze**: <br />
* Každý sloupec matice T je: T = [[e1]F,...,[em]F]E
* [A]F = T krát [A]E krát Tna-1
* Ctvercove matice A,B podobné, když existují regulární matice T tak, že A = T krát B krát Tna-1 <br />
WIP skok na matice <br />

![image](https://hackmd.io/_uploads/H16n7_jkfe.png) <br />
![image](https://hackmd.io/_uploads/rJRp7_oJMx.png) <br />
![image](https://hackmd.io/_uploads/SkCAX_jyzl.png) <br />
![image](https://hackmd.io/_uploads/H1CeVdikGx.png) <br />
**Vlastnosti funkcí:** <br />
![image](https://hackmd.io/_uploads/Sy-S4Oikfl.png) <br />
![image](https://hackmd.io/_uploads/HkkDEdo1Gx.png) <br />
![image](https://hackmd.io/_uploads/r1K2E_okzg.png) <br />
![image](https://hackmd.io/_uploads/rJsp4Oj1Mg.png) <br />
![image](https://hackmd.io/_uploads/H1gRVuiyfe.png) <br />

![image](https://hackmd.io/_uploads/SJr4SuiJfe.png) <br />
Log. funkce je inverzni exp., konstantni funkce v urovni 0 na ose x je nulova funkce. <br />
![image](https://hackmd.io/_uploads/H1jvrdokzx.png) <br />
![image](https://hackmd.io/_uploads/SJUOHdoJfg.png) <br />
![image](https://hackmd.io/_uploads/Sk0sr_okzx.png) <br />
![image](https://hackmd.io/_uploads/Skd6B_syGx.png) <br />

Hyperbolické funkce, pravděpodobně ne upe important: <br />
![image](https://hackmd.io/_uploads/SyAJL_iyzx.png) <br />
![image](https://hackmd.io/_uploads/B16eIuo1fl.png) <br />
![image](https://hackmd.io/_uploads/ryBWUOjkfg.png) <br />
![image](https://hackmd.io/_uploads/S1C-IOikGx.png) <br />

### 1.4) Kongruence a mod. algebra, dělitelnost
#### A. Kongruence
##### KONGRUENCE
[Kongruence souvisí zpětně s inkluzí a exkluzí](#####INKLUZE_EXKLUZE) <br />
![image](https://hackmd.io/_uploads/HJsu6rqJGe.png) <br />
![image](https://hackmd.io/_uploads/Skza6S51Ge.png) <br />
Dělení totiž vytváří novou hodnotu / nový prvek, relace jen zobrazuje nějakou skutečnost. U dělitelnosti platí asoc., komut. a přehazování stran.

Mějme celá čísla b, c a nenulové celé číslo a. Platí: <br />
Jestliže a b a současně a | c, pak a | (b+c). Jestliže a | b pak a | bc pro všechna celá čísla c. Jestliže a ba současně b | c, pak a ❘ c.

Mějme celá čísla b, c a nenulové celé číslo a. Jestliže a | b a současně <br />
a | c, pak a ❘ rb + sc pro libovolná celá čísla r, s.

**Každé celé číslo lze při dělení nenulovým číslem jednoznačně rozložit na součin dělitele a jednoho konkrétního podílu plus jeden přesně určený zbytek, který je menší než dělitel: 17=5⋅3+2**... Operace div dává celý podíl po dělení, zatímco mod dává zbytek po tomto dělení, zmíním znova v FPR.

**Kongruence: Mějme celá čísla a, b a přirozené číslo m. Řekneme, že čísla a, b jsou kongruentní modulo m, jestliže dávají stejný zbytek po dělení číslem m. Zapisujeme: <br />
a ≡ b (mod m) <br />
Formálně můžeme pomocí operace ,,mod" zapsat <br />
a ≡ b (mod m)⇔ a mod m ≡ b mod m** <br />
![image](https://hackmd.io/_uploads/SJ_QbU5yMl.png) <br />
![image](https://hackmd.io/_uploads/H1P0-UqkGg.png) <br />
(zase jsem byl lenoch s formátováním, jebe mi už z toho DIM a z toho, že nemohu kopčit text z prezentace jednoduše) <br />
![image](https://hackmd.io/_uploads/rJDNMLqkGx.png) <br />
**Pokud největší společný dělitel čísla a a modulu m je větší než jedna, inverze čísla a modulo m neexistuje.** <br />
![image](https://hackmd.io/_uploads/SkZSz89kGg.png) <br />
![image](https://hackmd.io/_uploads/BkvvzI9JMe.png) <br />
**V kongruencích lze krátit jen opatrně, buď číslem nesoudělným s modulem, nebo společným dělitelem obou stran i modulu - Bezout. věty.** <br />
![image](https://hackmd.io/_uploads/rJLKNUcyGl.png) <br />
![image](https://hackmd.io/_uploads/rkU5EI5kMx.png) <br />
Ale abychom to nezkoušeli postupně, tak použijem toho Bezouta. <br />
* Hledáme: 3x ≡ 1 (mod 7)
* Tedy řešíme: 3x + 7y ≡ 1
* Využijeme Euklid alg. a vyjádříme 1:
* 7=2.3+1
* 1=7-2.3
* Porovnáme s tím co řešíme a dosadíme za x,y: 1=(−2)⋅3+1⋅7
* Tedy: x=-2
* Modulo 7: −2 ≡ 5 (mod7)
* Takže: 3 umocněné na −1 ≡ 5 (mod7) <br />
![image](https://hackmd.io/_uploads/ByjyuL9JGg.png) <br />
![image](https://hackmd.io/_uploads/S1-x_89yMg.png) <br />

![image](https://hackmd.io/_uploads/Bygg9U9yfg.png) <br />
![image](https://hackmd.io/_uploads/S1Cl5I5JMx.png) <br />
##### A.I: Čínská zbytková věta
**Čínská zbytková věta se řeší tak, že každá kongruence nejdřív popisuje všechna svá řešení pomocí obecného tvaru... například x≡1(mod5) znamená x=1+5t, kde t je libovolné celé číslo a jen značí, že řešení se opakují po násobcích modulu. Místo hledání čísla, které splňuje víc podmínek najednou, se řeší jednodušší kongruence pro parametr. Ten obecný výraz se pak dosadí do další kongruence, čímž se odstraní x a vznikne jednodušší rovnice pro nový parametr t. Ten se znovu vyřeší stejným způsobem a dosadí zpět. Opakováním tohoto postupu se postupně skládají všechny podmínky dohromady, až vznikne jeden společný tvar řešení, který splňuje všechny kongruence najednou. Postupně redukujeme soustavu o jednu rovnici a neznámou.** <br />

[Dopředně na kombinatoriku](#####KOMBI) <br />

### 1.5) Posloupnosti a rekurence
#### A. Posloupnosti
##### POSL
![image](https://hackmd.io/_uploads/r1uxqZ5kGl.png) <br />
![image](https://hackmd.io/_uploads/B14-c-cyMe.png) <br />
![image](https://hackmd.io/_uploads/S1Sr5bcJGl.png) <br />
![image](https://hackmd.io/_uploads/rkp8iW9kGg.png) <br />
![image](https://hackmd.io/_uploads/r1gtjbc1Gg.png) <br />
![image](https://hackmd.io/_uploads/r1VCiW5JMg.png) <br />
K otázce, ano, konstaní posloupnosti, je jich víc, ale "ne nekonečně mnoho" - nepočítá se každé číslo jako konstanta, spíš typy, co tak chápu. <br />
![image](https://hackmd.io/_uploads/Bk993bc1zg.png) <br />
[Hned k limitám](#####LIMITY) <br />
Posloupnosti dle analýzy: <br />
![image](https://hackmd.io/_uploads/BJ_qUdsJzl.png) <br />
![image](https://hackmd.io/_uploads/SJrJvds1fl.png) <br />
![image](https://hackmd.io/_uploads/r1oVPOikfg.png) <br />
Pro každé kladné číslo ε existuje přirozené číslo n0 takové, že pro všechny indexy n větší než n0 je vzdálenost členu an od čísla a menší než ε. Jinými slovy: od určitého místa v posloupnosti už všechny další členy zůstávají dost blízko limity. <br />
![image](https://hackmd.io/_uploads/Byj_KOiyze.png) <br />
![image](https://hackmd.io/_uploads/B1c-2_i1zg.png) <br />
(nechtělo se mi to přepisovat) <br />
![image](https://hackmd.io/_uploads/HJJI2uiyzg.png) <br />
WIP A dál v limitách... <br />

#### B. Rekurence
V další kapitole se bude probírat kombinatorika, avšak ta nestačí na některé ulohy, napr. pocet prvku ve sjednoceni mnozin. Dalsi priklad uziti rekurentnich alg. je merge sort, obecne ulohy dynamickeho programovani, pocty uzavorkovani n+1 cinitelu s n zavorkama. <br />
WIP LINK NA PROGRAMKO OBECNE <br />
WIP LINK NA FPR <br />
WIP LINK NA ALG <br />

**1) U Fibonacciho víme, že první dva členy se rovnají 1, zanořujeme se, dokud k nim nedorazíme, každý člen je součet dvou předchozích: F(n) = F(n-1) + F(n-2)**

**2) U Hanojských věží se snažíme přemístit disky z jedné tyčky na druhou, třetí je pomocná. Všechny až na jednu přesuneš na pomocnou tyčku a největší disk hodíš na konečnou tyčku, pak všechny disky z pomocné tyčky přesuneš na konečnou tyčku, ale furt je to "n" bez jedné, který přesouváme: <br />
T(1) = 1 <br />
T(n) = 2·T(n-1) + 1** <br />
**Osamocená jednička je pro operaci s velkým diskem.**

**3) Hledáme počet bitových řetězců délky n bez dvou sousedních nul. Označme tento počet aₙ. Každý řetězec buď končí 1 (pak předchozích n-1 bitů tvoří platný řetězec) nebo končí 0 (pak předchozí bit musí být 1, a před ním stojí platný řetězec délky n-2). Tím dostaneme rekurenci: <br />
aₙ = aₙ₋₁ + aₙ₋₂,  začátky: a₁ = 2 (0 nebo 1),  a₂ = 3 (11 nebo 01 nebo 10) <br />
Obdoba fibonacciho s jiným začátkem.**

**4) Dekadická kódová slova se sudým počtem nul. Hledáme počet n-ciferných slov z číslic 0–9 obsahujících sudý počet nul. Označme tento počet xₙ, s tím, že v rekurenci kontrolujeme xₙ₋₁, které považujme za sudé. 10ⁿ⁻¹ jsou všechny možné řetězce. Přidáním cifry 1 až 9 na konec platného slova délky n-1 vznikne opět platné slovo (9xₙ₋₁ možností). Přidáním 0 se sudost počtu nul překlopí... platné se stane neplatným a naopak, tedy přibude 10ⁿ⁻¹ - xₙ₋₁ platných slov, i.e. všechny řetězce bez sudých. Tím dostaneme rekurenci:
xₙ = 8xₙ₋₁ + 10ⁿ⁻¹,  x₁ = 9**
**Sečetli jsme, proto to vypadá trochu jinak.** <br />

![image](https://hackmd.io/_uploads/rJuuSV9Jze.png) <br />
**Operátor rozdělí výraz na levou část (k členů) a pravou část (n-k členů). Počet uzávorkování každé části se násobí a sečte přes všechna možná místa rozdělení.**

Rekurentní rovnice jsou o tom, že najdeme vztah pro n-tý člen, stejně jako u alg. problémů nahoře, definovali jsme winning condition, první členy, možnosti kudma se algoritmus může vydat... <br />
![image](https://hackmd.io/_uploads/Skahd45kGx.png) <br />
**Ještě jednou, každý nový člen vznikne jako pevná (lineární) kombinace k předchozích členů, kde Céčka od 1 do k jsou konstanty nezávislé na n. Říká se jí „lineární“, protože jde jen o součet násobků předchozích členů, „homogenní“ znamená, že celý výraz je složený pouze z těchto členů posloupnosti... nevyskytuje se tam žádný dodatečný „vnější“ člen (např. +1, +n nebo jiná funkce n), který by do posloupnosti vstupoval nezávisle na jejích hodnotách. Také je tam „řád k“, protože závisí na "k" předchozích hodnotách.

Aby byla posloupnost jednoznačně určená, je potřeba znát prvních k členů. Hanojské věže a problém se sudým počtem nul v kodu nejsou případ homogenní r.r., protože máme operaci s největším diskem a u kodovaného slova 10ⁿ⁻¹ (všechny možné řetězce) není násobek ai, ale jinak je stejně jako fibonacci nebo bit. řetězec lineární a s konstantními koef. Catalanová řada se závorkama není lineární, protože Céčkové členy NASOBIME, NESECITAME a není pevného řádu protože počet sčítanců roste s "n".** <br />
![image](https://hackmd.io/_uploads/r1yysE91fx.png) <br />
![image](https://hackmd.io/_uploads/HyoaoN9Jzg.png) <br />
![image](https://hackmd.io/_uploads/HkMTOBc1fl.png) <br />
![image](https://hackmd.io/_uploads/H1rv0NqJze.png) <br />
(sorry to jsem byl líný upravovat formatting z prezentace, tak jsem to hodil chatovi) <br />
![image](https://hackmd.io/_uploads/B171QB51Gl.png) <br />
![image](https://hackmd.io/_uploads/S18XyS9kze.png) <br />
**Po dosazení máme totiž:** <br />
![image](https://hackmd.io/_uploads/r1yqgB5yfl.png) <br />
**TO JE TEN POSUN INDEXU A NASOBENI STEJNYM CISLEM, subscript z obecneho vztahu se hodi k těm "r".** **Vytkne se n-2, trochu se pouprací rovnice, abychom se zbavili "n" v mocninách a postaví se k nule, vznikne to, co je první krok na předchozím screenu.** <br />
![image](https://hackmd.io/_uploads/ByNH1rc1fl.png) <br />
**Zde je v subskriptu r nula, aby se to nepletlo, je jen jedno číslo pro jeden kořen. ** <br />
![image](https://hackmd.io/_uploads/B1lDkrckzl.png) <br />
Kořeny charakteristické rovnice určují základní „způsoby vývoje“ řešení rekurentní rovnice. Vývoj rekurence znamená, jak se hodnoty posloupnosti mění při postupném počítání dalších členů z předchozích (např. růst, pokles nebo kmitání). Každý kořen r odpovídá tvaru r^n, který představuje jeden typ vývoje. Tyto tvary jsou "nezávislé směry", protože popisují různé chování posloupnosti a nejdou získat jako násobek jiného. Rekurence 2. řádu má vždy dva stupně volnosti, protože je určena dvěma počátečními hodnotami, takže potřebuje dva nezávislé směry.

Pokud má rovnice dva různé kořeny r1 ≠ r2, jde o dva různé typy vývoje (např. různé rychlosti růstu nebo poklesu), a řešení je: <br />
a_n = A1 r1^n + A2 r2^n.

Pokud má jeden dvojnásobný kořen r0, existuje jen jeden základní vývoj r0^n, což nestačí pro 2 stupně volnosti. Proto se přidává druhý nezávislý tvar n·r0^n, kde faktor n znamená postupně rostoucí odchylku od čisté exponenciály, i.e. je to nejjednodušší funkce, která stále vyhovuje struktuře rekurence, ale už není jen jejím násobkem, takže dává nové nezávislé chování. Není už jen násobek puvodniho rustu.

Pokud rovnice nemá reálné kořeny (např. i, -i), vývoj je stále určen dvěma nezávislými složkami, ale projeví se jako oscilace (sinus a kosinus), tedy posloupnost kmitá místo čistého růstu či poklesu.

**TLDR: různé reálné kořeny = různé exponenciální vývoje; dvojnásobný kořen = jeden exponenciální + nutnost přidat n·r0^n pro druhý nezávislý vývoj; komplexní kořeny = oscilující vývoj.** <br />
![image](https://hackmd.io/_uploads/ryC5Kr5Jfe.png) <br />
**Řešení nehomogenní rekurence je vždy součet přirozeného chování systému (homogenní řešení) a jednoho konkrétního chování způsobeného vnějším vstupem F(n) (partikulární řešení). Ten vnější vstup tipnem a ověříme dosazením.** <br />
![image](https://hackmd.io/_uploads/rJ4HqS9JMe.png) <br />
**Tady se tipnulo nějaké cn + d, protože napravo v zadané rovnici je "n", působí lineárně.** <br />
![image](https://hackmd.io/_uploads/HkJAcH5yMx.png) <br />
![image](https://hackmd.io/_uploads/SkMUoB9yMg.png) <br />
**Partikulární řešení je polynom krát exponenciála, ale pokud je exponenciála už v homogenní části (např. 10 mocněné na "n", kdy 10 je kořenem charakteristické rovnice), musíš celý tvar vynásobit n mocněné na m, aby vzniklo nové nezávislé řešení.**

**U tvaru obec. řešení určíme konstantu až na konec, jakmile budeme znát partikulární řešení. Když nemáme pevný řád, nespočteme homog. rekurentní rovnici.**

WIP LINK NA LA spektrální teorii <br />

### 1.6) Kombinatorika a pravděpodobnost, binomická věta
#### A. Kombinatorika
##### KOMBI
**Výběr prvků z nějaké množiny, uspořádaně vs neuspoř. (zda a,b,c je to samé jako b,c,a nebo ne) a nebo s / bez opakování - kombinatorika.** **V kombinatorice je posloupnost uspořádaná n-tice prvků, ne posloupnost ve smyslu arit. nebo geomet. posloupnosti z vyšší kapitoly.** <br />
![image](https://hackmd.io/_uploads/BJ_00b9kGx.png) <br />

K-prvková **kombinace bez opakování** na n-prvkové množině X **je libovolný NEuspořádaný výběr** "k" prvků této **množiny**, které značíme C(n,k) <br />
![image](https://hackmd.io/_uploads/ByKu1f9Jfg.png) <br />
**Basically vybíráme postupně prvky z méně a méně možností, zajímá nás, co vyberem, a zbytek zahodíme.**

K-prvková **variace bez opakování** na n-prvkové množině X **je libovolný uspořádaný výběr** "k" prvků této **množiny**, které značíme V(n,k) <br />
![image](https://hackmd.io/_uploads/rJf6yGcJfg.png) <br />
![image](https://hackmd.io/_uploads/ryDeMG5yzl.png) <br />
**Basically vybíráme postupně prvky z méně a méně možností, zajímá nás, co vyberem, a zbytek zahodíme. U variace záleží na pořadí, reflektované v absenci k!, v tom slajdu je to blbě.** <br />
![image](https://hackmd.io/_uploads/ryX5Gz51Gg.png) <br />
![image](https://hackmd.io/_uploads/ByR8QG9kGl.png) <br />
![image](https://hackmd.io/_uploads/B1Vv7fcyze.png) <br />
**Každý hráč má pevnou roli. Utočník nemůže být vybrán jako obránce, čiže výběr útočníků vůbec neovlivní, kteří obránci jsou k dispozici. Množiny jsou disjunktní.** <br />
![image](https://hackmd.io/_uploads/HyADmM5JGl.png) <br />
**Jeden hráč může hrát útočníka i obránce. Jako útočník, zmizí z množiny obránců. Najednou závisí na tom, co jsme předtím vybrali.** <br />

**Permutace s opakováním, dělíme zde duplicity:** <br />
![image](https://hackmd.io/_uploads/HyaHVf5JGg.png) <br />
![image](https://hackmd.io/_uploads/Byaz4GcJfx.png) <br />
![image](https://hackmd.io/_uploads/SkO74G5kfl.png) <br />
**Narozdíl od první permutace tu je nějaký "předepsaný počet", i.e. určíme si, kolikrát chceme písmenko v stringu a hledáme permutace s tímto počtem.** <br />
WIP LINK PERMUTACE V MNOZINACH <br />

![image](https://hackmd.io/_uploads/B1ob8G9JGe.png) <br />
![image](https://hackmd.io/_uploads/Hk92Of91fl.png) <br />
**Multimnožina je prostě množina, kde se prvky mohou opakovat.** <br />
![image](https://hackmd.io/_uploads/rJ7uUM5Jfg.png) <br />
![image](https://hackmd.io/_uploads/rJCt8MqJfe.png) <br />
![image](https://hackmd.io/_uploads/H1oCtfcyGe.png) <br />

#### B. Pravděpodobnost
**Diskrétní pravděpodobnost:** <br />
**Konečný pravděpodobnostní prostor, vycházíme z četnosti nějakého jevu, což je číslo mezi 0 a 1: pravděpodobnost = četnost jevu / počtu pokusů.** <br />
**Konečný pravděpodobnostní prostor** je **dvojice (O,P)**, kde **základní prostor O je konečná množina elementárních jevů** a **P je funkce pravděpodobnosti.** Tato **dvojice každé podmnožině A z O (náhodný jev) přiřadí číslo P(A) (jeho pravděpodobnost) z intervalu 0 až 1.** <br />
* **P(∅) = 0** <br />
* **P(O) = 1 TOTO NENI NULA, ALE PISMENO O** <br />
![image](https://hackmd.io/_uploads/SJ4BTf9JMe.png) <br />
![image](https://hackmd.io/_uploads/rJlHTf51Ml.png) <br />
**Disjunktní jevy nemohou nastat současně, i.e. A punik B rovno prázdné množině.** <br />
**Když** je **každý elementární jev stejně pravděpodobný**, tak **se jedná** o **uniformní prostor**. **Pravděpodobnost jevu A je relativní velikost A vzhledem k O, protože prostoru O je uniformní pravděpodobnost přiřazena P(A) = |A| / |O|** <br />
![image](https://hackmd.io/_uploads/ByHHCzqyzx.png) <br />
**Prvek e z množiny O v pravděpodobnostní funkci postavené k celku dělený s velikostí O.** <br />
![image](https://hackmd.io/_uploads/SyLlkQ5kze.png) <br />
Příklad s fakeovou mincí a kloboukem. <br />
![image](https://hackmd.io/_uploads/B1hV1mqyzx.png) <br />
[Logika jen kvuli mention negace](#####LOGIKA) <br />

![image](https://hackmd.io/_uploads/ByUpJ7q1Ml.png) <br />
![image](https://hackmd.io/_uploads/S1y-xQ9kMl.png) <br />
**Střední hodnota = "vážený průměr" všech možných výsledků.**
Hod kostkou, možné hodnoty jsou 1–6, každá s pravděpodobností 1/6. Házíme miliardkrát, **průměrný výsledek se bude blížit k nějakému číslu**. To číslo je **střední hodnota**. <br />
![image](https://hackmd.io/_uploads/HJHWWXq1zx.png) <br />
![image](https://hackmd.io/_uploads/B1GSb7qJMg.png) <br />
**Každou možnou hodnotu vynásobíme její pravděpodobností a všechno sečtem. Hodnoty které nastávají často (vysoká p) přispívají hodně. Hodnoty které nastávají zřídka (nízká p) přispívají málo.** <br />
![image](https://hackmd.io/_uploads/HkRTfQ5kMe.png) <br />
Dvojka umocněná na "n", jako dvě možnosti pro každé "n" - je nebo není ve výběru. Mínusko jen protože inverzujeme, abychom dostali pravděpodobnost z celku. <br />
![image](https://hackmd.io/_uploads/HJegN791zx.png) <br />
![image](https://hackmd.io/_uploads/B1LgNm91fe.png) <br />
![image](https://hackmd.io/_uploads/B13gVQcyfx.png) <br />
![image](https://hackmd.io/_uploads/HkpXP79JGg.png) <br />
![image](https://hackmd.io/_uploads/HkdrvQqyMg.png) <br />
Zleva doprava a shora dole pricitani. <br />
![image](https://hackmd.io/_uploads/SJPPO75kMx.png) <br />
#### C. Binomická věta
**Binomicka veta nam rika, jak efektivne rozepsat vyraz a vychazi z kombinacniho cisla. Rika take: vsech podmnozin n-prvkove mnoziny je dvojka mocnena na "n", protoze n-prvkova mnozina ma stejny pocet podmnozin sude a liche velikosti, to jsou dve moznosti.** <br />
![image](https://hackmd.io/_uploads/B1_z5Q5JMg.png) <br />
![image](https://hackmd.io/_uploads/rJPB5m5kzl.png) <br />

#### Grafy, izomorfismus, souvislosti, komponenty, metriky, kostry, barevnost, rovinnost, sítě A STROMY
+ Hledání v grafech, Euler, Hamilton, ... <br />
WIP LINK NA ALG <br />

### 1.7) Matice, lineární rovnice a nerovnice s aproximací, hodnost, determinant, spektrální teorie
#### A. Matice a lin. rovnice + další věci k nim

#### B. Spektrální teorie

### 1.8) Limity, derivace, integrály:
![image](https://hackmd.io/_uploads/SyAWevqyMe.png) <br />
![image](https://hackmd.io/_uploads/BJYXlPqkGl.png) <br />
"Horní odhad množiny je takové číslo, které je větší nebo rovno všem prvkům dané množiny, zatímco dolní odhad je číslo, které je menší nebo rovno všem jejím prvkům. Supremum množiny je nejmenší z jejích horních odhadů, tedy nejnižší číslo, které ještě „leží nad“ celou množinou, a infimum je naopak největší z dolních odhadů, tedy nejvyšší číslo, které je stále „pod“ všemi prvky množiny. Intuitivně supremum představuje nejbližší horní hranici množiny a infimum nejbližší dolní hranici, přičemž tyto hodnoty nemusí být samotnými prvky množiny." <br />

[Link na množinussi](#####MNOZINY) <br />

Množina je shora omezená, pokud existuje číslo, které je větší nebo rovno všem jejím prvkům, a zdola omezená, pokud existuje číslo, které je menší nebo rovno všem jejím prvkům. Pokud je omezená shora i zdola zároveň, říkáme, že je omezená, a pokud ani jedna z těchto vlastností neplatí, je neomezená. Supremum je nejmenší horní odhad množiny, tedy nejnižší číslo, které je stále nad celou množinou, zatímco infimum je největší dolní odhad, tedy nejvyšší číslo, které je stále pod všemi prvky množiny. Maximum je největší prvek, který v množině skutečně leží, a minimum je nejmenší prvek, který v ní skutečně leží; pokud existují, pak platí, že maximum je zároveň supremum a minimum je zároveň infimum.

Například množina (-1,1) neobsahuje krajní body, takže minimum ani maximum neexistují, ale infimum je -1 a supremum je 1. Množina kladných reálných čísel R+ nemá ani minimum ani maximum, protože je neomezená shora i zdola, přičemž infimum je 0 a supremum je +∞. Množina {0} obsahuje jediný prvek, takže minimum i maximum jsou rovny nule a zároveň infimum i supremum jsou také nula. U množiny {1/n : n ∈ N} je maximum rovno 1, minimum neexistuje, infimum je 0 a supremum je 1.

Vztahy mezi těmito pojmy lze chápat tak, že maximum je vždy stejné jako supremum, pokud maximum existuje, a minimum je stejné jako infimum, pokud minimum existuje. Dále platí, že supremum množiny M souvisí s infimem množiny -M tak, že sup M = -inf(-M).

U funkce sinus platí, že její hodnoty leží mezi -1 a 1, takže infimum je -1 a supremum je 1, ale minimum ani maximum neexistují, protože těchto hodnot funkce nikdy přesně nedosáhne. U množiny řešení nerovnice x^2 + 3x - 6 ≥ 0 nejprve najdeme kořeny kvadratické rovnice, které rozdělují reálnou osu na intervaly. Protože parabola je otevřená nahoru, množina řešení je tvořena krajními intervaly a není omezená ani shora ani zdola, takže nemá maximum ani minimum, infimum je -∞ a supremum je +∞.

#### A. Limity
##### LIMITY
[Zpátky na funkce](#####FNCE) <br />
TODO bold text
[Znova z posloupností](#####POSL) <br />
![image](https://hackmd.io/_uploads/H1Nm6djyGe.png) <br />
![image](https://hackmd.io/_uploads/S1qE6_okGe.png) <br />
Pokud je posloupnost neklesající, pak její limita (pokud existuje v rozšířených reálných číslech) je rovna supremu jejích členů:  <br />
Posloupnost jen roste (nebo zůstává stejná), „nejvyšší hodnota, ke které se může přiblížit“ je její nejmenší horní závora (supremum), protože nikdy nepřeskočí nahoru nad své supremum, ale může se k němu přibližovat.

Pokud je posloupnost nerostoucí, pak její limita je rovna infimu jejích členů: <br />
Posloupnost jen klesá (nebo zůstává), „nejnižší hodnota, ke které se může dostat“ je největší dolní závora (infimum), nikdy nepůjde pod ni, ale může se k ní přiblížit. Pokud jsou „jednostranně řízené“ (jen rostou nebo jen klesají), tak jejich chování je úplně určeno jejich hranicemi, supremem nebo infimem. <br />
![image](https://hackmd.io/_uploads/r1bETOoyMl.png) <br />
![image](https://hackmd.io/_uploads/HJQwT_s1Gl.png) <br />
![image](https://hackmd.io/_uploads/BJ-_C_skzg.png) <br />
![image](https://hackmd.io/_uploads/BJq_0ujyGx.png) <br />
![image](https://hackmd.io/_uploads/SylAAOokGx.png) <br />
![image](https://hackmd.io/_uploads/rJTDgFskfg.png) <br />
Věta o dosazení mezi dvě funkce: pokud jedna funkce je vždy mezi dvěma jinými funkcemi, které mají stejnou limitu v bodě x0, pak i ta „prostřední“ funkce má stejnou limitu. To se často používá pro odhady.

Limita funkce lim f(x) = a znamená, že když se x blíží k bodu x0, tak se hodnoty funkce f(x) blíží k číslu a. Jinými slovy, nezáleží na tom, jestli se k x0 přibližujeme postupně přes posloupnost nebo obecně z okolí, výsledek se vždy natlačí k hodnotě a.

Stejná myšlenka: pro každé okolí čísla a existuje nějaké okolí bodu x0, takové že když vezmeme libovolné x dost blízko x0, pak už jsou všechny hodnoty f(x) uvnitř okolí čísla a. To znamená, že funkce se dá „udržet“ libovolně blízko hodnoty a, pokud se dostatečně přiblížíme k x0.

Zprava limita znamená totéž, ale bereme jen hodnoty x, které jsou větší než x0 a blíží se k němu. Zleva limita zase bere jen hodnoty menší než x0. Oboustranná limita existuje právě tehdy, když se shodují limity zleva i zprava.

A spojitost v bodě x0 znamená, že funkce se v tomto bodě nezlomí... formálně to říká, že limita funkce v bodě x0 je stejná jako její hodnota v x0. Ekvivalentně to lze říct i tak, že když vezmeme jakékoli číslo epsilon, existuje nějaké číslo delta (d), že pro všechna x v okolí x0 (vzdálená méně než delta), platí, že hodnoty f(x) se liší od f(x0) o méně než epsilon. Nebo také: když se x_n blíží k x0, pak f(x_n) se blíží k f(x0). <br />
![image](https://hackmd.io/_uploads/Bk2VzKjJMl.png) <br />
![image](https://hackmd.io/_uploads/rynrGtiJzl.png) <br />
![image](https://hackmd.io/_uploads/B16vfFsJGl.png) <br />
Základní elementární funkce (např. sin, cos, polynomy, exponenciála, logaritmus atd.) jsou spojité na svém definičním oboru. Zadne skoky když se x blíží k nějakému bodu, hodnota funkce se automaticky blíží k hodnotě funkce v tom bodě.

Z toho plyne: since jsou tyto funkce spojité, můžeme pro výpočet limit často jednoduše dosazovat. Například pro sinus platí, že je spojitý, takže limita v bodě se rovná hodnotě funkce v bodě, tedy lim x→0 sinx=sin0. (Stejně tak pro kosinus a další elementární funkce.)

Odhady mezi funkcemi pro dokazování (typicky pomocí nerovností mezi sinem a cosinem) a známé limity kosinu v nule, která je 1. Díky tomu, že sinus je sevřen mezi funkcemi, jejichž limita je známá, dostaneme stejnou limitu i pro sinus.

Pokud se argument x blíží k x0 a funkce f(x) se tím blíží k a, a zároveň funkce g(y) se při y→a blíží k b, pak i složená funkce g(f(x)) se blíží k b. Platí to ale jen tehdy, když je vše „dobře definované“ a alespoň jedna z funkcí je spojitá v potřebném bodě.

Varovné příklady ukazují, že když nejsou splněny podmínky (např. složená funkce není vůbec definovaná nebo se chování v bodě "rozbije"), tak i když jednotlivé limity existují, limita složené funkce nemusí existovat nebo nemusí vyjít správně.

#### B. Derivace
##### DERIVACE
[Zpátky na funkce](#####FNCE)
![image](https://hackmd.io/_uploads/SJODjKo1zg.png) <br />
![image](https://hackmd.io/_uploads/By6IoYiJfx.png) <br />
Nejprve se vezmou dva body na grafu funkce a spojí se přímkou – sečna. Když se tyto dva body začnou k sobě přibližovat, sečna se postupně otáčí a její poloha se mění. V limitě, kdy se oba body „splynou“ do jednoho, dostaneme přímku, která se křivky v bodě jen dotýká – tečna. Sklon této tečny pak přesně vyjadřuje derivace: říká, jak rychle funkce v daném bodě roste nebo klesá, tedy jaký má graf v tom místě okamžitý směr. <br />
![image](https://hackmd.io/_uploads/ryk2ots1fe.png) <br />
![image](https://hackmd.io/_uploads/B1zwhYs1zl.png) <br />
Pokud existuje derivace v bodě (ať už vlastní nebo nevlastní), pak musí existovat nějaké okolí tohoto bodu, ve kterém je funkce definovaná, tedy nelze derivaci chápat jen jako hodnotu v izolovaném bodě bez okolí.

Dále platí, že obě běžné formulace derivace jsou ekvivalentní: <br />
Derivaci můžeme chápat jako limitu rozdílu hodnot funkce, nebo jako limitu podílu změn funkce při přibližování k danému bodu, a pokud má jedna z těchto limit smysl, má ho i druhá.

Vlastní derivace znamená, že tato limita vyjde jako konečné reálné číslo, tedy běžný sklon tečny, zatímco nevlastní derivace nastává tehdy, když limita „utíká do nekonečna“ (kladného nebo záporného), což odpovídá situaci, kdy má graf v bodě svislou tečnu a sklon není konečný. <br />
![image](https://hackmd.io/_uploads/SySMhYsJMx.png) <br />
![image](https://hackmd.io/_uploads/BkD63tjkMg.png) <br />
![image](https://hackmd.io/_uploads/ByZJatokze.png) <br />
![image](https://hackmd.io/_uploads/r1k7pFoyfg.png) <br />
![image](https://hackmd.io/_uploads/Sy0mTKi1Mx.png) <br />
Derivací funkce f se rozumí nová funkce f', která každému bodu x přiřadí hodnotu derivace funkce f v tomto bodě, tedy „okamžitý sklon“ grafu v každém bodě, kde existuje. Jinými slovy: derivace už není jen číslo v jednom bodě, ale může být sama funkcí, která popisuje chování sklonu po celém definičním oboru.

Funkce f se nazývá diferencovatelná na intervalu (a,b), pokud má v každém bodě tohoto intervalu derivaci (ta je konečná), a zároveň pokud je na krajích intervalu correct, tedy v levém kraji existuje správná hodnota nebo jednostranné chování a stejně tak v pravém kraji. Intuitivně to znamená, že funkce má všude „hladký lokální sklon“ na celém intervalu, bez ostrých zlomů nebo nespojitostí.

Funkce je spojitě diferencovatelná, pokud je navíc její derivace sama spojitá. To znamená, že nejen že existuje sklon v každém bodě, ale že se tento sklon nemění skokově – mění se plynule. Na koncích intervalu se opět požaduje, aby se chovala spojitě z jedné strany (zprava u levého konce a zleva u pravého). <br />
![image](https://hackmd.io/_uploads/HkmIatiyMe.png) <br />
![image](https://hackmd.io/_uploads/HJja0Ks1fg.png) <br />
![image](https://hackmd.io/_uploads/H1R0CFi1Gl.png) <br />
![image](https://hackmd.io/_uploads/B1f2J5syfg.png) <br />
![image](https://hackmd.io/_uploads/SJlp19j1zx.png) <br />
![image](https://hackmd.io/_uploads/HJTayqjkfg.png) <br />
![image](https://hackmd.io/_uploads/rkIJlciyfl.png) <br />
![image](https://hackmd.io/_uploads/ryL_e9iyfg.png) <br />
Pokud má spojitá funkce na intervalu na jednom konci kladnou a na druhém zápornou hodnotu, pak musí uvnitř intervalu existovat bod, kde je hodnota funkce nulová, protože spojitá funkce nemůže preskocit z kladné do záporné bez průchodu všemi mezihodnotami. Důležité je, že funkce musí být spojitá na celém intervalu, jinak by to neplatilo.

Podobně pokud má funkce derivaci na otevřeném intervalu a tato derivace na krajích nabývá opačných znamének, pak musí existovat bod uvnitř intervalu, kde je derivace rovna nule. Tato podmínka stojí na tom, že derivace se chová mezihodnotově podobně jako spojitá funkce, ale je nutné, aby derivace existovala na celém otevřeném intervalu.

Z toho plyne důležitá vlastnost spojitých funkcí na uzavřeném intervalu jejich obraz nemůže být nesouvislá množina. To znamená, že když vezmeme všechny hodnoty, které funkce na intervalu nabývá, vznikne buď jediný bod když je funkce konstantní, nebo celý interval všech mezihodnot mezi minimem a maximem.

Pokud má navíc funkce na intervalu všude existující a všude nenulovou derivaci, znamená to, že její sklon se nikdy nezastaví a nikdy nepřechází přes nulu. Proto se nemůže změnit směr růstu funkce je pak ryze monotónní, což znamená, že je buď všude přísně rostoucí derivace je všude kladná, nebo všude přísně klesající derivace je všude záporná. Monotónnost zde není jen neklesá neroste ale skutečně bez jakýchkoli lokálních zvratů. <br />
![image](https://hackmd.io/_uploads/HJ8xW5sJfg.png) <br />
![image](https://hackmd.io/_uploads/SypX-5iJMl.png) <br />
![image](https://hackmd.io/_uploads/ryc4W5s1fe.png) <br />
![image](https://hackmd.io/_uploads/H13hWqsyzg.png) <br />

Nejprve pokud v bodě x0 platí že první derivace je nula tedy funkce má tam vodorovnou tečnu a zároveň druhá derivace je kladná znamená to že graf je v okolí bodu prohnutý nahoru jako miska takže bod x0 je ostré lokální minimum. Naopak pokud je první derivace opět nula ale druhá derivace je záporná graf je prohnutý dolů jako kopule a bod x0 je ostré lokální maximum. Tohle je druhá derivace testu extrémů první derivace říká že jsme v kandidátovi na extrém stacionární bod a druhá derivace rozhodne jestli jde o minimum nebo maximum.

Dále se to zobecňuje na vyšší derivace pokud jsou všechny derivace až do řádu n minus jedna v bodě x0 nulové a první nenulová derivace je až n ta pak rozhoduje parita tohoto řádu. Když je n liché funkce v bodě nemá extrém protože se tam chová průchodově graf přechází přes bod bez otočení. Když je n sudé pak znaménko této derivace určuje typ extrému kladné znamená ostré minimum záporné ostré maximum.

Bod kde je první derivace nulová se nazývá stacionární bod protože tam funkce lokálně neubíhá nahoru ani dolů tedy má nulový okamžitý sklon a může tam vzniknout extrém nebo jen placaté místo. <br />
![image](https://hackmd.io/_uploads/B1eLeN9s1zg.png) <br />
![image](https://hackmd.io/_uploads/ryhgVciJzx.png) <br />
![image](https://hackmd.io/_uploads/S1tfE5jyGe.png) <br />
![image](https://hackmd.io/_uploads/HJrXE5sJGl.png) <br />
![image](https://hackmd.io/_uploads/B1gEV9j1fe.png) <br />
![image](https://hackmd.io/_uploads/ryhhEcokMl.png) <br />
![image](https://hackmd.io/_uploads/rk0ENqiJfl.png) <br />
![image](https://hackmd.io/_uploads/H19KV5oJMg.png) <br />
![image](https://hackmd.io/_uploads/SJnqE9iJGx.png) <br />
![image](https://hackmd.io/_uploads/HyPi49jkfg.png) <br />
![image](https://hackmd.io/_uploads/H1hsNcjyze.png) <br />

**Taylor. polynom** <br />
![image](https://hackmd.io/_uploads/H1WtH9iyfg.png) <br />
![image](https://hackmd.io/_uploads/By-crqskMg.png) <br />
![image](https://hackmd.io/_uploads/S1dBUqj1Mg.png) <br />
![image](https://hackmd.io/_uploads/r15_dcjkfl.png) <br />

#### C. Integrály
WIP jump to ZPG kvuli krivkam <br />

u trojneho WIP jump k spektralni teorii<br />

### MATIKA IMPORTANT DEBRIEF !!!
oddelene regularni, ctverec, determinant, reseni, podminky n/k <br />

NOTE 7. dim prezentace temata algoritmicky + univerzum mention další, v 0. bijekce a isomorfismus
sloupcový proator A sedí na obor hodnot A!!!! 
abcd, nejzákladnější výpočet det. s minory a složitost (n-1)n!, det I = 1 (roste a11 na 12 a to samé i M velikost a mezi něma mínus plus mínus PAK EVOLVED NA vezmeš řádek a vynásobíš ho s minor det metodu)
adj matice je transpozice alg. doplňků, když vynásobím A s adj A dostanu det A bo prvky na diagonále korespondují k němu... n na druhou složitost protože operace na každý prvek
det fncí sloupců má stejné vlastnosti jako řádků <br />

### 2.1) Logika zbytek, predikátovka, aristetol., normální formy, rezolučka, ...
#### A. LOGIKA
##### LOGIKA
[Aplikace teorie v DB](#####DATABAZE_TEORIE_NORMALOVE_FORMY) <br />
Screeny z magnum opus, doporučuju projít samostatně zde: https://github.com/Dr00gy/Logicky-magnum-opus-naucny <br />
![image](https://hackmd.io/_uploads/HJMnb7kxzx.png) <br />
![image](https://hackmd.io/_uploads/Bki0Z7JeGx.png) <br />
![image](https://hackmd.io/_uploads/r1ZgM7yeMl.png) <br />
![image](https://hackmd.io/_uploads/rylbMQ1gzl.png) <br />
![image](https://hackmd.io/_uploads/Sk5mzQ1gGe.png) <br />
![image](https://hackmd.io/_uploads/rJvSfXJgfl.png) <br />
![image](https://hackmd.io/_uploads/SklUzQyezx.png) <br />
![image](https://hackmd.io/_uploads/SJ9IGmJefg.png) <br />
![image](https://hackmd.io/_uploads/rJGvzX1gfx.png) <br />
![image](https://hackmd.io/_uploads/SyNtfQJlzx.png) <br />
![image](https://hackmd.io/_uploads/rknFMXJxfe.png) <br />
![image](https://hackmd.io/_uploads/S1VcGQkxzg.png) <br />
![image](https://hackmd.io/_uploads/rycoMQ1lMg.png) <br />
![image](https://hackmd.io/_uploads/SyInzQ1gMg.png) <br />

### 2.2) UTI ultimate
Teoretická informatika je vědní obor na pomezí informatiky a matematiky zabývající se zkoumáním obecných otázek týkajících se algoritmů a výpočtů, zkoumáním různých formalismů pro popis algoritmů, zkoumáním prostředků pro popis syntaxe a sémantiky formálních jazyků (zejména programovacích jazyků) a matematickým přístupem k analýze a řešení problémů. Typické studované otázky jsou: Je možné daný problém řešit pomocí nějakého algoritmu? Jaká je výpočetní složitost tohoto algoritmu? Existuje efektivní algoritmus řešící daný problém? Jak se přesvědčit, že daný algoritmus je korektním řešením? Jaké instrukce musí umět vykonat stroj provádějící daný algoritmus? Další oblasti teoretické informatiky zahrnují teorii složitosti, teorii formálních jazyků, výpočetní modely, paralelní a distribuované algoritmy a další.

#### A. Teorie formálních jazyků
Teorie formálních jazyků je oblast teoretické informatiky zabývající se otázkami týkajícími se syntaxe. Jazyk je množina slov, slovo je sekvence symbolů z určité abecedy, abeceda je množina symbolů (znaků). Slova a jazyky se v informatice objevují při reprezentaci vstupních a výstupních dat, reprezentaci kódu programů, manipulaci s řetězci znaků nebo se soubory. Typické problémy využívající teorii formálních jazyků jsou tvorba překladačů (lexikální a syntaktická analýza) a vyhledávání v textu (hledání vzorku nebo textu zadaného regulárním výrazem). Prostředky používané pro popis formálních jazyků jsou automaty, gramatiky a regulární výrazy.

##### A.I: Abeceda a slovo
Abeceda je libovolná neprázdná konečná množina symbolů (znaků), často označovaná řeckým písmenem Σ (velké sigma). Příklad: Σ = {a, b, c, d}. Slovo v dané abecedě je libovolná konečná posloupnost symbolů z této abecedy. Příklad: cabcbba. Množina všech slov nad abecedou Σ se označuje Σ*. Pro proměnné jejichž hodnoty jsou slova se používají názvy w, u, v, x, y, z apod., případně s indexy. Zápis w = cabcbba znamená, že hodnotou proměnné w je slovo cabcbba; <br />
Zápis w ∈ Σ* znamená, že w je nějaké slovo tvořené symboly z abecedy Σ.
Příklady abeced a slov v nich: Σ₂ = {A–Z, ␣} – slovo HELLO␣WORLD; Σ₃ = {0–9} – slova 0, 31415926536, 65536; Σ₄ = {0,1} – slova 011010001, 111, 101010101010101010; Σ₅ = {a,b} – slova aababb, abbabbba, aaab.

#### B. Formální jazyk
(Formální) jazyk L v abecedě Σ je nějaká libovolná podmnožina množiny Σ*, tj. L ⊆ Σ*. <br />
Příklad pro Σ = {a, b, c}: jazyk L₁ = {aab, bcca, aaaaa}; jazyk L₂ = {w ∈ Σ* | počet výskytů symbolu b ve slově w je sudý}. <br />
Příklad: množina {00, 01001, 1101} je jazyk v abecedě {0,1}; množina všech syntakticky správných programů v jazyce C je jazyk v abecedě tvořené množinou všech ASCII znaků; množina všech textů obsahujících sekvenci znaků ahoj je jazyk v abecedě tvořené množinou všech ASCII znaků.

**Kódování vstupu a výstupu:** <br />
U algoritmických problémů často předpokládáme, že vstupy i výstupy jsou kódovány jako slova v nějaké abecedě Σ.<br />
Například u problému „Třídění" bychom mohli zvolit abecedu Σ = {0,1,2,3,4,5,6,7,8,9,,}; <br />
vstupem by pak mohlo být slovo 826,13,3901,128,562 a výstupem slovo 13,128,562,826,3901. Ne každé slovo ze Σ* musí reprezentovat nějaký vstup; kódování bychom ale měli zvolit tak, abychom byli schopni snadno poznat ta slova, která nějaký vstup reprezentují.

Vztah mezi rozpoznáváním formálních jazyků a rozhodovacími problémy
Každému jazyku L nad abecedou Σ odpovídá rozhodovací problém: vstup je slovo w nad Σ, otázka zní, zda slovo w patří do jazyka L. Ke každému rozhodovacímu problému P, jehož vstupy jsou kódovány jako slova nad abecedou Σ, existuje odpovídající jazyk L obsahující právě ta slova w, pro která je odpověď na otázku problému P „ANO". <br />
Příklad: rozhodovací problém „Obsahuje slovo w nad {a,b} sudý počet výskytů symbolu b?" odpovídá jazyku L = {w ∈ {a,b}* | slovo w obsahuje sudý počet výskytů symbolu b}.

#### C. Výpočetní modely
##### UTI_MODELY_AUTOMATY
[Automat v praxi](#####HW_PAMET) <br />
Různé druhy strojů provádějících algoritmy se liší tím, jaké instrukce jsou schopny provádět, jaký druh paměti používají a jak je tato paměť organizována. Různé druhy takovýchto strojů se označují jako různé výpočetní modely; v případě velmi jednoduchých druhů strojů se v teorii formálních jazyků označují jako automaty. Pro různé druhy výpočetních modelů zkoumáme: jaké algoritmické problémy jsou schopny řešit a jaké jazyky rozpoznávat, jak efektivně realizují různé algoritmy, jakým způsobem může určitý druh stroje simulovat jiný druh stroje a jak při takové simulaci narůstá počet provedených instrukcí.

**Základní pojmy – délka slova, prázdné slovo:** <br />
Délka slova je počet znaků ve slově; délku slova w označujeme |w|. <br />
Příklad: délka slova abaab je 5. Počet výskytů znaku a ve slově w označujeme |w|ₐ. <br />
Příklad: pokud w = cabcbba, pak |w| = 7, |w|ₐ = 2, |w|ᵦ = 3, |w|꜀ = 2, |w|ᵈ = 0. <br />
Prázdné slovo je slovo délky 0, tj. slovo neobsahující žádné znaky; označuje se řeckým písmenem ε (epsilon), přičemž |ε| = 0.

**Zřetězení slov:** <br />
Se slovy je možné provádět operaci zřetězení; například zřetězením slov cabc a bba vznikne slovo cabcbba. Operace zřetězení se označuje symbolem · (podobně jako násobení), který lze vypouštět. Pro u, v ∈ Σ* zapisujeme zřetězení buď jako u · v nebo jen uv.

Zřetězení je asociativní: pro libovolná tři slova u, v a w platí (u · v) · w = u · (v · w); <br />
díky tomu lze závorky při více zřetězeních vypouštět.

Slovo ε je pro operaci zřetězení neutrálním prvkem: ε · w = w · ε = w. <br />
Pokud daná abeceda obsahuje alespoň dva různé symboly, není operace zřetězení komutativní (např. a · b ≠ b · a). <br />
Z formálního hlediska je zřetězení slov nad abecedou Σ funkcí typu Σ* × Σ* → Σ*.

**Mocnina slova:** <br />
Pro libovolné slovo w ∈ Σ* a libovolné k ∈ ℕ definujeme slovo wᵏ jako slovo vzniklé zřetězením k kopií slova w. <br />
Příklad: pro w = abb je w⁴ = abbabbabbabb. <br />
Formální induktivní definice: w⁰ = ε; wᵏ⁺¹ = wᵏ · w pro k ∈ ℕ.

**Zrcadlový obraz slova:** <br />
Zrcadlový obraz slova w je slovo w zapsané pozpátku, označuje se wᴿ. Příklad: w = abbab, wᴿ = babba. Pokud w = a₁a₂···aₙ (kde aᵢ ∈ Σ), pak wᴿ = aₙaₙ₋₁···a₁. Formálně lze wᴿ definovat pomocí induktivně definované funkce rev: Σ* → Σ* jako hodnotu rev(w), kde rev(ε) = ε a pro a ∈ Σ a w ∈ Σ* platí rev(a · w) = rev(w) · a. <br />
![image](https://hackmd.io/_uploads/B1b1aXkgGe.png) <br />
![image](https://hackmd.io/_uploads/HJSya7ylGl.png) <br />
![image](https://hackmd.io/_uploads/Hy5kaQkeGe.png) <br />
![image](https://hackmd.io/_uploads/ByRkTQ1lze.png) <br />
![image](https://hackmd.io/_uploads/BkBg67Jgzx.png) <br />
![image](https://hackmd.io/_uploads/r19gTQylGx.png) <br />
![image](https://hackmd.io/_uploads/rkW-6QkeGx.png) <br />
Regulární výrazy popisují jazyky nad abecedou Σ. Základní regulární výrazy jsou ∅ (označuje prázdný jazyk), ε (označuje jazyk {ε}) a a pro a ∈ Σ (označuje jazyk {a}).  <br />
Jsou-li α, β regulární výrazy, pak i (α + β), (α · β) a (α*) jsou regulární výrazy: <br />
(α + β) označuje sjednocení jazyků označených α a β; <br />
(α · β) označuje zřetězení jazyků označených α a β;
(α*) označuje iteraci jazyka označeného α.  <br />
Neexistují žádné další regulární výrazy než ty definované podle těchto dvou bodů.

**Zjednodušený zápis regulárních výrazů:** <br />
Aby byl zápis přehlednější a stručnější, používají se tato pravidla: vynechávají se vnější závorky; vynechávají se závorky zbytečné vzhledem k asociativitě operací sjednocení (+) a zřetězení (·);  <br />
vynechávají se závorky zbytečné vzhledem k prioritě operací – nejvyšší prioritu má iterace (), menší zřetězení (·) a nejmenší sjednocení (+);  <br />
nepíše se tečka pro zřetězení. Příklad: místo (((((0 · 1)) · 1) · (1 · 1)) + (((0 · 0) + 1)*)) píšeme (01)111 + (00 + 1).

Příklady regulárních výrazů (Σ = {a, b}) <br />
a – jazyk tvořený jediným slovem a <br />
ab – jazyk tvořený jediným slovem ab <br />
a + b – jazyk tvořený dvěma slovy a a b <br />
a* – jazyk tvořený slovy ε, a, aa, aaa, … <br />
(ab)* – jazyk tvořený slovy ε, ab, abab, ababab, … <br />
(a + b)* – jazyk tvořený všemi slovy nad abecedou {a, b} <br />
(a + b)*aa – jazyk tvořený všemi slovy končícími aa <br />
(ab)bbb(ab) – jazyk tvořený všemi slovy obsahujícími podslovo bbb předcházené i následované libovolným počtem slov ab <br />
(a + b)*aa + (ab)bbb(ab) – jazyk tvořený všemi slovy, která buď končí aa nebo obsahují podslovo bbb předcházené i následované libovolným počtem slov ab <br />
(a + b)b(a + b) – jazyk tvořený všemi slovy obsahujícími alespoň jeden symbol b <br />
a*(baba)* – jazyk tvořený všemi slovy obsahujícími sudý počet symbolů b <br />
![image](https://hackmd.io/_uploads/H1ed0mylMe.png) <br />
![image](https://hackmd.io/_uploads/r1XuAQJxfg.png) <br />
![image](https://hackmd.io/_uploads/HyP_RX1xMe.png) <br />
![image](https://hackmd.io/_uploads/Sk5uA71efl.png) <br />
![image](https://hackmd.io/_uploads/SkadR71xGx.png) <br />
![image](https://hackmd.io/_uploads/rkfFRQJezg.png) <br />
![image](https://hackmd.io/_uploads/S1UtC71ezl.png) <br />
![image](https://hackmd.io/_uploads/rJKYCm1xGe.png) <br />
![image](https://hackmd.io/_uploads/rJnKRmkgGg.png) <br />
![image](https://hackmd.io/_uploads/rkxc0X1xfx.png) <br />
![image](https://hackmd.io/_uploads/H1lsR71gMx.png) <br />
![image](https://hackmd.io/_uploads/ryGsC7Jeze.png) <br />
![image](https://hackmd.io/_uploads/S1NiRQklfl.png) <br />
![image](https://hackmd.io/_uploads/ryOsAQklzl.png) <br />
![image](https://hackmd.io/_uploads/Hksj071gGg.png) <br />
![image](https://hackmd.io/_uploads/Sk0sCmJeGg.png) <br />
![image](https://hackmd.io/_uploads/rk1hl4JlGl.png) <br />
![image](https://hackmd.io/_uploads/S1z2lEkeGl.png) <br />
![image](https://hackmd.io/_uploads/r1S3lVJlzg.png) <br />
![image](https://hackmd.io/_uploads/ry_2eVJlGx.png) <br />
![image](https://hackmd.io/_uploads/Hyq2lV1eMg.png) <br />
![image](https://hackmd.io/_uploads/SyThe4Jefl.png) <br />
![image](https://hackmd.io/_uploads/SkbTgE1eGx.png) <br />
![image](https://hackmd.io/_uploads/r1X6xE1gMe.png) <br />
![image](https://hackmd.io/_uploads/rkPplVyxMl.png) <br />
![image](https://hackmd.io/_uploads/HyhaeNJefe.png) <br />
![image](https://hackmd.io/_uploads/SJoM-E1gfx.png) <br />
![image](https://hackmd.io/_uploads/rkkmZNJefe.png) <br />
![image](https://hackmd.io/_uploads/r1GXWNJxzl.png) <br />
![image](https://hackmd.io/_uploads/HJr7ZV1gzl.png) <br />
![image](https://hackmd.io/_uploads/r1dm-Ekxfl.png) <br />
![image](https://hackmd.io/_uploads/SJ9mbNylMg.png) <br />
![image](https://hackmd.io/_uploads/SyRQb41xGe.png) <br />
![image](https://hackmd.io/_uploads/H1gE-VklGx.png) <br />
![image](https://hackmd.io/_uploads/B1XNW4JxMe.png) <br />
![image](https://hackmd.io/_uploads/HkjHb4klMl.png) <br />
![image](https://hackmd.io/_uploads/BkXUbEygzx.png) <br />
![image](https://hackmd.io/_uploads/rJ8IbE1xfg.png) <br />
Ekvivalence konečných automatů a regulárních výrazůEkvivalence konečných automatů a regulárních výrazů <br />
Věta: Jazyk je regulární právě tehdy, když je ho možné popsat regulárním výrazem.

#### D. Neregulární jazyky
Ne všechny jazyky jsou regulární – existují jazyky, pro které neexistuje žádný konečný automat, který by je rozpoznával. <br />
Příklady neregulárních jazyků: L₁ = {aⁿbⁿ | n ≥ 0}; L₂ = {ww | w ∈ {a,b}}; <br />
L₃ = {wwᴿ | w ∈ {a,b}}. <br />
Existence neregulárních jazyků vyplývá již z faktu, že automatů pracujících nad nějakou abecedou Σ je jen spočetně mnoho, zatímco jazyků nad abecedou Σ je nespočetně mnoho. Jak dokázat o nějakém jazyce L, že není regulární? Jazyk není regulární, jestliže neexistuje (tj. není možné sestrojit) konečný automat, který by ho rozpoznával. Důkaz neexistence se provádí sporem – předpokládáme, že existuje nějaký automat A rozpoznávající jazyk L, a ukážeme, že tento předpoklad vede k logickému sporu. <br />
![image](https://hackmd.io/_uploads/ByQwbE1xMx.png) <br />
![image](https://hackmd.io/_uploads/rJ_DZEyxzl.png) <br />
![image](https://hackmd.io/_uploads/rJowb4JeGe.png) <br />
![image](https://hackmd.io/_uploads/rkQLmVJgMx.png) <br />
![image](https://hackmd.io/_uploads/HJIL7EJeze.png) <br />
![image](https://hackmd.io/_uploads/SJKLXVJxze.png) <br />
![image](https://hackmd.io/_uploads/r13IX4Jxfg.png) <br />
![image](https://hackmd.io/_uploads/ryyPX41gzl.png) <br />
![image](https://hackmd.io/_uploads/rJfw7Eylzx.png) <br />
![image](https://hackmd.io/_uploads/B1VDmNyefl.png) <br />
![image](https://hackmd.io/_uploads/HJIDQEJlzl.png) <br />
![image](https://hackmd.io/_uploads/rkYD7EklMl.png) <br />
![image](https://hackmd.io/_uploads/S1TwQEklfl.png) <br />
![image](https://hackmd.io/_uploads/SkI_7Nkezg.png) <br />
![image](https://hackmd.io/_uploads/BJud74keGg.png) <br />
![image](https://hackmd.io/_uploads/S19_QN1lMl.png) <br />
![image](https://hackmd.io/_uploads/HkTd7V1eze.png) <br />
![image](https://hackmd.io/_uploads/HklKm4yefl.png) <br />
![image](https://hackmd.io/_uploads/BJfKQVyxGg.png) <br />

##### D.I: Zásobníkové automaty, Turing, výpočetní modely
![image](https://hackmd.io/_uploads/rJm7UE1lGx.png) <br />
![image](https://hackmd.io/_uploads/ryrmUNklfe.png) <br />
![image](https://hackmd.io/_uploads/rJd7I4ylGe.png) <br />
![image](https://hackmd.io/_uploads/B1j7LVJlze.png) <br />
![image](https://hackmd.io/_uploads/ryR78VJeGe.png) <br />
![image](https://hackmd.io/_uploads/H1zV8Vylze.png) <br />
![image](https://hackmd.io/_uploads/r1BVIV1gzg.png) <br />
![image](https://hackmd.io/_uploads/S1dV841lzl.png) <br />
![image](https://hackmd.io/_uploads/HyiV8EylGl.png) <br />
![image](https://hackmd.io/_uploads/SyAV8Nyxfx.png) <br />
![image](https://hackmd.io/_uploads/SJVB8VJxzx.png) <br />
![image](https://hackmd.io/_uploads/S1vS84ylfe.png) <br />
![image](https://hackmd.io/_uploads/HyqHUVJeGg.png) <br />
![image](https://hackmd.io/_uploads/Sk3rIEJlzl.png) <br />
![image](https://hackmd.io/_uploads/BJ-ULVJlfx.png) <br />
![image](https://hackmd.io/_uploads/H1VLUVyxfl.png) <br />
![image](https://hackmd.io/_uploads/BJwI8N1xfl.png) <br />
![image](https://hackmd.io/_uploads/B1cLLVkgfx.png) <br />
![image](https://hackmd.io/_uploads/B1TL8N1lzl.png) <br />
![image](https://hackmd.io/_uploads/r1lDUEygfl.png) <br />
![image](https://hackmd.io/_uploads/Sy9dINJgfe.png) <br />
![image](https://hackmd.io/_uploads/BypOUVJxMg.png) <br />
![image](https://hackmd.io/_uploads/BJxFI4yxGx.png) <br />
![image](https://hackmd.io/_uploads/r1GYIEyeGe.png) <br />
![image](https://hackmd.io/_uploads/SyT9841lGl.png) <br />
![image](https://hackmd.io/_uploads/BJx3UNJxMx.png) <br />
![image](https://hackmd.io/_uploads/BkM3IV1lMl.png) <br />
![image](https://hackmd.io/_uploads/rJrhINJxMg.png) <br />
![image](https://hackmd.io/_uploads/rJDhUVkxMe.png) <br />
![image](https://hackmd.io/_uploads/Sy938N1xze.png) <br />
Turingův stroj — zařízení podobné konečnému automatu s následujícími rozdíly:
* pohyb hlavy oběma směry
* možnost zápisu na pásku na aktuální pozici hlavy
* páska je nekonečná <br />
![image](https://hackmd.io/_uploads/BJuaA4klze.png) <br />
![image](https://hackmd.io/_uploads/HJl0A41gMg.png) <br />
![image](https://hackmd.io/_uploads/Sy7ACVyeMx.png) <br />
![image](https://hackmd.io/_uploads/SkICA41xGg.png) <br />
![image](https://hackmd.io/_uploads/B1tAAEkeGg.png) <br />
![image](https://hackmd.io/_uploads/S12C0E1gzx.png) <br />
![image](https://hackmd.io/_uploads/HJy1JHJlzx.png) <br />
![image](https://hackmd.io/_uploads/ByzJkHJlfg.png) <br />
![image](https://hackmd.io/_uploads/ryryJH1xMx.png) <br />
![image](https://hackmd.io/_uploads/rkw1ySyefx.png) <br />
![image](https://hackmd.io/_uploads/BkglySklMg.png) <br />
![image](https://hackmd.io/_uploads/BJ7eySylze.png) <br />
![image](https://hackmd.io/_uploads/HkLekrJefe.png) <br />
![image](https://hackmd.io/_uploads/SJqxyBJgfe.png) <br />
![image](https://hackmd.io/_uploads/BkpxySJxzg.png) <br />
##### D.II: Chomského hierarch. / Chomsky: <br />
![image](https://hackmd.io/_uploads/SJrWkSygMx.png) <br />
![image](https://hackmd.io/_uploads/Hkub1SJxGl.png) <br />
![image](https://hackmd.io/_uploads/SyibkrJgGg.png) <br />
![image](https://hackmd.io/_uploads/SJ6-1HyeMg.png) <br />
![image](https://hackmd.io/_uploads/B1xGkHylGx.png) <br />
![image](https://hackmd.io/_uploads/SkNfJB1xGl.png) <br />
![image](https://hackmd.io/_uploads/r1vM1r1gGx.png) <br />
![image](https://hackmd.io/_uploads/S15MJHkgzx.png) <br />
![image](https://hackmd.io/_uploads/SyAz1H1xfe.png) <br />
![image](https://hackmd.io/_uploads/rJZ7ySJxMg.png) <br />
![image](https://hackmd.io/_uploads/SJM3JHkgMl.png) <br />
![image](https://hackmd.io/_uploads/HkHnyBkgMx.png) <br />
![image](https://hackmd.io/_uploads/BJg-bS1eGg.png) <br />
![image](https://hackmd.io/_uploads/S1zZZB1lzl.png) <br />
![image](https://hackmd.io/_uploads/B1UW-r1lzx.png) <br />
![image](https://hackmd.io/_uploads/HyfBZrygzl.png) <br />
![image](https://hackmd.io/_uploads/HkFSZSkezx.png) <br />
![image](https://hackmd.io/_uploads/SkTHbHylGg.png) <br />
![image](https://hackmd.io/_uploads/rJy8WB1xfl.png) <br />
![image](https://hackmd.io/_uploads/HJGIZHygMx.png) <br />
![image](https://hackmd.io/_uploads/Hy48bHkxGg.png) <br />
![image](https://hackmd.io/_uploads/r1vLbSJxze.png) <br />
![image](https://hackmd.io/_uploads/BkIwWS1gfl.png) <br />
![image](https://hackmd.io/_uploads/Bk9P-r1efe.png) <br />
![image](https://hackmd.io/_uploads/ry6v-Byezg.png) <br />
![image](https://hackmd.io/_uploads/BJld-rkezg.png) <br />
![image](https://hackmd.io/_uploads/Hy7_WSJxMl.png) <br />
Vidíme, že činnost libovolného Turingova stroje je možné simulovat Minského strojem s dvěma čítači. Vidíme, že činnost libovolného Turingova stroje je možné simulovat Minského strojem s dvěma čítači. Tato simulace je však mimořádně neefektivní: už simulace pásky Turingova stroje pomocí tří čítačů vyžaduje exponenciálně větší počet kroků, než kolik by jich vykonal tento Turingův stroj. Simulace činnosti těchto tří čítačů pomocí dvou čítačů tento počet kroků dále exponenciálně zvyšuje. <br />
![image](https://hackmd.io/_uploads/SkM5-SkeMx.png) <br />
![image](https://hackmd.io/_uploads/rkB5-H1lMx.png) <br />
![image](https://hackmd.io/_uploads/BytqZSyxGx.png) <br />
![image](https://hackmd.io/_uploads/B1n9bBylfx.png) <br />
![image](https://hackmd.io/_uploads/r1R5bSkgzg.png) <br />
![image](https://hackmd.io/_uploads/HkUoWryefl.png) <br />
![image](https://hackmd.io/_uploads/H1ui-rJezl.png) <br />
![image](https://hackmd.io/_uploads/rkoiWrylze.png) <br />
![image](https://hackmd.io/_uploads/B10sWSyxfe.png) <br />
![image](https://hackmd.io/_uploads/rkfh-B1xfl.png) <br />

[Množiny skok](#####MNOZINY) <br />
[Relace skok](#####RELACE) <br />
[Kongruence a modulo skok](#####KONGRUENCE) <br />
WIP nekde skok na grafy a na algoritmy <br />
[Paměti HW se zásobníkem](#####HW_PAMET) <br />
WIP skok na programko zasobnik <br />

### 3.1) UTI ultimate Aplikace matematicko-logických záležitostí:
#### A. LA
##### A.I: Čistě geometricky:
* Osová, středová souměrnost - čára mezi dvěma body prochází originem, který je ve středu oné čáry NEBO přímka (osa) a k ní kolmá čára spojující zase dva body, střed té čáry na ose
* Rotace, posun - po směru hod. ručiček negativní smysl, orientovaný angle xSx' roven anglu jakým jsme otočili
* Soulehlost - nějaký násobek k
Hraje roli S jako střed rovno tomu transformovanému, akorát v posunu je S nějaký vektor, sčítání matic a všude jinde násobení. <br />

-1 0 <br />
0 -1 <br />
střed. <br />

1 0 <br />
0 -1 <br />
os. <br />

cos -sin <br />
sin cos <br />

2 0 <br />
0 2 <br />

## Praktická část
Zde budou zpětné linky na matiku / logiku pro případ nouze, kdy žáček zapomene, o co vlastně šlo.

### 1.1) APPS, OSY, ZDS
##### OBVODY_TRANZISTORY
#### A. Ciselne obvody a bool.
[Skok rovnou na V/V brány spojené s pravdivostními hodnotami](#####OBVODY_TRANZISTORY) <br />
* Hybridní - pasivní a aktivní součástky připevněné v jedné nosné destičce, vzájemně propojené a zapouzdřené. Pro cislo na analog nebo naopak prevody.
* Monolitické - potřebné prvky na destičce POLOVODICE nejbezneji z kremiku, ale jinak taky passive a active propojení. Pro elektronicke cislicove systemy. <br />
Dal se venujeme monolitum...

Podle stupne integrace:
* SSI - small scale int. do 3O prvku
* MSI - middle scale int. do 1000
* LSI - large scale int. do 100 000
* VLSI - very large scale int. do 10 mil
* ULSI - ultra scale int. do miliardy
* GSI - gigantic scale int. nad miliardu

##### A.I: Bipolár:
Bipolarni technologie vyuzivaji bipolarni tranzistory, a az na nektere vyjimky jsou rychlejsi nez unipolar. Nedosahuji tak velkeho stupne integrace, vetsi spotreba, ale levnejsi. Rychle k bipolar. tranz... conductuje i elektrony, tak diry (nosiče nábojů), zatimco unipolar jen jedno nebo druhe. Bipolar ma kolektor, emitor a bazi jako elektrody.

**DTL:** <br />
Vstupni diody D1, D2, ..., rezistory a na konci tranzistor, muzeme mit i posouvaci diody. muzeme realizovat napr. NAND, kde vstupni diody s rezistorem pracuji jako diodovy logicky soucin. alespon jedna 0 na vstupu znamena to, ze mezi diodama D1 a D2 nastane nulovy potencial a tranzistor zapojeny jako invertor se uzavre, coz znamena ze na vystupu bude 1. posuvne diody zajistuji plne uzavreni a sumovou imunitu, protoze zvedaji napeti nutne pro otevreni tranzistoru, s otevrenym tranzistorem mame hodnotu na konci logicke nuly.

**TTL:** <br />
Tranzistorove obvody s tranzis. logikou, neboli tvorba tranzistoru s vice nasobnym emitorem. na vstupu tranzistor, kde prechod z baze na emitor muzeme nahradit DTL soucinovym hradlem, baze na konektor s posouvacima diodama. <br />
![image](https://hackmd.io/_uploads/HJPJ_83kMx.png) <br />
Výstup se dobře chová při kapacitní zátěžo a nízká výstupní imedance je vhodná i díky tomu, že parazitní signály pak nemají takový vliv na činnost obvodu, přednost oproti DTL, kde výstupní impedance je v době uzavření tranz. na výstupu obvodu určena jeho kolektorovým odporem. Avšak tyto obvody nepoužijeme v kaskádě bez oddělení, bo se mezi sebou ovlivní, pro paralelní propojení existuje obvod s otevřeným kolektorem na výstupu logického členu, tj. chybí z této strany na tom tranzistoru vnitřní pull-up rezistor, který se pak připájí jako diskrétní rezistor, což z tohoto dělá montážní obvod. Dobrá šumivá imunita a odolné proti static elect. <br />
Varianty LTTL A HTTL jako low and high speed.

**STTL:** <br />
TTL, ale lepší poměr rychlost k příkonu, bo spínací rychlost je vyšší s využití Schottkyho diody. Protože je na diodě v propustném směru podstatně menší napětí než na přechodu mezi kolektorem a bází tranzistoru, paralelním připojením Schott-kyho diody k tomuto přechodu se zabrání nasycení tranzistoru a tím se sníží doba jeho zpoždění a příkon je dvojnásobný. <br />
Další varianty LSTTL, ASTTL, ALSTTL jako advanced low STTL.

Funkční vlastnosti jednotlivých variant technologie TTL jsou stejné,
proto jsou také všechny technologie slučitelné. Obvody se však liší především svojí rychlostí a spotřebou. Stupen integrace do 500.

**IIL:** <br />
Velmi rychlé s malým příkonem s velkou hustotou integrace. např. invertor obvod, kde PNP tranzistor jako injektor tvoří konstantní proud, bez ohledu na druh signálu je na vstupu vždy zápornější báze, než emitor a tranzistor zustava otevren. Je-li na vstupu nulový potenciál (logická 0), prochází injekční proud směrem k tomuto vstupu a tranzistor T2 s vícenásobným kolektorem je uzavřený. Při kladném potenciálu (logická 1) na vstupu, prochází injekční proud směrem do báze tranzistoru s vícenásobným kolektorem, ten se otevře a vytváří na výstupu úroveň logické 0.  <br />
S izolací se jedná o IIIL, ve sloučení s TTL pro výrobu velkokapacitní RWM a mikroprocesory.

**ECL:** <br />
Neboli emitor coupled logic: emitorová vazba tak, at nemuze dojit k nasycenim na bazi nejakeho tranzistoru T3 stabilni referencni napeti, aby se nesnizila sumiva imunita obvodu. T1 a T2 pracuji na principu spinani proudu, proto oznaceni current mode logic, na ne se mohou pripojit dalsi tranzistory paralelne. Je-li na všech vstupech tranzistorů T1 a T2 úroveň logické 0, na výstupu se objeví úroveň logické 1. Je-li alespoň jeden ze vstupů na úrovni logické 1 na výstupu se objeví úroveň logické 0. Zapojení tedy představuje funkci NOR. Pro dosažení malého výstupního odporu bývá na výstupu často připojen emitorový sledovač T4. ECL mají malou šumovou imunitu a nejsou přímo slučitelné s TTL obvody.

##### A.II: Unipolár:
Vysoká integrace pro PCs. Známe je spíš jako field effected tranzistor neboli FET. Princip je že hloubka vniku elektrického pole do látky je uměrná převrácené konduktivitě, i.e. s menší konduktivitou látky do ní líp vnikne elektrické pole. Izolanty ale nemají vubec elek. proud, takže nevhodné pro aplikaci. Vhodný je dotovaný polovodič s malinkou kondukt. a s trošku proudem, aby to pole, co vstoupí, mohlo tento proud ovlivnit. <br />
Podle toho, jak je tato proudová dráha (kanál) dotovaná, tak máme tranzistor řízen kanálem N nebo P. Elektrické pole pusobi na proudovy kanal bud pres závěrnou vrstvu přechodu nebo přes zvláštní izolační vrstvu... vyplývá FET s přechodovým hradlem, neboli JFET jako junction FET, případně IGFET jako isolated gate FET, ten se ještě rozděluje na ochuzovací nebo obohacovací typ.. <br />
FET má tři elektrody source jako emitor, drain jako kolektor a gate jako hradlo. Podle toho, která elektroda se používá společně pro vstup a výstup, mluvíme o zapojení se společným emitorem, kolektorem a hradlem. Nejobvyklejším je zapojení se společným emitorem. IGFET využívá izolační vrstvu oxidu, čiže vznikne MOSFET jako metal oxide semiconductor FET, pro číslicové obody jeho obohacovací typ.

**MOSFET:** <br />
MOSFET s obohaceným kanálem P, ale může být i N (na konci odstavce), vytváří a rozšiřuje vodivý kanál mezi emitorem a kolektorem vlivem příčného elektrického pole vyvoláno přivedením napětí na hradlo G. Vysoký výstupní odpor, málá spotřeba a odolnost proti rušení + výborné spínací vlastnosti. Činnost obohacovacího typu MOSFETu s kanálem N je analogická s tím, že polarity proudů a napětí budou opačné (kladné) a šipka ve schematické značce bude mít opačný směr.

**PMOS:** <br />
Postive metal oxid semicond., kde základ je MOS s kanálem P. Obvod univerzálního logického členu, kde se spojí nějaká spojka K1 se zemí a v obvodu dál stojí 3 tranzistory v sérii a na výstupu Y je hodnota logické 0 jen tehdy, kdy všechny 3 tranz. jsouv vybuzeny, tj. vznikne NAND. NOR vznikne vybuzením jednoho z těch tranzistů, když K1 a K3 se zemí a K2 spojená s Y.  <br />
Díky tomu, že jsou tranzistory řízeny elektrickým polem a nikoliv elektrickým proudem jako u technologie TTL, jsou u nich značně redukovány nároky na spotřebu elektrické energie. Neslučitelné s TTL kvůli napájecímu napětí, takže využito jen u první generace mikroproc. NMOS je s kanálem N, třikrát rychlejší s víc pohyblivými nosičy - RWM a ROM využiití, bo funguje s TTL. <br />
![image](https://hackmd.io/_uploads/HJC5rP31zx.png) <br />

**HMOS:** <br />
Součin zpoždění a ztrátového výkonu (který obecně charakterizuje integrovaný obvod) je přibližně úměrný třetí mocnině rozměru základní struktury. Při zvyšování rychlosti, má však zmenšování rozměrů hradla i vedlejší nepříznivé efekty, jako zvyšování intenzity elektrického pole při stejném napájecím napětí, pronikání elektronů do řídící elektrody, podpovrchové průrazy atd. U HMOSII a HMOSIII se řešily problémy tím, že se parametry upravují s jiným faktorem, získaným optimalizačními výpočty.  <br />
Technologie HMOS i její vylepšené varianty se uplatňují při výrobě monolitických mikroprocesorů s desítkama tisíc až půl milionem tranzistorů na čipu a také pro výrobu moderních pamětí RWM–RAM.

**CMOS:** <br />
Complementary MOS, využívá NMOS a PMOS obohacovacího typu, střídají se ve funkci řízeného zatěžovacího rezistoru MOS a spínacího tranzistoru. Invertor kde je vstup X, výstup Y mezi PMOS a NMOS, NMOS k zemi, PMOS napětí E v default schema.  <br />
Při signálu logické 1 na vstupu X (kladná logika) je vodivý (zapnutý) tranzistor NMOS a tranzistor PMOS je vypnutý. Na výstupu Y je logická 0. Při úrovni logické 0 na vstupu X je tranzistor PMOS zapnutý (vodivý) a tranzistor NMOS je vypnutý. Na výstupu Y je úroveň logické 1.  <br />
Extrémně nízká příkon a dobrá šumivá imunita, slučitelné s TTL a široké rozmezí napájecího napětí + velký rozsah pracovních teplot a velký logický zisk. Výroba monolitických mikroprocesorů i pamětí a dalších prvků obvodů LSI, VLSI, ULSI. Tedy, tranzistory fungují jako spínače, které přepínají výstup buď na napájecí napětí E nebo k zemi. Takže pokud nezatěžujeme výstup takového obvodu, je jeho spotřeba v klidovém stavu prakticky nulová. Výstup obvodu má relativně malou impedanci v obou stavech (řádově stovky ohmů).

**SOI a SOS:** <br />
Silicon on sapphire, kde základ čipu je destička syntetického safíru. Podložka zmenší parazitní kapacitu až 3x a potlačí parazitní vazby a dosáhne vysokých spíánacích rychlostí porovnatelné s parametry bipolárních obvodů, hustota 4x větší než u CMOS. Mikroproc. a RWM. Safír je ale expensive, takže SOI neboli silicon on insulator využívá křemíkovou destičku jako izolant, konkrétně oxid křemičitý (SiO2), kde se tvoří ostrůvky polovodič. struktur, dobrý izolant.

**FAMOS a FLOTOX:** <br />
Pro EPROM technika plovoucího hradla s lavinovou injekcí nosičů - FAMOS (Floating–gate Avalanche–injection MOS), základem paměťové buňky tranzistor MOS s řídící elektrodou (hradlem z polykristalického křemíku), která není k ničemu připojena, neboť je ze všech stran izolována oxidem křemičitým. Při mazání informace z pamětí se působí na čip ultrafialovým ionizujícím zářením.

Elektrony v ozářené řídící elektrodě absorbují fotony záření a získávají dostatečnou energii k překonání bariéry v opačném směru. Potenciály hradla a emitoru se tak vyrovnávají, zruší (vymaže) se obsah paměti FAMOS a tranzistor FAMOS se uvede do původního vypnutého (nevodivého) stavu. Tím je paměť opět připravena k dalšímu programování. Při každém mazání informace ozářením dochází k mírné degradaci parametrů paměťové buňky FAMOS. Pokud však je mazání šetrné (např. studeným utrafialovým zářením), nevybočí parametry pamětí EPROM z tolerancíani po několika desítkách cyklů mazaní–programování.

FLOating gate Tunnel OXide cell je modifací FAMOS pro tvorbu paměťových buněk mikroelektronických vymazatelných a programovatelných pevných pamětí EEPROM (Electrically Erasable and Programmable ROM). Při dalším rozvoji této technologie se uplatňují stejné myšlenky zjemňování struktury čipů, jako u přechodu od klasické technologie NMOS k technologii HMOS. Výsledkem je technologie HMOS–E pro výrobu pamětí EPROM a EEPROM.

**CCD a BiCMOS:** <br />
CCD a BiCMOS: Charge couled devices, není typická zesilovací činnost základních obvodových členů, ale přenos náboje na parazitních kapacitách soustavou elektrod vytvořených na strukturách MOS. Na tomto principu se vytvářejí posuvné registry, ale sekvenční paměti z nich vyrobené nejsou energeticky nezávislé, proto se v mikropočítačové technice neuplatňují.  <br />
Součástky CCD mají rozsáhlejší použití v analogové technice jako paměti ve snímačích obrazu pro televizi a v monolitických plochých displejích, kde jsou zviditelněny jejich výhody, jako je malá spotřeba energie a malé rozměry. U technologie BiCMOS se kombinuje vysoká hustota integrace technolgie CMOS s dobrými vlastnostmi v řízení proudu bipolárních technologií. <br />
![image](https://hackmd.io/_uploads/HyMnHd31fl.png) <br />
![image](https://hackmd.io/_uploads/BJB3Bd3kfx.png) <br />

TODO proč jsou dobré některé elektrické vlastnosti a u čeho, tabulka? co se z čeho vyrábí nebo vyrábělo

TODO boolean
##### A.III: Boolean algebra:
##### BOOLEAN
[Logika jump](#####LOGIKA_START) <br />

#### B. Paměti
##### HW_PAMET
Nejdřív ferit pamět na principu zmagnetiz. ferit. jader. Pak bubnové paměti kdy magnetický materiál nanesen na magnetický buben otáčející se vysokou rychlostí. Poté bublinové paměti založeny na velkokapacitních posůvných registrech. Pak polovodičové paměti popsané v subkapitole nad touto, konkrétně MOS. Pak DRAM a SRAM, tedy dynamic a static paměti.

RAM - paměti s libovolným přístupem, SAM se sériovým, nakonec paměti se speciálními zpusoby pristupu jako asociativni pamet, pamet fronta / zasobnik, vice branove pameti a pameti s kombinovanym rizenim.

[RAM a zásobník z pohledu UTI](#####UTI_MODELY_AUTOMATY) <br />
[RAM a zásobník z pohledu programka](#####N/A) <br />
WIP skok z programka sem na paměti <br />

RWM je read write mem a ROM read only.  <br />
NVRAM jako non volatile RAM je kombinace RWM a EEPROM. WOM je write only zatímco WORM write once read many times, aka CD ROM.  <br />
PROM, EPROM, EEPROM, FLASH - programovatelné paměti.  <br />
Non Volatile se označují ty paměti, které informaci uchovávání i po odpojení napájení, jako jsou různé typy pamětí xxROM. <br />
Volatile - paměti ztrácející uloženou informaci po odpojení napájení, jako jsou paměti DRAM a SRAM. Otázkou může v této chvíli být, kam zařadit hlavní paměť počítače, které se hovorově říká „ramka“. Z uvedeného dělení pamětí je zřejmé, že toto označení je neúplné a tedy nepřesné.  <br />
Hlavní paměť počítače je určena pro čtení a zápis, musí umožňovat náhodný přístup a informace je uložena v kondenzátoru a po odpojení napájení se uložené informace ztratí. Úplné označení by tedy dle předchozího dělení být Volatile RWM DRAM.

##### B.I: Dynamic memory
V dynamických pamětech je informace uložena ve formě náboje v kondenzátoru. Kondenzátor může být buď nabitý (logická 1) nebo vybitý (logická 0). Např. dvě jednotranzistorové paměťové buňky dynamické paměti.  <br />
Jelikož kondenzátory jsou extrémně miniaturní, jsou to jen parazitní kapacity na tranzistotu, jejich kapacita je velmi malá - jednotky až desítky fF (femtoFarad). Kondenzátor si tak není schopen zachovat uloženou informaci po neomezenou dobu, i velmi malý proud tekoucí do nebo z tohoto kondenzátoru, vyvolá velké změny jeho napětí v krátkém čase. Je proto nutné často obnovovat napětí kondenzátoru - tato procedura je označovaná jako občerstvení neboli refresh.  <br />
Pro tento proces jsou dnes na čipu implementovány speciální obvody, těm stačí pouze pravidelně přečíst libovolnou buňku z každé řady a následovně bude občerstvena celá tato řada. <br />
![image](https://hackmd.io/_uploads/BkQluu3JGl.png) <br />
... signály RAS a CAS. <br />

![image](https://hackmd.io/_uploads/rysLdd2Jzx.png) <br />
![image](https://hackmd.io/_uploads/S1f_OuhJfe.png) <br />
![image](https://hackmd.io/_uploads/SJqKduhyzl.png) <br />
![image](https://hackmd.io/_uploads/B1i_OOnkfe.png) <br />
Minulá sekce popisovala normální mód DRAM. Paměťové čipy mohou také schopné vykonávat jeden nebo více jiných sloupcových módů pro snížení přístupové doby. Ten nejznámější je stránkový mód (Page Mode). Čtení a zápis dat, se zmiňuje, že v průběhu přístupu do paměťové buňky je nejprve zadána adresa řádku s aktivním RAS signálem a potom adresa sloupce s aktivním CAS signálem. Pokud se další přístup do paměti vztahuje na stejný řádek a pouze jiný sloupec (to znamená, že adresa řádku zůstala stejná a jen adresa sloupce je změněna), není nutné vkládat a dekódovat znovu adresu řádku (ve stránkovém módu je změněna pouze adresa sloupce, ale adresa řádku zůstala zachována). Takže jedna stránka koresponduje právě s jedním řádkem v poli.

Během stránkového módu při přístupu do paměťové buňky ve stejném řádku paměťový kontrolér nedeaktivuje RAS signál. Pouze CAS signál je deaktivován na krátkou dobu a poté znovu aktivován. Všechny přístupové tranzistory připojené na adresovém vodiči adresovaného řádku proto zůstanou sepnuty a všechna přečtená data jsou na konci datových vodičů. Nová adresa sloupce je dekódována v dekodéru sloupce. Ve stránkovém módu je přístupová doba o 50% (a doba cyklu až o 70%) kratší, než v normálním módu. Toto samozřejmě platí pro druhý i každý další přístup. <br />
![image](https://hackmd.io/_uploads/H14_td2yfx.png) <br />
SDRAM znamená synchronní DRAM, což by se nemělo zaměňovat s SRAM (statické RAM). V praxi není rozdíl mezi SDRAM a EDO DRAM podstatný. Jeden z důvodů je paměť L2 cache, která zvedá výkon slabších EDO čipů o nějaký stupeň. Při porovnání s EDO DRAM je patrný větší výkon pamětí SDRAM pokud je systémová taktovací frekvence větší než 100 MHz, což je případ drtivé většiny dnešních systémů. SDRAM pracují v burst módu a se synchronní taktovací frekvencí, ne s různým RAS a CAS časováním jak tomu je u jiných RAM čipů. SDRAM také používají odpovídající signály RAS, CAS, WE a CE, ale používají je k přesunutí příkazů jako zápis, čtení a burst stop. Signály RAS a CAS jsou zkombinovány pro vytvoření příkazové sběrnice. SDRAM používá principu podobnému prokládání paměťových polí tak, že zatímco s jedním pracuje (je z něj čteno), druhé se připravuje na následující přístup.

Přenosová rychlost dat může být zdvojnásobena, pokud jsou data přenášena nejen na náběžné hraně hodinového pulsu, ale také na sestupné hraně hodinového pulsu. Přesně tento princip používají paměti double data rate DRAM (DDR-RAM). <br />
![image](https://hackmd.io/_uploads/r11lqu21fe.png) <br />
![image](https://hackmd.io/_uploads/rkUl9uhJfx.png) <br />
![image](https://hackmd.io/_uploads/S1Tec_3Jfl.png) <br />

##### B.I: Static memory
![image](https://hackmd.io/_uploads/HkzN5_3JMl.png) <br />
![image](https://hackmd.io/_uploads/SyO4qu3kGl.png) <br />
![image](https://hackmd.io/_uploads/BJp4cunyzl.png) <br />
![image](https://hackmd.io/_uploads/HyKucunkzg.png) <br />

![image](https://hackmd.io/_uploads/SJec9uhyfl.png) <br />
![image](https://hackmd.io/_uploads/rk8ccd2yMl.png) <br />
... do RAM paměti a vymazat ho z flash paměti. V RAM paměti se “1” zapíše do daného řádku a ten se potom celý zapíše zpět do flash paměti na jeho
původní místo. <br />

![image](https://hackmd.io/_uploads/HyFsqd3kfe.png) <br />
![image](https://hackmd.io/_uploads/HJ2TcuhkMe.png) <br />
... z určité adresy informaci, přečte zároveň informace i z následujících adres (což by pravděpodobně dělal za chvíli). <br />

![image](https://hackmd.io/_uploads/B1TfiO2yzg.png) <br />
![image](https://hackmd.io/_uploads/HyH7j_2JMg.png) <br />
![image](https://hackmd.io/_uploads/BJjXju3Jfx.png) <br />

[Start pamětí](#####HW_PAMET) <br />
WIP skok na struktury jako fronta programko <br />

##### B.II: Chyby paměti, parita, kontroly a EEC paměti
DRAM paměti jsou náchylné k paměťovým chybám, protože ukládají data jako náboje v malých kondenzátorech, které musí být neustále obnovované. Existují dva typy chyb: opakující se (tvrdé) chyby, kdy hardware trvale vrací špatné výsledky, a přechodné (měkké) chyby, kdy se bit přečte špatně jen jednou a poté funguje správně.

Měkká chyba se může opakovat v rozsahu od minut po několik let. Fyzická parita ukládá paritní bity do paměťového modulu během zápisu; logická parita je generuje až při čtení, takže paritní informace modulu nejsou relevantní. Moduly s logickou paritou ušetří více než 10 % (4 až 36 bitů) kapacity a jsou levnější. Běžná paměť bez parity používá přesně 8 bitů na byte. Paměť s paritou přidává 1 bit na každých 8 bitů dat – celkem tedy 9 bitů na byte – výhradně pro detekci chyb. Generátor/kontrolér parity při zápisu spočítá počet jedniček v bytu a nastaví 9. bit tak, aby celkový počet jedniček byl vždy lichý (lichá parita).

Při čtení obvod znovu spočítá jedničky; sudý počet signalizuje chybu. Systém detekuje chybu, ale neví, ve kterém bitu nastala. Paritní chyba vyvolá nemaskovatelné přerušení (NMI). 

Parita nedokáže detekovat chyby ve dvou bitech současně – pokud se prohodí dva bity, počet jedniček zůstane lichý a chyba zůstane neodhalena. ECC (Error Correction Code) detekuje jednobitové i vícebitové chyby a navíc dokáže jednobitové chyby během čtení opravit. Místo jednoho paritního bitu na 8 bitů dat používá ECC skupiny bitů:  <br />
7 bitů pro ochranu 32 bitů dat, nebo 8 bitů pro ochranu 64 bitů dat.  <br />
ECC dokáže detekovat chyby 2, 3 i 4 bitů, opravit však umí pouze jednobitové. Vícebitové chyby řeší stejně jako parita – pomocí NMI. ECC způsobuje zpomalení systémových operací přibližně o 2–3 %, protože algoritmus vyžaduje jeden dodatečný čekací stav při čtení z paměti.

##### B.III: Externí paměti / disky
Pevný disk RAMAC, pak první uzavřená disková jednotka s přímo integrovanou čtecí hlavou - disky, poté diskety... první pružný disk, dále mechanika, dále větší mechanika a větší diskety... CD-ROM přišly se specifikací standardu Red Book, pak první CD-R mechanika, pak standard Yellow Book s možností ukládat poč. data a první CD-RW mechanika... DVD nakonec.

* Magnetické paměti, tj. pevný disk a diskety
* Optické paměti, tj. CD a DVD
* Magneto-optické <br />
![image](https://hackmd.io/_uploads/rJEHVF2yzg.png) <br />
Pevný disk je uzavřená jednotka v počítači, používaná pro trvalé ukládání dat (tzv. data zůstanou na disku zachována i po vypnutí napájení počítače). Pouzdro chrání disk před nečistotami a poškozením. Pevný disk obsahuje pevné plotny diskového tvaru, které jsou většinou vyrobeny ze slitiny hliníku nebo skla. Plotny na rozdíl od disket nelze ohýbat, proto termín pevný disk. Ve většině případů platí, že plotny nelze vyjmout. Z těchto důvodů se někdy používá termín pevná disková mechanika (fixed disk drive) nebo hard disk drive HDD.

Casti pevneho disku: <br />
* plotny + pohon
* hlavy pro read a write + pohon
* vzduchové filtry
* řídící deska s elektronikou
* kabely a konektory <br />
![image](https://hackmd.io/_uploads/HJWiEK2Jzg.png) <br />
![image](https://hackmd.io/_uploads/r1ij4KhJfx.png) <br />
![image](https://hackmd.io/_uploads/HJbh4Khkzx.png) <br />

Casi disketovych mechanik: <br />
* hlavy pro read a write + pohon
* pohon pro mechaniku
* řídící deska
* řadič
* konektory

![image](https://hackmd.io/_uploads/r1UeHY2yMx.png) <br />
![image](https://hackmd.io/_uploads/Hy0erY3Jze.png) <br />
![image](https://hackmd.io/_uploads/H1N-HFhkfg.png) <br />
![image](https://hackmd.io/_uploads/rJ9-SYnJzg.png) <br />
![image](https://hackmd.io/_uploads/HkvGrKhJfl.png) <br />

Casi mechaniky CD-ROM: <br />
* laserová neboli optická hlava
* fotodetektor
* servomechanismus
* ovládací čip
* vyrovnávací pamět
* elektronika pro dekodovani signalu a rizeni procesu

![image](https://hackmd.io/_uploads/BJavBF31Gg.png) <br />
![image](https://hackmd.io/_uploads/SJgW_HFn1fl.png) <br />
![image](https://hackmd.io/_uploads/rJvdSKhJze.png) <br />
![image](https://hackmd.io/_uploads/SyUFBF3yfg.png) <br />

WIP skok na OSY <br />

![image](https://hackmd.io/_uploads/H1I43O31Ml.png) <br />
![image](https://hackmd.io/_uploads/BJs42_2kze.png) <br />
![image](https://hackmd.io/_uploads/rkQBn_2JMe.png) <br />
![image](https://hackmd.io/_uploads/ByKBh_2yzl.png) <br />
![image](https://hackmd.io/_uploads/ByyIhu31fg.png) <br />
![image](https://hackmd.io/_uploads/rkN8ndh1zx.png) <br />
![image](https://hackmd.io/_uploads/BJ5Lhd3yMg.png) <br />
![image](https://hackmd.io/_uploads/rklPhOn1Gx.png) <br />
[Skok na obvody a tranzistory](#####OBVODY_TRANZISTORY) <br />
##### V/V brány
![image](https://hackmd.io/_uploads/H1_u2uhkMx.png) <br />
![image](https://hackmd.io/_uploads/HJZt2_3yGg.png) <br />
![image](https://hackmd.io/_uploads/Sk5Y2Ohyfg.png) <br />
![image](https://hackmd.io/_uploads/SkJcnOh1Gl.png) <br />
![image](https://hackmd.io/_uploads/SJrc3_21Me.png) <br />
![image](https://hackmd.io/_uploads/SJ252un1zl.png) <br />
![image](https://hackmd.io/_uploads/rybihunyMe.png) <br />
![image](https://hackmd.io/_uploads/BkPo2O3kMe.png) <br />
![image](https://hackmd.io/_uploads/Hkqshu31zg.png) <br />
![image](https://hackmd.io/_uploads/rySnhunJMx.png) <br />
![image](https://hackmd.io/_uploads/HJF2nO3kGx.png) <br />
![image](https://hackmd.io/_uploads/ryypnd3kzl.png) <br />
![image](https://hackmd.io/_uploads/rJd62dhkMg.png) <br />
![image](https://hackmd.io/_uploads/Hy0pnO3JGe.png) <br />
Monolity jsou celé zkopčené poliho skripta, bo si nejsem jistý, zda je worth z toho dělat výtah, might do it later.

#### C. Procesory RISC a CISC
Konečně nadstavba done. Jdem na jednu z kapitol of all time. <br />
* CISC - počítač se složitým souborem instrukcí (Complex Instruction Set Computer)
* RISC - počítač s redukovaným souborem instrukcí (Reduced Instruction Set Computer)
Není to dnes upe black and white, spíš mix rysů. CISC nebyl složitostně pak viable v rámci vývoje, a tak se objevily první pokusy o celkové zjednodušení struktury procesorů. Vznikla tak zcela nová kategorie procesorů, dnes označovaná jako RISC. <br />
![image](https://hackmd.io/_uploads/BJf0pu3JMg.png) <br />
![image](https://hackmd.io/_uploads/r1_Cpdhyfe.png) <br />
Bezesporu nejtypičtější vlastností charakterizující počítače RISC je malý instrukční soubor. Pro tuto vývojovou větev procesorů si ale vývojáři stanovili celou řadu dalších vcelku zásadních kritérií, charakterizujících metodiku návrhu nejen procesoru, ale celého počítače. Procesoru je třeba přenecha jen tu činnost, která je nezbytně nutná a přenést další potřebné funkce do architektury počítače, programového vybavení a kompilátoru.

WIP skok na kompilátory <br />

Výsledkem návrhu konstrukce procesoru RISC jsou zejména tyto vlastnosti: <br />
* V každém strojovém cyklu by měla být dokončena jedna instrukce (pozor, to neznamená, že její vykonání trvalo jeden stroj. cyklus)
* Mikroprogramový řadič může být nahrazen rychlejším obvodovým řadičem
* Používat zřetězené zpracování instrukcí
* Celkový počet instrukcí a způsobů adresování je malý
* Data jsou z hlavní paměti vybírána a následně ukládána výhradně jen pomocí dvou instrukcí LOAD a STORE
* Instrukce mají pevnou délku a jednotný formát, který vymezuje význam jednotlivých bitů
* Je použit vyšší počet registrů
* Složitost se z technického vybavení přesouvá částečně do optimalizujícího kompilátoru

Všechny uvedené vlastnosti tvoří dobře promyšlený a provázaný celek.
Např. navýšení počtu registrů souvisí s omezením komunikace s pamětí na dvě instrukce LOAD a STORE. Pokud ostatní instrukce nemohou používat paměťové operandy, je třeba mít v procesoru uloženo více dat.

Další souvislost je patrná mezi zřetězeným zpracováním a formátem instrukcí. Jednotná délka instrukcí dovoluje rychlejší výběr instrukcí z paměti a tím zajišťuje lepší plnění fronty instrukcí (viz další kapitola). Jednotný formát pak zjednodušuje dekódování instrukcí.

Výsledné počítače vytvořené podle těchto pravidel přinášejí výhody jak pro uživatele, tak i pro výrobce. Zkracuje se vývoj procesoru a zpravidla již první realizované čipy fungují správně.

Architektura RISC má i své nedostatky, přesto se většina výrobců CISC procesorů uchýlila při výrobě procesorů k realizaci stále většího počtu vlastností architektury RISC. Mezi nevýhody RICS architektury patří třeba nutný nárůst délky programů, tvořených omezeným počtem instrukcí a také díky jednotné délce všech instrukcí. Zpomalení, které by z toho mělo nutně plynout, se ale v praxi nepotvrdilo. Je třeba si uvědomit, jak malé procento instrukcí muselo být rozepsáno a zřetězené zpracování instrukcí zásadním způsobem urychluje práci procesoru.

![image](https://hackmd.io/_uploads/B1_lJYnkGg.png) <br />
[Paměti HW zase](#####HW_PAMET) <br />
![image](https://hackmd.io/_uploads/ry-mJthkzg.png) <br />
![image](https://hackmd.io/_uploads/SJOXytnJMl.png) <br />
Zřetězené zpracování instrukcí přináší nejen výrazné navýšení výkonu procesoru, ale nese s sebou i řadu nástrah, úskalí a problémů. Mezi hlavní problémy, které budou dále popsány, patří hazardy datové i strukturální a problémy s plněním fronty instrukcí.

Datový hazard nastává, když rozpracovaná instrukce potřebuje data, která ještě nebyla uložena předchozí instrukcí. Řešením je buď specializovaná konstrukce zřetězené jednotky, nebo prevence na úrovni překladače. Strukturální hazard vzniká při souběžném požadavku více částí zřetězené jednotky na sdílenou sběrnici, ke které má přístup vždy jen jedna jednotka – přístup je nutné koordinovat, což zpomaluje práci.

WIP skok na PJP překladače <br />

Nepodmíněné skoky a volání podprogramů s pevnou adresou jsou jednoduše řešitelné – zřetězená jednotka začne vybírat instrukce z cílové adresy. Pokud se cílová adresa musí vypočítat z již rozpracovaných instrukcí, výsledek není včas k dispozici a hrozí výpadek fronty; četnost těchto případů lze snížit optimalizací pořadí strojových instrukcí v překladači.

Podmíněný skok je nejkomplikovanější případ – cílová adresa je zpravidla známá, ale není jasné, zda se skok provede. Jedno řešení pokračuje sekvenčně a v případě skoku použije rozpracovanou frontu; jinak ji zahodí a začne znovu. Výkonné procesory implementují dvě paralelní fronty – jedna pokračuje sekvenčně, druhá (kratší, typicky 4 kroky) připravuje instrukce z cílové adresy; přepnutí front je výhodnější než výpadek celé fronty.

Procesory RISC používají navíc predikci skoků. Statistiky ukazují, že podmíněné skoky tvoří 15–25 % instrukcí, proto se vyplatí hledat levná řešení jejich předpovídání. <br />
![image](https://hackmd.io/_uploads/SyxwyK3kMg.png) <br />
![image](https://hackmd.io/_uploads/SkX_ytnJze.png) <br />
Ve formátu instrukce je vyhrazen jeden bit, který predikuje, zda se skok provede.

Statická predikce vkládá bit již při kompilaci nebo programátorem. Dynamická predikce zaznamenává výsledek každého provedeného podmíněného skoku a přizpůsobuje se aktuálním podmínkám – je výhodnější, ale vyžaduje zápis predikčního bitu, což může být technicky komplikované nebo nemožné u chráněné paměti. Jednobitová predikce selhává vždy na začátku a na konci každého cyklu; u vnořených cyklů je chybovost výrazně vyšší. Dvoubitová predikce snižuje počet selhání na jedno za cyklus, a to až na jeho konci. Chování dvoubitové predikce popisuje čtyřstavový automat: stav A predikuje provedení skoku, stav N jeho neprovedení; přechod mezi nimi nastane až po dvou stejných výsledcích po sobě. V ustáleném stavu se predikce nastaví na A–00 nebo N–11

[UTI automaty neboli modely start](#####UTI_MODELY_AUTOMATY) <br />

Ve tříúrovňové zřetězené jednotce (VID → VVD → PUV) způsobí provedení skokové instrukce zahození všech právě rozpracovaných instrukcí. Místo zahozených instrukcí lze vložit prázdné instrukce NOP – logika programu se nezmění, ale efektivita procesoru neklesá. Lepším řešením je před skokovou instrukci přesunout několik instrukcí, které nesouvisí s podmínkou skoku – ty se pak vykonají na místě NOP a zpoždění skoku se využije produktivně. Optimalizující překladač dokáže takovéto přeskupení instrukcí realizovat poměrně snadno.

Tabulka provedených podmíněných skoků je implementována přímo v procesoru s pevně danou velikostí; ukládají se do ní adresy naposledy provedených skoků. Na základě těchto dat se aplikuje jednobitová nebo dvoubitová predikce. Metoda nevyžaduje úpravu formátu strojových instrukcí, není závislá na překladači a je zpětně kompatibilní s existujícím strojovým kódem.

##### C.I: CISC
##### CISC
Screeny z poliho skript <br />
![image](https://hackmd.io/_uploads/SyulGtn1Me.png) <br />
![image](https://hackmd.io/_uploads/SyRxfY31Mx.png) <br />
![image](https://hackmd.io/_uploads/SkoZMF31Gx.png) <br />
![image](https://hackmd.io/_uploads/BylGfK21Mg.png) <br />
![image](https://hackmd.io/_uploads/SJvMztnJzl.png) <br />
![image](https://hackmd.io/_uploads/HJpzfFhJzl.png) <br />
![image](https://hackmd.io/_uploads/SyM7zK2Jzl.png) <br />
![image](https://hackmd.io/_uploads/S1L7GYhyzl.png) <br />
![image](https://hackmd.io/_uploads/rkjQzF31Mx.png) <br />
![image](https://hackmd.io/_uploads/ByeEfFhyGx.png) <br />
![image](https://hackmd.io/_uploads/B1U4zK3yMx.png) <br />
![image](https://hackmd.io/_uploads/Bk24GKnJGe.png) <br />
![image](https://hackmd.io/_uploads/S1zrMYhkGe.png) <br />
![image](https://hackmd.io/_uploads/HJvHzYh1Gg.png) <br />
![image](https://hackmd.io/_uploads/S1hBzK31Mx.png) <br />
![image](https://hackmd.io/_uploads/SJz8zKnkMg.png) <br />
![image](https://hackmd.io/_uploads/r1xtzFnkzx.png) <br />
![image](https://hackmd.io/_uploads/Sk9KMK2kfl.png) <br />
![image](https://hackmd.io/_uploads/Hy-qMK2kMg.png) <br />
![image](https://hackmd.io/_uploads/SJwcMK2yzx.png) <br />
![image](https://hackmd.io/_uploads/SJ65zKnyMx.png) <br />
![image](https://hackmd.io/_uploads/HkmoMFhyfe.png) <br />
![image](https://hackmd.io/_uploads/rJhsGFn1Ge.png) <br />
![image](https://hackmd.io/_uploads/r1QnGtnJfg.png) <br />
![image](https://hackmd.io/_uploads/H1D3fFhkMx.png) <br />

Architektura jako screeny z poliho skript: <br />
![image](https://hackmd.io/_uploads/ry2igt21Ml.png) <br />
![image](https://hackmd.io/_uploads/SyxhgFnJze.png) <br />
![image](https://hackmd.io/_uploads/HkUnxt3kzx.png) <br />
![image](https://hackmd.io/_uploads/HJ32xK21fx.png) <br />
![image](https://hackmd.io/_uploads/BJHaet3kGx.png) <br />
![image](https://hackmd.io/_uploads/rJYpWY3Jfx.png) <br />
![image](https://hackmd.io/_uploads/SkN0WYhkzx.png) <br />

TODO fixnout nadpisy všude po docu

### 1.2) PJP
![image](https://i.imgur.com/uNzoMmV.png) <br />
![image](https://i.imgur.com/s9pxcHs.png) <br />
![image](https://i.imgur.com/lvMkZNC.png) <br />
![image](https://i.imgur.com/x1k0gLH.png) <br />
![image](https://i.imgur.com/RbloneI.png) <br />
![image](https://i.imgur.com/fBNk1i3.png) <br />
![image](https://i.imgur.com/18FurZn.png) <br />
![image](https://i.imgur.com/p5LsB2H.png) <br />
![image](https://i.imgur.com/f0qMZj2.png) <br />
![image](https://i.imgur.com/iUMFQ8A.png) <br />
![image](https://i.imgur.com/xIm8iIC.png) <br />
![image](https://i.imgur.com/RtZf5ET.png) <br />
![image](https://i.imgur.com/ehsZ8uf.png) <br />
![image](https://i.imgur.com/vdr0y85.png) <br />
![image](https://i.imgur.com/tUzyB01.png) <br />
![image](https://i.imgur.com/ZnjFp01.png) <br />
![image](https://i.imgur.com/GKTACIQ.png) <br />
![image](https://i.imgur.com/ujig0fC.png) <br />
![image](https://i.imgur.com/QfV3U9W.png) <br />
![image](https://i.imgur.com/4GQEVlY.png) <br />
![image](https://i.imgur.com/dCYPczT.png) <br />
![image](https://i.imgur.com/YMg0Xa1.png) <br />
![image](https://i.imgur.com/t1JwDd2.png) <br />
![image](https://i.imgur.com/v21wPka.png) <br />
![image](https://i.imgur.com/2mkO0C5.png) <br />
![image](https://i.imgur.com/maSCoaP.png) <br />
![image](https://i.imgur.com/jUFhEhi.png) <br />
![image](https://i.imgur.com/hphzLyC.png) <br />
![image](https://i.imgur.com/brj4Vql.png) <br />
![image](https://i.imgur.com/4Vjfdme.png) <br />
![image](https://i.imgur.com/FsTxeZV.png) <br />
![image](https://i.imgur.com/1OlBWLF.png) <br />
![image](https://i.imgur.com/iZdJMa6.png) <br />
![image](https://i.imgur.com/ZTKpSTq.png) <br />
![image](https://i.imgur.com/za48Gq9.png) <br />
![image](https://i.imgur.com/5t4Xmuy.png) <br />
![image](https://i.imgur.com/uMfrNJL.png) <br />
![image](https://i.imgur.com/3lF5jeN.png) <br />
![image](https://i.imgur.com/0vVn6Ma.png) <br />
![image](https://i.imgur.com/wYmkdOf.png) <br />
![image](https://i.imgur.com/OuqUTH0.png) <br />
![image](https://i.imgur.com/0jhanh3.png) <br />
![image](https://i.imgur.com/zw9ZLia.png) <br />
![image](https://i.imgur.com/Tk6G5CP.png) <br />
![image](https://i.imgur.com/nDpHZHg.png) <br />
![image](https://i.imgur.com/V0d6zpE.png) <br />
![image](https://i.imgur.com/RZyfoIh.png) <br />
![image](https://i.imgur.com/c5FVntJ.png) <br />
![image](https://i.imgur.com/JSvKy9r.png) <br />
![image](https://i.imgur.com/Cl0FmDZ.png) <br />
![image](https://i.imgur.com/xT6Jj2M.png) <br />
![image](https://i.imgur.com/DjGOuND.png) <br />
![image](https://i.imgur.com/HjcNvg8.png) <br />
![image](https://i.imgur.com/D0dPu4J.png) <br />
![image](https://i.imgur.com/7okxR8V.png) <br />
![image](https://i.imgur.com/EP846Mx.png) <br />
![image](https://i.imgur.com/zqzD4Sz.png) <br />
![image](https://i.imgur.com/ADdz8AO.png) <br />
![image](https://i.imgur.com/KOOU9fe.png) <br />
![image](https://i.imgur.com/2wEWexN.png) <br />
![image](https://i.imgur.com/v5cFvTY.png) <br />
![image](https://i.imgur.com/nEsEzGy.png) <br />
![image](https://i.imgur.com/dpazlOW.png) <br />

### 1.3) Programka (OOP, JAVA, FPR, UPR, SKJ)
Možná vztahy na DSka, ALG a jakési PJP, ZDS. Něco malinko z SWI stuff.

* Public declaration is accessible to all clients.
* Protected declaration is accessible only to the class itself and its subclasses.
* Private declaration is accessible only to the class itself.

### 1.4) ALG

### 1.5) ZSU

### 1.6) Sítě
WIP JUMP na ZDS <br />
* Simplex, signál jedním směrem, např. TV broadcast
* Half duplex, signál v obou směrech, ale jen one at a time, 2 way rádio, nebo Ethernet stanice propojené přes hub
* Full duplex, komunikace v obou směrech naráz, např. switched ethernet

* Paralelně transmittujeme několik bytů
* Seriálně bit by bit transmit, nejčastěji používané, synchroně nebo async. Kabely totiž drahé a media interface circuitry + synchronizační problémy

**Async. seriál:** <br />
Data trasmitted char by char, where char can have 5 to 8 bits. Reciever a transmitter mají independent clocks sejné frekvence. Před tranzmicí každého charu se synchronizuje clock recievera přes leading edge of the start bit. As the difference between the transmitter and receiver clocks still increases, we may transfer just a few bits without a need of resynchronization.

Paritní bit na konci každého charu pomáhá detekovat pár transmit. errors. Pauza mezi charaktery aby reciever zprocesoval charakter. Stop bit - 1 má opozitní polaritu od start bitu - 0. Pauzy pro synchronizaci a mezi charaktery jsou oproti synchronní komunikaci neefektivní, proto používané pro terminály, industriální automaci, PC COM porty, čiže pomalá character orientovaná komunikace.

**Sync. seriál:** <br />
Reciever clock derivovaný z reciever signálu. Transmiter a reciever hodiny vždy synchronised. Data transmit. ve framech skládající se z headeru, payload (variable length, hundreds of bytes to few kilobytes) a frame checksum (FCS). Frames delimitované flagy in a transmitted bit stream. Pokud nejsou data na transmit, tak transmiter posílá empty frames / repeating flags. Menší overhead, bo není potřeba synchronizovat pro každý char. <br />
Pro highspeed data transfer na isochronous links, tedy LANs, WAN linky, ISDN channely.

Transmitované data reprezentované změnami fyzické kvantity, tedy signály. Jiné často používané fyzické kvantity jsou voltage / current, intenzita elekromagnetické radiace neboli světla, sound pressure. Signál cestuje médiem, např. optickým vláknem, twisted pair či coaxial káblem. <br />
![image](https://hackmd.io/_uploads/r1Bj1c2JMg.png) <br />
Charakteristiky transmission media: attentuation, crosstalk, ACR, velocita propagace signálu, return loss. Tyto charakteristiky jsou závislé na frekvenci, tedy se snažíme utilizovat nejvíce narrow frequency band, co jde. <br />
![image](https://hackmd.io/_uploads/S1LfgcnyMx.png) <br />
Signál afektován tím médiem přenosu, např. sinusovka obsahuje jednu frekvenci, získáme particular parametr z measured medium charakteristik. Každý periodický signál treated jako suma (nekonecnych) sinusovkových vln různých frekvencí. Několik instancí základní frekvence - komponenty individuálních signálů se liší v aplitudě a phase shiftu. Kalkulované Fourier sérií. Investigace jak medium influencuje individuální signálové komponenty a pak suma results. <br />
![image](https://hackmd.io/_uploads/rJ4gZc2Jzl.png) <br />
Basically používáme integrály.

Frekvenční spektrum signálu indikuje how much power is carried by individual harmonic components. Allows us to asses how much neglecting / filtering out some components influences the signal.

Baseband utilizuje celý bandwidth média, signál může obsahovat frekvence hodně blízko k nule. Broadband používá specifickou část bandwidthu, několik komunikací mohou používat toto médium naráz, avoids usage of subbands with unsuitable charakteristik - static či dynamic selection. <br />
U broadbandu ten signál můžeme signál shiftnout na freq. band suitable for transmission over a particular medium using modulation, also solving problems with channels that cannot pass the DC component. <br />
![image](https://hackmd.io/_uploads/Hk7WMq31fe.png) <br />
![image](https://hackmd.io/_uploads/HyHbMq2JGl.png) <br />
![image](https://hackmd.io/_uploads/BJo-z5nJzl.png) <br />
![image](https://hackmd.io/_uploads/S1NGG53JMl.png) <br />
* Modulation rate: num of changes of signal during a time interval, measured in bauds - Bd.
* Transfer date: number of bits transferred during a time interval, measured in bits per seconds - bps.

The transfer rate can be higher than the modulation rate, as we may represent multiple bits by a single signal change, provided that we have enough types of the signal changes. U basebandu encodovaný bit stream je transmitted v originálním freq. bandu, modulace není využitá. Casto pouzivane pro metallic media v LANs nebo optické média v LANs a WANs.

Vzdálenost je limitovaná kvuli par nestabilnim charakterisitc media v nekterych castech nami pouzivaneho frequency band. Kdyz nevyuzivame modulaci, tak potrebujeme dalsi mechanismus synchronizace mezi transmitterem a recieverem, neboli data encoding. Aby měl reciever šanci se synch., ensurujeme dostatek změn signálu, nutné pro fázi synchronizace kontinuálního adjustmentu reciever hodin, ale signál s víc změnama v nějakém časovém intervalu obsahuje víc frekvencí a potřebuje teda širší frequency band.

Dál odstranujeme DC komponent, if the coupling circuitry, such as a transformer, does not pass the DC component, we would not be able to tell a diff between a seq of 0s and 1s. Do not confuse the data encoding with data encryption applied for security purposes. 0s and 1s are encoded directly by a low and high signal levels respectively during the whole bit interval. <br />
![image](https://hackmd.io/_uploads/By0xE5hkfl.png) <br />
Nejvíc se používá na encoding basebandu Manchester a diferenční Manchester.

**Manchester:** <br />
Jednička expressed by a low to high transition uprostřed periody a nulou v high to low. Tranzice na začátku periody are made as neccessary and dont signify data. Používané v 10Mbps Eth v copper media.

**Differential Man.:** <br />
Nula expressed jako změna signálu na začátku periody a 1 jako nezměněná hodnota. There is always a transition at the middle of the period (either low-to-high or high-to low as necessary to encode the subsequent bit). <br />
![image](https://hackmd.io/_uploads/Hyq2VqnyMl.png) <br />

Rate Zero má 3 levely signálu, 0, -1 a +1. Pozitivní 1 reprezentuje binární 1 a negativní binární 0. Signál vždy na levelu 0 v druhe pulce intervalu.

Non Return to Zero Inverted má 2 sign. levely. Změna signálu enkoduje binární 1, k enkodaci 0 necháme signál na original urovni.

AMI neboli Alternate Mark Invasion, 0, -1 a +1 levely. Binary 0: level 0. Binary 1: reprezentováno alternately by -1 a +1 levely. By violation of polarity alternation rule, we mark a significant event in the data stream, třeba start a začátek framu. Stále problém s reciever synchronizací po dlouhé sekvenci 0. <br />
![image](https://hackmd.io/_uploads/rJd2S92yze.png) <br />
![image](https://hackmd.io/_uploads/ryT2B92yGx.png) <br />

![image](https://hackmd.io/_uploads/SyJpj9nJMe.png) <br />
![image](https://hackmd.io/_uploads/ryLaoqn1Ge.png) <br />
![image](https://hackmd.io/_uploads/Bkhps5n1Mg.png) <br />

#### Přenosové média
* Copper neboli měděné, metallic káble: Coaxial a Twisted Pair, který ještě je shielded nebo unshielded. V případě coaxialu drahé, avšak dobré parametry ve vysokofrekv. rangi, pro baseband i broadband. Twisted Pair je levnější, začalo v telefonních linkách, horší parametry. Diferenční mode tranzmice přes balanced pair, kdy reciever detekuje rozdíl mezi 2 levely.
* Optické v singlemode nebo multimode
* Wireless <br />
![image](https://hackmd.io/_uploads/HkkDU52Jfg.png) <br />
![image](https://hackmd.io/_uploads/H1H08cnkGg.png) <br />
![image](https://hackmd.io/_uploads/S1Jkwq2kzx.png) <br />
![image](https://hackmd.io/_uploads/rJ4evq3yfg.png) <br />

Optické vlákna pro velmi high transfer rates of tens of Gbps. Resilient proti šumu a signal trapping neboli eavesdropping. Reachable distance záleží na bitratu, again, máme multimode nebo singlemode.

Optická vlákna fungují na principu šíření světla v jádře s vyšším indexem lomu než má okolní plášť, takže se světlo uvnitř udržuje pomocí úplného vnitřního odrazu na rozhraní těchto dvou prostředí. Chování paprsku při přechodu mezi prostředími popisuje Snellův zákon lomu, který říká, že změna směru závisí na poměru indexů lomu. Důležitou vlastností vlákna je numerická apertura, která určuje, pod jakým maximálním úhlem může světlo do vlákna vstoupit, aby se v něm ještě šířilo.

V multimódových vláknech se světlo šíří v mnoha módech, tedy po různých drahách, které odpovídají různým úhlům dopadu, a přenos probíhá postupnými odrazy od stěn jádra díky úplnému vnitřnímu odrazu, což umožňuje vedení signálu na delší vzdálenosti, i když s většími disperzními ztrátami. Vybraná frekvence musí být kompatibilní s produkcí světla ze zdrojů a detekování... well, detektory, takže LEDs, PIN fotodiody,... Několik ranges mohou být použity paralelně - WDM a DWD< systémy.

2 level data encoding: tma a světlo, attentuation není hlavní problém, hlavní limitace je bit rate limitace disperzí, což deformuje čtvercový signál tak, že se pulsy overlappují, jelikož několik frekvencí cestuje vláknem ruznymi rychlostmi, snažíme se použít zdroje světla s narrow freq. band emitovaného světla, třeba laser. To je chromatic disperze, když popisujeme modal disperzi, tak tomu rozumíme tak, že několik light rays vstoupí do vlákna pod ruznymi uhly, ty se pak odráží v ruznych uhlech skrze to vlákno. Path of the rays mají jiné délky a z toho vzniká ten delay, co deformuje signál, muzeme to redukovat s gradient index vlaknem, kde rays followují sinusoidní paths. Kompletně se tohoto zbavíme se signal mode vlákny. <br />
![image](https://hackmd.io/_uploads/H1z6Kq2JMe.png) <br />
Svařování. <br />
![image](https://hackmd.io/_uploads/BJzAYq3yze.png) <br />

**Structured cabling:** <br />
V dnešní době používáme generický cabling systém nezávislý na aplikaci v particular sítové technologii. Integrace např. LAN, telefonie, alarmových systémů. Umoznuje upgrade v budoucnosti a zmeny obecne jsou ez. Instalacni investment je vsak vysoky k ad-hoc cabling čistě pro current potřeby. <br />
![image](https://hackmd.io/_uploads/r18I9ch1Mx.png) <br />
Network devices and stations may be interconnected in a flexible manner using patch cords on appropriate patch panels.

#### Connection oriented vs. conectionless comm, vrstvy
![image](https://hackmd.io/_uploads/r1Pp5qhJGl.png) <br />
![image](https://hackmd.io/_uploads/SkaC952JGe.png) <br />
![image](https://hackmd.io/_uploads/H1zJi53Jfe.png) <br />
![image](https://hackmd.io/_uploads/BkiJs521fl.png) <br />
![image](https://hackmd.io/_uploads/SJEes531ze.png) <br />
![image](https://hackmd.io/_uploads/rkngiqn1fx.png) <br />
![image](https://hackmd.io/_uploads/rkjWj9h1Me.png) <br />
![image](https://hackmd.io/_uploads/HyGzoqnkfg.png) <br />
![image](https://hackmd.io/_uploads/rk5Go531Ge.png) <br />
![image](https://hackmd.io/_uploads/S11Xs531Gx.png) <br />
##### ISO/OSI
[TCP/UDP skok](#####TCP/UDP) <br />
#### LAN či WAN topologie
##### LAN_a_WAN
![image](https://hackmd.io/_uploads/H1KPj9nJMg.png) <br />
![image](https://hackmd.io/_uploads/HkfOj521Ge.png) <br />
![image](https://hackmd.io/_uploads/Bydus931Me.png) <br />
![image](https://hackmd.io/_uploads/BJ6diq2JMg.png) <br />
![image](https://hackmd.io/_uploads/BJVti9hkze.png) <br />

#### Adresace
##### ADRESACE
![image](https://hackmd.io/_uploads/S1TJ3qh1fe.png) <br />
![image](https://hackmd.io/_uploads/HkHe392Jzx.png) <br />
![image](https://hackmd.io/_uploads/B1penq2JGl.png) <br />
![image](https://hackmd.io/_uploads/SJQWh53kfe.png) <br />
![image](https://hackmd.io/_uploads/S1dZ35n1Ge.png) <br />
![image](https://hackmd.io/_uploads/HkTlV7yeGl.png) <br />
![image](https://hackmd.io/_uploads/S1K-EQJxMl.png) <br />
![image](https://hackmd.io/_uploads/HJxfNXylzl.png) <br />
![image](https://hackmd.io/_uploads/SksfVmJgGg.png) <br />
![image](https://hackmd.io/_uploads/r1JQNQylfl.png) <br />
[VLSM](#####VLSM) <br />

#### LAN zařízení
* Interconnection of (originally separate) network segments
* Division of too large (congested) networks

**Duvody pro connection a divizi:** <br />
* Increase of the coverage
* Overcoming of reach limitation of the particular network technology
* Interconnection of originally independent and/or geographically distant networks
* Traffic separation
* Reduction of collisions and broadcast traffic
* Better fault resiliency (fault isolation)
* Security (eavesdropping, attacks etc.) <br />
![image](https://hackmd.io/_uploads/r1nw25hkzg.png) <br />
![image](https://hackmd.io/_uploads/H1Su393kGg.png) <br />
![image](https://hackmd.io/_uploads/HyTu2cn1Gg.png) <br />
1. Election of the tree root neboli root bridge, zvoleno podle konfigurace bridge priorit a nebo factory set Bridge ID když máme equal priorities všude. <br />
2. Creation of the shortest paths tree, preference linek influenced konfigurací a nebo dle ceny linek. Link cost je set in reverse proportion to the link speed by def, čiže faster link má menší cenu. <br />
3. Porty na stejném stromě forwardují framy, zbytek je blokován. <br />

Root bridge generuje BPDU zprávu každé dvě sekundy, který cestuje stromem dolů. Každý bridge checkne prezenci BPDU na svém root portu. STP algoritmus definuje transient port stavy jako learning a listening, potřebné pro avoidance of temporary loops during convergence. Po failure, rekonvergence muze trvat az 50 sekund. <br />
![image](https://hackmd.io/_uploads/r1W0aq21Ge.png) <br />
![image](https://hackmd.io/_uploads/Hy1xCcnJGl.png) <br />
![image](https://hackmd.io/_uploads/BkEP1snJMl.png) <br />
![image](https://hackmd.io/_uploads/SklOyo2JGe.png) <br />
![image](https://hackmd.io/_uploads/rkjOko31fx.png) <br />
![image](https://hackmd.io/_uploads/rJQq1ihkMl.png) <br />
![image](https://hackmd.io/_uploads/HJZj1j2yzx.png) <br />
![image](https://hackmd.io/_uploads/B18jkj2JMl.png) <br />

**Routing protokoly rozdíly:** <br />
* utilizované metriky
* levels of routers knowledge of the network topology
* schema propagace of the routing info, rozumime exchange between neighbours, flooding to all routers nebo diffusion algoritmus atd.
* technicka implementace posilani routing infa, tedy broadcast ci multicast, update period
* zda je aim fast konvergence, i.e. cas mezi zmenami topologie a stabilizace routing tables of all routers

**Klasifikace rout. prot.:** <br />
* Distance vektor, starší, avšak ez impl.
* Link state, komplexnější, ale rychlejší konvergence, víc determenistické chování ve special případech <br />
![image](https://hackmd.io/_uploads/ByKixshJze.png) <br />
![image](https://hackmd.io/_uploads/S1Gngj31Me.png) <br />
![image](https://hackmd.io/_uploads/B1vTxonyzg.png) <br />
![image](https://hackmd.io/_uploads/S1KRxi3yfx.png) <br />
![image](https://hackmd.io/_uploads/BJVkbj3kMl.png) <br />
WIP skok na grafy v DIM <br />

* **Dijkstra:** Calculates a shortest paths tree from a given vertex to all other vertices of a edge-labeled graph Used in OSPF (a little bit modified)
* **Floyd:** Calculates routing tables for individual routers from a cost matrix of the network topology graph
* **Ford-Fulkerson:** Calculates distances from all nodes to a given node In distributed version used as a basis of RIP <br />
![image](https://hackmd.io/_uploads/rkIEbj3yMg.png) <br />
##### VLSM
[IPs a adresace zpátky](#####ADRESACE) <br />

![image](https://hackmd.io/_uploads/B1Aubin1ze.png) <br />
##### VLANY
[Skok na advanced switching](#####SWITCHING_DEEP) <br />
![image](https://hackmd.io/_uploads/HJe5ZjnJfl.png) <br />
![image](https://hackmd.io/_uploads/rkF5Zj3kGl.png) <br />
![image](https://hackmd.io/_uploads/SkxsZihkfx.png) <br />
No (active) switch port belongs to red VLAN, do not sent red VLAN frames to me (prune the red VLAN tree) <br />
![image](https://hackmd.io/_uploads/Hyd3Zih1Gg.png) <br />
![image](https://hackmd.io/_uploads/rkz6Wih1Me.png) <br />
![image](https://hackmd.io/_uploads/Hk2hSQygMg.png) <br />
![image](https://hackmd.io/_uploads/rJw6rm1efx.png) <br />
![image](https://hackmd.io/_uploads/HyZ0B7ygMe.png) <br />
![image](https://hackmd.io/_uploads/B19CS7JgGx.png) <br />
![image](https://hackmd.io/_uploads/BJe1LXkxMg.png) <br />

TODO nalinkuj ISO OSI subkapitoly na sebe a link na TCP IP protocol suite veci z L5 6 <br />
![image](https://hackmd.io/_uploads/SywQzs3yzl.png) <br />
![image](https://hackmd.io/_uploads/BkkNGjhJfl.png) <br />
* PPP – Point to Point Protocol, Asynchronous or synchronous links (dial-in to ISP, links between routers, ...)
* HDLC – High Level Data Link Control, A predecessor of the most of today's link protocols
* LAPD – Link Access Procedure – D-channel, Encapsulated signaling messages on ISDN D-channel
* Logical Link Control (IEEE 802.2), Unifies MAC sublayers of various LANs

![image](https://hackmd.io/_uploads/HkNwEQ1lMe.png) <br />
![image](https://hackmd.io/_uploads/HyxuE7kgGx.png) <br />
![image](https://hackmd.io/_uploads/Bkq_V7Jxzx.png) <br />
![image](https://hackmd.io/_uploads/HkdtVQ1lGx.png) <br />
![image](https://hackmd.io/_uploads/rJycN7yxfl.png) <br />
![image](https://hackmd.io/_uploads/r1h94XyeMe.png) <br />
**General Classification:** <br />
* Centralized Control
* Distributed Control

**Centralized Control** <br />
A master station is dedicated to assign the capacity of the channel to the other (slave) stations. Introduces a single point of failure.

**Centralized Control – Polling** <br />
The central station polls (offers the right to transmit to) the other stations. The polled station either sends the data frame or informs that there are no data to send, or remains silent. Round-robin polling scheme is applicable for channels with a small signal propagation delay; behaves well when the most of stations want to transmit equally and all the time, but is inefficient for large number of stations and a light of unbalanced load. Other polling schemes may be also applied.

**Centralized Control – Request Arbitration** <br />
Stations use the separate (narrow-band) channels to ask the access to the data channel. The central station arbitrates the requests and assigns the channel – the channel assignment message is transmitted on the common data channel. Used in radio networks, where a low-speed TDM channel is commonly used for access requests.

**Contention-free Protocols – Distributed Control** <br />
Independent on a single central control station. The implementation tends to be more complicated. <br />
![image](https://hackmd.io/_uploads/B1ATEQklfe.png) <br />
![image](https://hackmd.io/_uploads/H1K04Xkefg.png) <br />

**Distributed Control – Token Passing**
A right to transmit is represented by a token; a station may hold the token only for a limited time. The token is passed around between nodes, and every station needs to know its address and the successor address. Necessary supporting mechanisms include ring initialization (stations have to learn their successors), attachment of another station to the ring, detachment of station from the ring, and handling of the token loss and duplication.

**Virtual Token Passing**... A station with address m senses the medium and determines that station with address n just finished its transmission. Station m may start to transmit if the medium is idle for ((m-n) mod N)*t, where N is the total number of stations and t is the longest possible signal propagation time.

After a frame transmission finishes, every other station has a dedicated time interval to start its transmission; if it does not start, the next station gets its chance and so on.

The procedure can be seen as passing of an implicit (virtual) token, which limits the overhead of passing the real token. Stations have to hear each other well. More efficient compared to standard token passing if there is a lot of stations and a light load.

**Distributed Medium Access Control – Access Control on Ring Networks**
Token Ring (Newhall): a station ready to transmit changes the identifier of the arrived token frame to identify the data frame and sends its data frame; after the data frame returns back, the token is released to the neighboring station.

Slotted Ring (Pierce ring): fixed-size frames with a control bit indicating whether the frame is busy or empty circulate around the ring; the source station that receives its own frame coming back from the ring resets the busy indicator bit.

**Distributed Medium Access Control – Access Control on Ring Networks**
Register Insertion Ring: the station prepares the frame to transmit in a shift register that may be switched into the ring between two frames; after the frame rotates round the ring, the switch register is switched out. The fact that frames return back to the source in the ring networks may be utilized to acknowledge reception by the receiver to the source station using control bits of the frame header.

**Comparison of the Contention-free to Probabilistic MAC Protocols:**
* Delay of the packet delivery under the light load.
* The contention-free protocols introduce an overhead of the MAC algorithm grows with a number of involved stations.
* Channel utilization under heavy load.
* Probabilistic methods cannot avoid the complete blocking of the channel by collisions.

**Ethernet and IEEE** <br />
[Topologie relation zpětně](#####LAN_a_WAN) <br />

[Back to VLANS](#####VLANY) <br />
##### SWITCHING_DEEP
**Switching Advantages:** <br />
Switching is collision-free, which results in a higher overall transfer rate with no data loss and allows different pairs of network segments to communicate simultaneously.

Switches can enforce more deterministic network behaviour through frame priorities and flow control.

Better security is achieved as only frames destined for a node are passed to its NIC after a CAM table is learned, making eavesdropping more difficult.

Network maintenance is easier due to isolation of faulty segments, broadcast storm control, and intruder detection using source MAC addresses.

**Switching Methods:** <br />
Store-and-forward reads the whole frame into memory, checks CRC, and then forwards it to the destination port. This is inevitable in case of asymmetric switching (switching between segments with various port bandwidths).

Cut-through begins forwarding the frame just after the destination MAC address is read.

Fragment Free combines advantages of both previous methods – it operates as cut-through, but delays the beginning of transmission until there may not happen a collision on the source port, provided the physical network cabling is designed properly; useful in network designs that combine switches and hubs (group switching).

**Parameters of LAN Switches:** <br />
Number of MAC addresses per port determines whether the port can connect just one station or a hub (group switching). Total number of MAC addresses equals the number of rows in the CAM table. Methods of address-to-port assignment are either dynamic (self-learning, flooding of frames with unknown addresses) or static (supports intruder detection).

Further parameters include administration method and port monitoring capabilities (Telnet, SNMP, WWW), SPAN ports (Switched Port Analyser), and additional functions such as multicast processing, traffic filtering, and VLAN support.

**Half-duplex and Full-duplex mode in switched networks: :** <br />
Full duplex is collision-free and offers longer reach with no timing requirements for CSMA/CD. Half duplex means the switch port and station's NIC contend for the medium, so collisions may occur. Every switch port may operate in different mode; half duplex is still supported because of old NICs and backward compatibility. <br />
![image](https://hackmd.io/_uploads/r1VELX1eGe.png) <br />
![image](https://hackmd.io/_uploads/Bkt48X1lfl.png) <br />
![image](https://hackmd.io/_uploads/BJZB8Qkeze.png) <br />
![image](https://hackmd.io/_uploads/rJ9r871gzl.png) <br />
![image](https://hackmd.io/_uploads/By-U8XylGl.png) <br />
![image](https://hackmd.io/_uploads/S1CtU71lGg.png) <br />
![image](https://hackmd.io/_uploads/SJHqIQklzx.png) <br />
![image](https://hackmd.io/_uploads/rJj587klzx.png) <br />

##### Aplikační vrstva
![image](https://hackmd.io/_uploads/H1d5Hs3kMe.png) <br />
![image](https://hackmd.io/_uploads/SkMjHj2Jzg.png) <br />
![image](https://hackmd.io/_uploads/S1nsSs21Me.png) <br />
![image](https://hackmd.io/_uploads/HymhBon1Ge.png) <br />
![image](https://hackmd.io/_uploads/SyxpSjnJzx.png) <br />
"SMTP posíláš, POP3 stahuješ z poštovního setveru k sobě na fyzicky svuj disk a pak se to smaže z toho poštovního serveru a IMAP je poštovní... IMAP umožnuje pracovat s poštou přímo na serveru" <br />
![image](https://hackmd.io/_uploads/rypfIihyzg.png) <br />
![image](https://hackmd.io/_uploads/Skk4Ui3yfg.png) <br />
![image](https://hackmd.io/_uploads/r1n48oh1Mg.png) <br />
WIP link na URI a URL z programka <br />
![image](https://hackmd.io/_uploads/S1g8Li31Ge.png) <br />
![image](https://hackmd.io/_uploads/SyvU8snkMl.png) <br />
![image](https://hackmd.io/_uploads/r1lDIs31Ge.png) <br />
![image](https://hackmd.io/_uploads/BkKKIo21Mg.png) <br />
![image](https://hackmd.io/_uploads/rJX9Uj2JGx.png) <br />
![image](https://hackmd.io/_uploads/B1s9Ls2yGe.png) <br />
![image](https://hackmd.io/_uploads/B1t1DonyMx.png) <br />
![image](https://hackmd.io/_uploads/S12MvjhkGl.png) <br />
![image](https://hackmd.io/_uploads/BkccPohkfx.png) <br />
![image](https://hackmd.io/_uploads/ryX3Pj2JMg.png) <br />
![image](https://hackmd.io/_uploads/SywADj2yzg.png) <br />
![image](https://hackmd.io/_uploads/rkb-Osn1fl.png) <br />
![image](https://hackmd.io/_uploads/SJjb_o21fl.png) <br />
![image](https://hackmd.io/_uploads/HJafdo3JGe.png) <br />
![image](https://hackmd.io/_uploads/r1M7uihyMx.png) <br />
![image](https://hackmd.io/_uploads/SkOQOonyfl.png) <br />
![image](https://hackmd.io/_uploads/HJENuj3yMg.png) <br />
![image](https://hackmd.io/_uploads/S1krOi2JGe.png) <br />
##### TCP/UDP
[ISO/OSI vrstvy zpátky](#####ISO/OSI) <br />
![image](https://hackmd.io/_uploads/rkDvdjnkze.png) <br />
![image](https://hackmd.io/_uploads/HJMOdjh1zl.png) <br />
![image](https://hackmd.io/_uploads/S1_OOo3JGl.png) <br />
![image](https://hackmd.io/_uploads/r1gidjn1fl.png) <br />
![image](https://hackmd.io/_uploads/BydjOj2kze.png) <br />
![image](https://hackmd.io/_uploads/r1s2us2Jzx.png) <br />

**NAT**
![image](https://hackmd.io/_uploads/SJxBPXyefg.png) <br />
**NAT Modes** <br />
* Full-cone NAT (one-to-one NAT): when the internal address is mapped to an external address, any external host can send packets to any port of internal address by using the external one.
* Address-restricted-cone NAT: outside host can send packets to any port on internal host once a packet came to it from the external address corresponding to the internal address.
* Port-restricted cone NAT: like (A)RC NAT, but limited to the port as well.
* Symmetric NAT: requests from the same internal address and port to different outside hosts are mapped to different external address/port pairs, PRC NAT rules apply.

**Static and Dynamic NAT** <br />
Static NAT: the translation table is preconfigured manually.

Dynamic NAT: the contents of the translation table is created dynamically according to the network traffic, and public addresses are allocated to individual conversations from the public address pool. Nowadays a combination of both approaches is typically used.

**Usages of Static NAT** <br />
Static translation of a (private) inside source address to a (global) address of the outside network. Static translation of a (global) outside destination address to a particular (private) address of the inside network – "port forwarding", making internal server with specific addresses accessible from outside, with port preservation using the same (TCP/UDP) port for inside and outside address, though not always possible.
![image](https://hackmd.io/_uploads/SkuUvXJxMe.png) <br />
![image](https://hackmd.io/_uploads/HykDPQkgfg.png) <br />
![image](https://hackmd.io/_uploads/rkUDvXkxMl.png) <br />
![image](https://hackmd.io/_uploads/r1hDvXJeMx.png) <br />

NAT Disadvantages** <br />
* Limits the universal connectivity... only clients may reside in the internal network... today's network designs take that into account
* Stateful device in the data path, problem arises in case of the state information loss (e.g. NAT device reboot)
* Problematic usage with asymmetric routing (e.g. the network connected to the outside world by more than 1 router), the incoming traffic may return through the other router than the corresponding outgoing traffic

#### Security and err control
Sliding Window – Basic Principle: The transmitter may send multiple frames without waiting for an ACK; the maximum number is given by the sending window size. A separate timeout timer is started after transmission of every frame. A frame is maintained in the sending window until it is acknowledged; if a timeout expires, the frame is retransmitted.

The receiver sends ACK after each successfully received frame. In case of reception of an erroneous frame, the receiver sends NAK or silently discards it, causing the transmitter's timeout to expire. A transmitter can discard the "oldest" frame from the sending window after it is acknowledged, and shift the window – i.e. accept another frame for transmission from the upper layer.

**Buffers in Sliding Window:** <br />
Sending Window maintains the frames that were transmitted but not yet acknowledged; they might have been potentially lost and thus have to be retransmitted in case of timeout expiration. Receiving Window maintains the received frames that could not be passed to the upper layer because previous packet(s) of the sequence are still missing. Both windows "slide" over a set of sequence numbers. <br />
![image](https://hackmd.io/_uploads/BJrgvXJlMx.png) <br />
![image](https://hackmd.io/_uploads/r1pxP71lGl.png) <br />
![image](https://hackmd.io/_uploads/S1vWPX1xzl.png) <br />
![image](https://hackmd.io/_uploads/SJhbwm1xMe.png) <br />
![image](https://hackmd.io/_uploads/BJQfw71eGe.png) <br />
WIP

### 1.7) Databáze
##### DB_START
DB systémy neboli Systémy pro Řízení Báze Dat - SŘBD jsou: <br />
* masivní
* perzistentní
* bezpečné
* více uživatelksé
* pohodlné
* efektivní
* spolehlivé
Jedná se o aplikaci nabízející rozhrání pro vytvoření databáze a komunikaci s ní. Databáze sama o sobě je množina vzájemně propojených dat uloženy v nějakém DB systému. <br />
[Množiny matika](#####MNOZINY) <br />

Typické DB modely tvořené při analýze: <br />
1. Datový model neboli DB schéma, (např. relační datový model) je popis DB definované pro konkrétní DB systém <br />
2. Konceptuální neboli logický model je popis struktury DB, jenž nezohlednuje konkrétní DB systém <br />
![image](https://hackmd.io/_uploads/BkM9ci21fx.png) <br />

**Role lidí věnující se SŘBD:**
* Aplikační programátor - programuje aplikační úlohy nad databázemi
* Návrhář databáze - stanoví schéma databáze
* Správce databáze - administrátor databáze a databázového systému; udržuje databázový systém v kondici a dostupnou, přideluje přístupová práva k datům, a řeší případné výpadky.
* Programátor databázových systémů - často velké týmy lidí

**ORSŘBD** <br />
![image](https://hackmd.io/_uploads/BJRboMklMg.png) <br />
![image](https://hackmd.io/_uploads/HJJ7ozJxGe.png) <br />
![image](https://hackmd.io/_uploads/SJqXoGygMg.png) <br />
![image](https://hackmd.io/_uploads/SJgEoM1lze.png) <br />
WIP skok na OOP <br />
![image](https://hackmd.io/_uploads/rJZIszkxfx.png) <br />
![image](https://hackmd.io/_uploads/HJ7wjGkeGe.png) <br />
![image](https://hackmd.io/_uploads/rkGOsfJefg.png) <br />
SQL Server i Oracle obsahují koncept pomocných tabulek – global/local temporary table. <br />

WIP skok na architekturu, ORM atd. <br />
[Skip na architektury do hloubky SWI](#####ARCHIT) <br />
[Skip na architektury do hloubky V RAMCI DB!!!](#####DB_IS_ARCHIT) <br />
[ORM jump](#####ORM) <br />

* Tabulky nejsou persistentní, většinou jsou platné jen v rámci aktuálního přihlášení (session)/bloku apod.
* S daty pracujeme pomocí SQL.
* Používáme je pro nějakou dočasnou, na zdroje náročnou akci, jsou rychlejší.
* Jedná se tedy o alternativu ke kolekcím.

Globální/lokální pomocné tabulky, Oracle <br />
Oracle:
* global temporary table:
  data jsou automaticky mazána na konci transakce/session,
  definice tabulky je ale součástí systémového katalogu
  CREATE GLOBAL TEMPORARY TABLE ...
* local temporary table:
  data i tabulka jsou automaticky mazány na konci transakce/session
  CREATE PRIVATE TEMPORARY TABLE ora$ptt_<name> ...
* Použití v proceduře, např. místo kolekcí, je poměrně komplikované:
  buď musíme pomocnou tabulku vytvořit před první kompilací
  nebo musíme použít dynamické SQL.

Globální/lokální pomocné tabulky, SQL Server <br />
SQL Server:
* local temporary table:
  viditelná v rámci session,
  název začíná prefixem #
* global temporary table:
  viditelná také pro procedury,
  název začíná prefixem ##
* table variables:
  platné v rámci procedury,
  název začíná prefixem @
* persistent temporary tables:
  název začíná prefixem TempDB

WIP skok na POS bezpečnost

**Datový model:**
Data uspořádana či strukturována mnoha způsoby:
* Relační model, čiže množina záznamů
* Semistruktur. model jako XML, JSON nebo BSON
* Graf - RDF
* Ciste nestruktorovane data <br />
![image](https://hackmd.io/_uploads/B1efsj3kfl.png) <br />

Schéma popisuje strukturu DB a data jsou konkrétní záznamy odpovídající této struktuře. Podobné jako třída vs objekt, či datový typ vs proměnná. Části relačního datového modelu:
* Struktura - definice relací a jejich obsahů
* Integrita - obsah DB musí splnit podmínky
* Operace - jak můžeme přistupovat k a manipulovat data
##### SCHEMA_DB
[Relace once more](#####RELACE) <br />
WIP LINK na OOP <br />

V kontextu DB je relace: <br />
![image](https://hackmd.io/_uploads/S1DN2ohJfl.png) <br />
Relační DB je množina relací, kdežto schéma relační DB je množina relačních schémat.

**Integritní omezení (I/O)**
Jedná se o podmínky, které definují požadované vlastnosti jednotlivých atrib. Konzistení databáze znamená to, že všechny její relace splní IO. Příkladem IO: "Muze nebo nemuze atribut nabyvat hodnoty NULL?", "Splnuje hodnota datovy typ a pozadovany obsah atrib.?"

Btw, o NULL reprezentujícím missing data můžem rozhodovat, zda atribut může mít null value nebo ne, když tvoříme table. Primární klíče jsou jediné atributy, co nesmí mít NULL nikdy: Primární klíč - jednoznacně identifikuje řádek tabulky. Může jít o jeden atribut, ale může být tvořen i více atributy.

Cizí klíč - reprezentuje vazbu mezi relacemi. Cizí klíč se třeba odvíjí od primárního klíče nějaké tabulky, na kterou se odkazuje. Proto v tomto případě bude výhodnější vytvořit umělý primární klíč ID pro oddělení. <br />
Referencní integrita - hodnota cizího klíče v záznamu musí existovat v atributu tabulky na kterou se cizí klíč odkazuje. Problém při škálování distribuované databáze.

**Dotazování relačních DB:**
##### DOTAZ_RELAC
![image](https://hackmd.io/_uploads/r1U01nnkGg.png) <br />
![image](https://hackmd.io/_uploads/ry-Jen2yMe.png) <br />
![image](https://hackmd.io/_uploads/SyZgxn3kzx.png) <br />
![image](https://hackmd.io/_uploads/HJB-ln2Jfg.png) <br />
![image](https://hackmd.io/_uploads/rkQBx2hyfg.png) <br />
[Odkaz na kartéz. součin jako vyjímka](#####KARTEZ) <br />
![image](https://hackmd.io/_uploads/ByyIxnhyfx.png) <br />
![image](https://hackmd.io/_uploads/rkywg3nyze.png) <br />

**Konceptuální model:**
![image](https://hackmd.io/_uploads/SyZ41n2kMl.png) <br />
Součástí SWI části v oblasti DBs... <br />
[Start SWI](#####SWI_START) <br />
4 kroky při DB developmentu: <br />
1. Psaná specifikace tásku, který nefejkujeme:speaking_head_in_silhouette:
2. Konceptuální modelování, tj. logický popis DB
3. DB schema design, tedy relační datový model
4. Fyzický design neboli konkrétní implementace data files, CREATE TABLE, CREATE INDEX, apod.

Task specifikace odpovídá na otázky jako proč, pro koho, kdo (role users, NENI USER ANI ADMIN), inputy (entity, ktere ukladame v systeu), outputy (nejdulezitejsi pohledy), netrivialni funkce, historie.

Konceptuální modelování je proces developování popisu systému, který se pak následně použije při designu a implementaci actual appky. Je nezávislý na DB a definuje restrikce na datech.

**Lineární notace:**
Student(stID, name, birth_year)
Subject(suID, name, study_year)
* Entity type
* Attribute
* Key
* Entity – object of a reality (one instance of entity type)

Vztah je popis vztahu mezi typy entit (2 a víc, někdy vztah sám se sebou), v rámci lineární notace:<br />
RELATIONSHIP(EntityType1,..., EntityTypen) <br />

**Vztah s atributy:** <br />
STUDIES(Student, Subject, gained_points) <br />

Kardinalita vztahu, neboli distinkce vztahu podle toho, kolik entit vstupuje do toho vztahu, binární: 1:1, 1:N, M:N. <br />
Pak máme Mandatory relationship, where each entity has to have a relationship and an obligatory relationship - there can be entities without relationship.

E-R digram (ERD) je grafická reprezentace konceptuálního modelu, neexistuje standard, ale třeba kardinalita je často zobrazena jako číslo u nožičky. <br />
![image](https://hackmd.io/_uploads/Hy6hp33JMx.png) <br />
![image](https://hackmd.io/_uploads/Hk9J0hhkfx.png) <br />
![image](https://hackmd.io/_uploads/rkOGRn21zx.png) <br />
U relačního data modelu DB vždy v designu includujeme cizí klíče v modelu a dekompozitujeme M:N vztahy via spojovací tabulky. Taky přidáme info o data types, NULL / NOT NULL hodnotách. We should always ask ourselves whether the 1:1 relationship is necessary. Sometimes we can simply merge the tables into one. Foreign keys related to the 1:1 relationship can be placed on both sides. It increases redundancy, nevertheless, it may be easier to check the consistency. <br />
![image](https://hackmd.io/_uploads/ry6aChnyzx.png) <br />
![image](https://hackmd.io/_uploads/BJRAR221Mg.png) <br />
**Historické data! There are basically two ways how to solve it:** <br />
1. We never update values like price but we insert new records. <br />
2. We can add price into M:N relationship. <br />
Dvojka is a much better solution in a case of frequent price updates... <br />
![image](https://hackmd.io/_uploads/HklXJT3Jzl.png) <br />
![image](https://hackmd.io/_uploads/rykK162JGl.png) <br />
![image](https://hackmd.io/_uploads/Sk0Yk6nJzg.png) <br />
WIP skok na grafy v DIM kvuli labeled edges <br />
![image](https://hackmd.io/_uploads/rya5J6hyfl.png) <br />
![image](https://hackmd.io/_uploads/ryBRJa2kfl.png) <br />
![image](https://hackmd.io/_uploads/Sk_a163yMg.png) <br />
![image](https://hackmd.io/_uploads/HJEyep3kzl.png) <br />
![image](https://hackmd.io/_uploads/HkCkgankMl.png) <br />
![image](https://hackmd.io/_uploads/S11XlThJfe.png) <br />
![image](https://hackmd.io/_uploads/SJnQxT3yGe.png) <br />
![image](https://hackmd.io/_uploads/ByyHgThyzx.png) <br />
![image](https://hackmd.io/_uploads/ryQYean1zg.png) <br />
![image](https://hackmd.io/_uploads/HyYcgpnyMx.png) <br />
![image](https://hackmd.io/_uploads/Bk7sxa2yGg.png) <br />
![image](https://hackmd.io/_uploads/rJiieT3kGx.png) <br />
![image](https://hackmd.io/_uploads/HyH2xp2yzg.png) <br />
![image](https://hackmd.io/_uploads/H1CngTn1Gg.png) <br />

**DB scheme design:** <br />
![image](https://hackmd.io/_uploads/HJCzD1aJfl.png) <br />
![image](https://hackmd.io/_uploads/BkTmv1TJzx.png) <br />
![image](https://hackmd.io/_uploads/ByAHDy6JGx.png) <br />
![image](https://hackmd.io/_uploads/Bk1wDJpJMe.png) <br />
![image](https://hackmd.io/_uploads/Hk2uv1pyzl.png) <br />
![image](https://hackmd.io/_uploads/H1aKPJ6JMl.png) <br />
![image](https://hackmd.io/_uploads/Bki9wkpkze.png) <br />
![image](https://hackmd.io/_uploads/SJmswk61fx.png) <br />
**Minimal Non-redundant FDs** <br />
The goal is: <br />
to find a minimal set of totally non-trivial and non-redundant FDs such that all FDs for the relational scheme are implied by this set. When determining a set of FDs for some scheme, we usually intuitively create a set satisfying this condition. In the following slides, we introduce a technique how to find this set. <br />
![image](https://hackmd.io/_uploads/BkKeuyTkGe.png) <br />
![image](https://hackmd.io/_uploads/rkkMuy61zx.png) <br />
![image](https://hackmd.io/_uploads/SyG7dJ6Jzx.png) <br />
![image](https://hackmd.io/_uploads/r11VO1akfl.png) <br />

[Axiomy matematika/logika](#####AXIOMY) <br />
[Začátek VL k matice](#####LOGIKA_START) <br />
[Výroková logika a predikátovka](#####LOGIKA) <br />
##### DATABAZE_TEORIE_NORMALOVE_FORMY
![image](https://hackmd.io/_uploads/BkAj_yaJzx.png) <br />
![image](https://hackmd.io/_uploads/HyK3Oy61Ml.png) <br />
![image](https://hackmd.io/_uploads/r1Gau1TkMe.png) <br />
![image](https://hackmd.io/_uploads/ry6T_kakGl.png) <br />
We need to decompose the relation in order to have a relation in 2NF. <br />
![image](https://hackmd.io/_uploads/rk7kFkTJfg.png) <br />
![image](https://hackmd.io/_uploads/SJ1eFkayMg.png) <br />
![image](https://hackmd.io/_uploads/r1Fltk6Jzx.png) <br />
![image](https://hackmd.io/_uploads/Hy97tkpkzg.png) <br />
![image](https://hackmd.io/_uploads/rJGVtka1fx.png) <br />
![image](https://hackmd.io/_uploads/rk2VYJpkMx.png) <br />
![image](https://hackmd.io/_uploads/HyqrK161ze.png) <br />
![image](https://hackmd.io/_uploads/ByxwtJ6Jfg.png) <br />
![image](https://hackmd.io/_uploads/SJ1_FkTyGl.png) <br />

[Hop na dotazování relač. DB](#####DOTAZ_RELAC) <br />
![image](https://hackmd.io/_uploads/ByKwennyze.png) <br />
![image](https://hackmd.io/_uploads/H1Pqx23kze.png) <br />
![image](https://hackmd.io/_uploads/ByVig231Mx.png) <br />
![image](https://hackmd.io/_uploads/Sk22g23yzl.png) <br />
![image](https://hackmd.io/_uploads/ByV6ehh1fe.png) <br />
![image](https://hackmd.io/_uploads/rJHCghnyGx.png) <br />
![image](https://hackmd.io/_uploads/SyfJ-23kGx.png) <br />
![image](https://hackmd.io/_uploads/SJZgb33JGl.png) <br />
![image](https://hackmd.io/_uploads/ry9Wbn31zl.png) <br />
![image](https://hackmd.io/_uploads/SJHM-3hJfg.png) <br />
![image](https://hackmd.io/_uploads/Hy7mbn3JMl.png) <br />
![image](https://hackmd.io/_uploads/SynXb32kfe.png) <br />
![image](https://hackmd.io/_uploads/BJKSWh2Jfg.png) <br />
![image](https://hackmd.io/_uploads/SJEIWh2kzl.png) <br />
![image](https://hackmd.io/_uploads/HJBt-n3yGe.png) <br />
![image](https://hackmd.io/_uploads/SJg5bn3kGx.png) <br />
![image](https://hackmd.io/_uploads/Sk2q-hn1Mg.png) <br />
![image](https://hackmd.io/_uploads/B1B-8nnyfg.png) <br />
There are several ways how to express a semi join in SQL:
* IN subquery
* EXISTS subquery <br />
![image](https://hackmd.io/_uploads/r1gQUnh1Ge.png) <br />
![image](https://hackmd.io/_uploads/rJa7Ihn1Gx.png) <br />
![image](https://hackmd.io/_uploads/HkSV833yMx.png) <br />
![image](https://hackmd.io/_uploads/Skh48n31Gl.png) <br />
![image](https://hackmd.io/_uploads/S1sSUh31ze.png) <br />
![image](https://hackmd.io/_uploads/HJQUU23kGl.png) <br />
![image](https://hackmd.io/_uploads/HyyPIn3JGg.png) <br />
![image](https://hackmd.io/_uploads/SkDwI3hkze.png) <br />
![image](https://hackmd.io/_uploads/SJ8K8n3JGe.png) <br />
![image](https://hackmd.io/_uploads/S1AqLnh1ze.png) <br />
![image](https://hackmd.io/_uploads/SkU3Lh2kfx.png) <br />
![image](https://hackmd.io/_uploads/BkxaUnhyfg.png) <br />
![image](https://hackmd.io/_uploads/HkqgD32yzl.png) <br />
![image](https://hackmd.io/_uploads/rkP-vhhJGe.png) <br />
![image](https://hackmd.io/_uploads/BkLmPhhJGx.png) <br />
![image](https://hackmd.io/_uploads/rk6QDh31zg.png) <br />
![image](https://hackmd.io/_uploads/ryrSPh21zx.png) <br />
CTE may simplify notation and avoid redundancy. However, some database systems evaluate the CTE first and store the result. This may cause problems for certain queries. <br />
![image](https://hackmd.io/_uploads/BkBPvn21Ge.png) <br />
Query plan is a tree where a node is an operator and edge represents a fact that output of one node is input of another node.  <br />
We recognize two major types of plans:
* Logical tree - typically a relational algebra
* Physical (query plan) - specific algorithms <br />
![image](https://hackmd.io/_uploads/r1iqP221fl.png) <br />
![image](https://hackmd.io/_uploads/ryfjPn31Gx.png) <br />

**Agregační funkce**
![image](https://hackmd.io/_uploads/r1vGGh31Ml.png) <br />
GROUP BY defines attributes that specify logical groups in the input relation... <br />
![image](https://hackmd.io/_uploads/rJu27n2JGe.png) <br />
![image](https://hackmd.io/_uploads/rJbzEnn1zl.png) <br />
![image](https://hackmd.io/_uploads/HJiHE32yfg.png) <br />
![image](https://hackmd.io/_uploads/H1Xt423yfl.png) <br />
![image](https://hackmd.io/_uploads/HyiKV22kGe.png) <br />
![image](https://hackmd.io/_uploads/H1BqNn3yzg.png) <br />
![image](https://hackmd.io/_uploads/SynR4nhJGx.png) <br />
Every condition in SQL is evaluated into true, false or unknown. Row is in the result only if the result of the condition is true.  <br />
Examples when a predicate returns unknown:
* attribute = null
* unknown and true
* unknown or false <br />
![image](https://hackmd.io/_uploads/rkhDS33yzl.png) <br />

![image](https://hackmd.io/_uploads/r1lKr32Jzx.png) <br />
![image](https://hackmd.io/_uploads/SknKSh2Jfl.png) <br />
WIP skok na ZDS <br />
![image](https://hackmd.io/_uploads/r1JIbTnyGx.png) <br />
![image](https://hackmd.io/_uploads/rJoF-pn1fg.png) <br />
WIP skok na OSY paging <br />
![image](https://hackmd.io/_uploads/B1ehbp31Ml.png) <br />
![image](https://hackmd.io/_uploads/HySa-a3yzg.png) <br />
![image](https://hackmd.io/_uploads/rJvRWp2yGg.png) <br />
![image](https://hackmd.io/_uploads/rybyfTn1zg.png) <br />
![image](https://hackmd.io/_uploads/HkxdJfTnyGe.png) <br />
![image](https://hackmd.io/_uploads/H1-gMTnkMx.png) <br />
![image](https://hackmd.io/_uploads/ByhgGpnJze.png) <br />
![image](https://hackmd.io/_uploads/SkQ-Mp3kGl.png) <br />
![image](https://hackmd.io/_uploads/SkoMfankMe.png) <br />
![image](https://hackmd.io/_uploads/BJUXGp31fx.png) <br />
![image](https://hackmd.io/_uploads/ry7Efanyzx.png) <br />
![image](https://hackmd.io/_uploads/Bkerzahyfg.png) <br />
![image](https://hackmd.io/_uploads/ryASM6nyGg.png) <br />
![image](https://hackmd.io/_uploads/ryvIz62yze.png) <br />
![image](https://hackmd.io/_uploads/BJyDfTnyzl.png) <br />
![image](https://hackmd.io/_uploads/B1ZuMT21fl.png) <br />
Matcher to hotfix to release to develop to feature to feature <br />
![image](https://hackmd.io/_uploads/ryOKfph1ze.png) <br />

PL/SQL věci: <br />
![image](https://hackmd.io/_uploads/BJr_Bx6kMg.png) <br />
![image](https://hackmd.io/_uploads/H1gVtrlayfg.png) <br />
![image](https://hackmd.io/_uploads/H1f9Sl61fe.png) <br />
WIP odkaz na programko cause datové struktury a vyjímky <br />
![image](https://hackmd.io/_uploads/BJqsHxakfx.png) <br />
![image](https://hackmd.io/_uploads/SJchSl6yMg.png) <br />
![image](https://hackmd.io/_uploads/ryqRrl6yzg.png) <br />
![image](https://hackmd.io/_uploads/S1Y1IxayMl.png) <br />
![image](https://hackmd.io/_uploads/SJEeUlTyzx.png) <br />
![image](https://hackmd.io/_uploads/HkybIl6kfe.png) <br />
![image](https://hackmd.io/_uploads/rk0-Uxakze.png) <br />
![image](https://hackmd.io/_uploads/r1_zIxTkze.png) <br />
PL/SQL umožňuje vytvářet několik typů procedur. V zásadě se liší
především způsobem jakým jsou spouštěny:
* Anonymní procedury
* Pojmenované/uložené procedury (stored procedures)
* Pojmenované/uložené funkce (stored functions)

Anonymní procedury jsou nepojmenované procedury, které nemohou být volány z jiné procedury.
Tyto procedury mohou být uloženy v souboru, nebo přímo zapsány na příkazový řádek, a spouštěny z klienta (např. Oracle SQL Developer).

Anonymní procedury nejsou předkompilovány a mohou být proto pomalejší než pojmenované procedury a funkce. Jinými slovy: jedná se o PL/SQL block. <br />
![image](https://hackmd.io/_uploads/S124IxpJfe.png) <br />
Pojmenované procedury obsahují hlavičku se jménem a parametry procedury. Takovouto proceduru je možné volat z jiných procedur nebo spouštět příkazem EXECUTE (zkráceně EXEC).
Na rozdíl od anonymních procedur jsou pojmenované procedury předkompilovány a uloženy v databázi. <br />
![image](https://hackmd.io/_uploads/ByEDUxTkMe.png) <br />
![image](https://hackmd.io/_uploads/SkCPLeT1Me.png) <br />
![image](https://hackmd.io/_uploads/r1SOIea1Mx.png) <br />
![image](https://hackmd.io/_uploads/HJHtLgTyGx.png) <br />
![image](https://hackmd.io/_uploads/ryTKUxa1Me.png) <br />
![image](https://hackmd.io/_uploads/S1uc8eayzg.png) <br />
![image](https://hackmd.io/_uploads/SycsLepkzl.png) <br />
![image](https://hackmd.io/_uploads/BkN08eTJMx.png) <br />
![image](https://hackmd.io/_uploads/SJ4kveTkGx.png) <br />
![image](https://hackmd.io/_uploads/HyJevgayzl.png) <br />
V PL/SQL můžeme použít několik základních řídících konstrukcí jako je podmínka a cyklus.
Jejich syntaxe se výrazně neliší od podobných konstrukcí v jiných programovacích jazycích.

WIP skok na programko <br />
![image](https://hackmd.io/_uploads/HyxQweaJzg.png) <br />
![image](https://hackmd.io/_uploads/SkUmDgpyMe.png) <br />
![image](https://hackmd.io/_uploads/Bye4veTyfg.png) <br />
![image](https://hackmd.io/_uploads/Byj4vxTJGg.png) <br />
![image](https://hackmd.io/_uploads/SJVHwxT1zg.png) <br />
##### JMENNY
Balíky mají podobnou funkci jako knihovny případně jmenné prostory (namespace) v jiných programovacích jazycích.
Seskupují PL/SQL objekty (funkce, procedury, proměnné, výjimky atd.) do jednoho jmenného prostoru. <br />
[Domény again](#####DOMENY) <br />

Balíky mají hned několik výhod, umožňují:
* Deklarovat proměnné a výjimky která jsou viditelné/platné i mimo proceduru či funkci.
* Vytvořit veřejné a soukromé funkce a procedury. Soukromé funkce a procedury bude možné volat jen z procedur a funkcí uvnitř balíku.
* Vytvořit vlastní jmenný prostor, kde je možné mít libovolná jména PL/SQL objektů.
* Snadnější orientaci v PL/SQL kódu, což je výhodné zejména u větších projektů.

Dvě části balíku: specifikace a tělo: Specifikace balíku představuje veřejnou část, která je dostupná nejen uvnitř balíku. Obsahuje definice veřejných proměnných, výjimek a hlaviček procedur a funkcí. Tělo balíku obsahuje soukromou část balíku a definice procedur a funkcí deklarovaných ve specifikaci balíku. <br />
![image](https://hackmd.io/_uploads/Bk-owlakzx.png) <br />
![image](https://hackmd.io/_uploads/SJB3Dl6kMg.png) <br />
![image](https://hackmd.io/_uploads/H19ADe6yGg.png) <br />
![image](https://hackmd.io/_uploads/Sy-Hue61zx.png) <br />
![image](https://hackmd.io/_uploads/r1L8dgT1Gg.png) <br />
Implicitně běží kód uložených procedur/funkcí/balíčků s právy vlastníka (tedy toho kdo proceduru vytvořil). Tento režim se označuje AUTHID DEFINER.

Aktuální schéma = schéma vlastníka procedury. Druhou možností je, aby kód běžel s právy aktuálního uživatele (tedy ten kdo proceduru spustil).

Volba: AUTHID CURRENT_USER (od Oracle 8i) <br />
Aktuální schéma = schéma aktuálního uživatele. <br />
Všimněte si, že AUTHID CURRENT_USER neřeší problém s bezpečností v proceduře kill_locked_sessions. Procedura musí běžet pod administrátorem (uživatel SYS), aby bylo možné zavolat ALTER SYSTEM KILL SESSION. Nicméně chceme, aby uživatel mohl ukončit jen své procesy. <br />
![image](https://hackmd.io/_uploads/HJmvdxp1fx.png) <br />
V PL/SQL bloku nemůžeme přímo volat všechny dostupné SQL příkazy. Příkazy, které lze volat v PL/SQL přímo, nazýváme statické příkazy PL/SQL. Mezi statické příkazy patří: <br />
SELECT, INSERT, UPDATE, DELETE, MERGE <br />
LOCK TABLE, COMMIT, ROLLBACK, SAVEPOINT, SET <br />
TRANSACTION <br />
Je zřejmé, že mezi příkazy které nemůžeme volat přímo, jsou všechny příkazy JDD (DDL) a příkazy které v době překladu nejsou známy (tedy např. i select pro tabulku jejíž jméno předáváme jako parametr procedury).

Dynamické PL/SQL umožňuje sestavit a volat jakýkoli SQL příkaz (na který má uživatel právo) za běhu aplikace. <br />
Nevýhodou je, že nelze jednoduše ověřit syntaktickou správnost (správné datové typy, počet parametrů atd.). Navíc se vystavujeme nebezpečí SQL injection!

Dynamické PL/SQL spouštíme příkazem EXECUTE IMMEDIATE.
Upozornění: Dynamické PL/SQL používáme jen v případě,
kdy není možné použít statické PL/SQL! <br />
![image](https://hackmd.io/_uploads/ByEtOl61Ge.png) <br />
![image](https://hackmd.io/_uploads/Syjt_ea1Mx.png) <br />
WIP skok na vázané proměnné, které dám někde v logice asi
TODO alert na tuto vazbu <br />
![image](https://hackmd.io/_uploads/SyVcYxTkMl.png) <br />
![image](https://hackmd.io/_uploads/SJ9pYe6yMg.png) <br />
WIP skok na programka <br />
![image](https://hackmd.io/_uploads/HJJk9eTkzl.png) <br />
![image](https://hackmd.io/_uploads/B1015l61Gl.png) <br />
![image](https://hackmd.io/_uploads/rJFx9gTyMe.png) <br />
![image](https://hackmd.io/_uploads/S1mb5lakGl.png) <br />
Má smysl psát logiku aplikace v PL/SQL / T-SQL2? Rozhodně ano! Jsme nejblíž databázi, na straně klienta efektivitu nemůže ovlivnit v takové míře jako v PL/SQL.

Postup: <br />
Co lze napsat v SQL, napište v SQL. <br />
Co nelze napsat v SQL, napište ve statickém PL/SQL. <br />
Co nelze napsat ve statickém PL/SQL, napište v dynamickém PL/SQL. <br />
Co nelze napsat v PL/SQL, napište v klientské aplikaci. <br />

![image](https://hackmd.io/_uploads/BJ9mnf1xMl.png) <br />
###### TRANSAKCE
Transakce je logická (nedělitelná, atomická) jednotka práce s databází, obsahující více databázových operací (select, update, delete, insert), která začíná operací BEGIN TRANSACTION a končí operacemi COMMIT nebo ROLLBACK.

* COMMIT – úspěšné ukončení transakce.
  Transakce byla úspěšně dokončena, databáze je nyní v korektním stavu,
  a všechny aktualizace (update/delete/insert) transakce jsou trvale
  uloženy v databázi (jsou potvrzeny).
* ROLLBACK – neúspěšné provedení transakce.
  Jedna z operací transakce nebyla korektně ukončena,
  všechny aktualizace provedené transakcí musí být zrušeny.
* Transakce je atomická ⇒ Transakce se nemohou zanořovat.

Korektní stav databáze, potvrzovací bod ...
* Úkolem transakce je převést korektní stav databáze na jiný
  korektní stav, po dílčích operacích transakce, může být databáze
  v nekorektním stavu.
* Operace COMMIT zavádí tzv. potvrzovací bod
  (angl. commit point), ve smyslu bodu v čase,
  ve kterém je databáze v korektním stavu.
* ROLLBACK vrací databázi do stavu, ve kterém byla při vykonání
  BEGIN TRANSACTION, vrací tedy databázi k předchozímu
  potvrzovacímu bodu (tedy do korektního stavu).

[Skok na ACID jelikož je relevantní právě pro transakce](######ACID) <br />

**Klasifikace chyb při provádění transakcí:** <br />
Lokální chyby: chyba v dotazu, přetečení hodnoty atributu.

Globální chyby: <br />
* Chyby systémové (soft crash): výpadek proudu, pád operačního systému nebo databázového systému,
* Chyby disku (hard crash).

**Log soubor** <br />
Jak je možné zrušit aktualizace transakce? Programátor připojením k DBS nepracuje přímo se soubory databáze. <br />
Pro podporu transakcí používá DBS soubor log (journal), uložený na disku, kde jsou zaznamenány detaily o všech operacích provedených transakcí. Na základě těchto záznamů je možné, například, zrušit operaci transakce pomocí ROLLBACK.

Korektní vs konzistentní stav databáze? <br />
V některých případech se v souvislosti s transakcemi mluví o konzistentním stavu databáze. Pojem konzistentní databáze znamená přesně to, že v databázi neexistují žádné výjimky z daných integritních omezení. <br />
V příkladu s převodem peněz mezi účty nejsme ale schopni žádné integritní omezení definovat. Proto je tedy přesnější mluvit o korektním stavu databáze, tedy stavu odpovídajícímu výsledku operace v reálném světě (převod částky z účtu na účet). <br />
![image](https://hackmd.io/_uploads/SyK7TG1lzx.png) <br />
![image](https://hackmd.io/_uploads/H1-BTzygGl.png) <br />
![image](https://hackmd.io/_uploads/By9B6fJgGg.png) <br />
![image](https://hackmd.io/_uploads/B1fI6fyeze.png) <br />
![image](https://hackmd.io/_uploads/rkF8aGJeMg.png) <br />
![image](https://hackmd.io/_uploads/HJyPpzJlzg.png) <br />
![image](https://hackmd.io/_uploads/BkHwaM1lfg.png) <br />
![image](https://hackmd.io/_uploads/By1OTzJeMx.png) <br />
Transakci jsme dosud prezentovali jako atomickou (nedělitelnou) databázovou operaci.

Koncept záchranných bodů (savepoints), zavedený v SQL99, umožňuje transakci rozdělit na menší části. V případě operace ROLLBACK nedochází ke zrušení celé transakce, ale k návratu na záchranný bod. Záchranný bod ale není ekvivalentní potvrzení změn příkazem COMMIT.

Transakce v SQL následují teorii popsanou v předchozích kapitolách. Všechny SQL příkazy jsou atomické. <br />
Operace BEGIN TRANSACTION se v SQL provede příkazem START TRANSACTION, operace COMMIT příkazem COMMIT WORK a operace ROLLBACK příkazem ROLLBACK WORK. <br />
Při práci s databázovým systémem je třeba dát pozor zejména na AUTOCOMMIT – pokud je nastaveno AUTOCOMMIT ON, operace ROLLBACK nedává smysl. <br />
![image](https://hackmd.io/_uploads/HJNtpzJgze.png) <br />
![image](https://hackmd.io/_uploads/ryFYTfJlzl.png) <br />

TODO undo redo atd tabulka

T-SQL: <br />
![image](https://hackmd.io/_uploads/B1BECGyeMx.png) <br />
![image](https://hackmd.io/_uploads/rkGH0M1eGg.png) <br />
![image](https://hackmd.io/_uploads/rJL_Af1xzg.png) <br />
![image](https://hackmd.io/_uploads/SygYRMJeMl.png) <br />
![image](https://hackmd.io/_uploads/ByFKAM1lMg.png) <br />
![image](https://hackmd.io/_uploads/HyWc0fJeMg.png) <br />
![image](https://hackmd.io/_uploads/B1dq0GJeze.png) <br />
![image](https://hackmd.io/_uploads/Bk4sRf1lfx.png) <br />
![image](https://hackmd.io/_uploads/ryAj0fklzl.png) <br />

#### Jiné DB systémy
Open source jako Postgre nebo MySQL, komerční Oracle, SQL Server.

Výhody relačního mimo jiné referenční integrita skrze primary a foreign key + integritní omezení, také příjemné rozhraní ve formě SQL. Ostatní výhody však i v jiných systémech:
* Transakční integrita (při řízení souběhu operací)
* Persistence
* Řízení přístupu
* Zotavení po chybě
* Spolehlivost (dostupnost)

Aspekty výběru databázového systému:
* Cílová architektura
* Typ vytížení
* Datový model
* Dostupnost
* Hlavní pamet’
* DBaaS <br />
![image](https://hackmd.io/_uploads/SJMAsyT1zl.png) <br />

Architektura IS: <br />
[Architektura v SWI a obecně relevantní info pro DB systémy taky](######ARCHIT) <br />
S databází obv nepracují users přímo přes klienta typu SQL Server Management Studio, ale pracují s appkou, která si komunikaci s DB nějak zprostředkovává a interpretuje, třeba developed v jazyce Java, .NET. Rozlišuje 2 typy IS:
* Web app - appka ve web. prohlížeči
* Desktop app - appka přimo v OS, oknová

![image](https://hackmd.io/_uploads/r1ev2kpyfe.png) <br />
Sloupcové databáze... <br />
Databáze pro datové sklady bývají casto odlišně koncipovány (sloupcove orientované databáze). Vedle sebe jsou (v paměti i na disku) uloženy hodnoty ze stejného sloupce. Rychlé vykonání agregačních funkcí nad mnoha řádky. Komprese sloupce. Vertica, MonetDB, Netezza, SQL Server, Oracle, ...

Datový model: <br />
Rozdelení dle použitého datového modelu a podporovaných operací: <br />
* Relační databáze (SQL)
* Key-value / Dokumentové
* XML databáze (XPath, XQuery)
* Prostorové databáze (rozsahové dotazy)
* Grafové databáze (kNN, hledání nejbližších sousedů)

Důležité jsou zejména podporované operace. Lehce můžeme například prostorová data uložit v relační tabulce, ale vykonání mnoha typických operací pro prostorová data bude v SQL dost komplikované a neefektivní.

Key-value Databázový systém je založen na nejjednodušším datovém modelu: <br />
Základním elementem databázového systému je (klíč, hodnota). Podporováno je vyhledání/aktualizace/mazání hodnoty na základe klíče. Key-value se vetšinou liší celou řadou aspektů:
* Podporované datové typy
* Škálovatelností
* Podporou datových struktur
* Podporované operace na klíčích/hodnotách  <br />
Redis, Memcached, ..., RocksDB, LMDB

Datový model Dokumentové DB: <br />
Jedná se také o určitý typ key-value. Nicméně hodnota je většinou JSON (popřípadě jiný semistrukturovaný formát).  <br />
Jedna dvojice (klíč, JSON) je nazývána dokument. Dokumenty jsou organizovány do kolekcí, což kromě zpřehlednení (kolekce analogii tabulky) obvykle přináší i výkonové zlepšení. JSON je schema-less. Možnost indexování hodnot v JSON (tzn. vyhledáváme dokumenty nejen dle klíče).  <br />
MongoDB, CouchBase

Datový model XML databáze: <br />
V XML databázích opet najdeme určité rysy předchozího datového modelu. Nicméně tady není žádný klíč pro přístup k semistrukturovaným datům (t.j. k XML). Mále kolekci XML a propráci využíváme jazyky jako je XQuery.  <br />
XBase, Saxon

Škálovatelnost: <br />
V současné době se stávají velmi aktuálními databáze, které se zameřují na:
* Vysokou dostupnost - data jsou replikována i v několika datových centrech, aby se pčedešlo nedostupnosti.
* Škálovatelnost - možnost bezpracně nastavovat počet databázových serverů úmerné zátěži. Využívá se distribuce dat na více serverů, které spolu komunikují pouze po síti (nemají žádné sdílené prostředky). Dostupnost a zejména škálovatelnost má v relačních databázích své limity. Z tohoto důvodu vznikla celá skupina databází, která se na tyto parametry zameřuje (NoSQL, NewSQL)

Scale up... Také se nazývá vertikální škálování (Scale up)... znamená možnost navyšování výkonu přidáváním jader procesoru na uzlu. Tzn. paralelizace v rámci jednoho uzlu. Toto již dnes nabízí celá řada databázových systémů (např. LevelDB)

Scale out... Také se nazývá horizontální škálování (Scale out)... znamená možnost navyšování výkonu přidáváním nových serverů (uzlů). Scale out může být problémem pro relační databáze. Scale out je limitováno tzv. CAP teorémem:

Scale out - CAP teorém  <br />
Máme tři vlastnosti systému, které ovlivnujeme, když provádíme scale out: <br />
* Konzistence dat - všichni vidí stejná data naposledy potvrzená data.
* Dostupnost - každý požadavek dostane nějakou konzistentní odpoved (nemusí jít o poslední konzistetní stav).
* Tolerance k výpadkům - systém funguje i při přerušení spojení mezi uzly. <br />
Teorém tvrdí, že není možné dosáhnout všech tří vlastností at once...
 
Scale out - NoSQL <br />
Relační databáze jsou založeny konzistenci, takže trpí bud dostupnost, nebo tolerance k výpadkům v sítí. NoSQL se nicméne vzdává některých požadavků na konzistenci. Mnoho aplikací nevyžaduje, aby všichni viděli poslední konzistentní stav (počet shlédnutí, atp.). Příznačné je, že nepoužívají SQL ani relační model.  <br />
MongoDB, Redis, Voldemort, atp.

Scale out - NewSQL databázové systémy se snaží zvýšit požadavek na konzistenci dat na možné maximum při zachování relačního datového modelu SQL. Obvykle se snaží i o zachování maxima z požadavků ACID (ne vše je možné). <br />
VoltDB, MemSQL, ...

###### ACID
A - atomičnost (atomicity) – transakce musí být atomická: jsou provedeny všechny operace transakce nebo žádná.
C - korektnost (correctness) – transakce převádí korektní stav databáze do jiného korektního stavu databáze; mezi začátkem a koncem transakce nemusí být databáze v korektním stavu.
I - izolovanost (isolation) – transakce jsou navzájem izolovány: změny provedené jednou transakcí jsou pro ostatní transakce viditelné až po provedení COMMIT.
D - trvalost (durability) – jakmile je transakce potvrzena, změny v databázi se stávají trvalými i po globální chybě.

Transakce umožňuje provést ROLLBACK, pokud není vykonána celá (A). <br />
Pokud běží v DBS více transakcí, jsou navzájem izolovány, tj neovlivňují své výsledky (I). <br />
Umožňuje zotavení databáze v případě globální chyby (např. při výpadku serveru) (D). <br />

[Zpátky na transakce](######TRANSAKCE) <br />

TODO race conditions, ...

In-memory: <br />
Rozdělení dle požadavků na pamet. Tradiční databázové systémy byly navrženy s ohledem na klasickou architekturu Disk-Pamet-CPU. Nicméně dnes cena pamětí neustále klesá, když není AI krize, nezapomenout poděkovat miliardářovi dneska... Teda ehm, již nejsou vyjímkou servery se stovkami GB  <br />
![image](https://hackmd.io/_uploads/B1-3ge61Ml.png) <br />
![image](https://hackmd.io/_uploads/BkP2elTyGe.png) <br />

![image](https://hackmd.io/_uploads/HkQg0MyeMe.png) <br />
![image](https://hackmd.io/_uploads/ryl-0MJeGx.png) <br />

Funkční analýza <br />
Typy funkcí jsou: CRUD operace nad jednou tabulkou, komplikovaný dotaz a transakce.

Funkční analýza je soupis funkcí datové vrstvy – CRUD operace nepopisujeme, maximálně je uvedeme v seznamu funkcí; komplikované dotazy a transakce popisujeme, přičemž transakce nejčastěji minispecifikací (pseudoalgoritmus doplněný o databázové operace).

Důležité je vyvážit úplnost (implementátor by měl být schopen naimplementovat funkce jen čtením funkční analýzy) a přesnost (nepopisujeme triviální funkce, např. CRUD operace). Přílišná analýza vede k tzv. analysis-paralysis, kdy je analýza delší než samotná implementace.

Je funkční analýza zbytečná? <br />
Nezkušený analytik by mohl namítnout, že funkční analýza je zbytečná, protože počet funkcí je roven 5 (insert, update, delete, selectOne, selectAll) × počet tabulek. Takový IS by byl prakticky nepoužitelný z pohledu formulářů UI a v některých případech dokonce nekorektní, pokud potřebujeme transakce. Otázkou tedy je, jak zjistit, jaké funkce má mít navrhovaný informační systém.

Návrh formuláře  <br />
Funkční analýza často začíná návrhem formulářů, protože formulář umožňuje pochopit, jaké funkce potřebujeme, a analytik může při jeho tvorbě spolupracovat se zadavatelem. Triviální formuláře, například obsahující pouze 5 CRUD operací pro číselník, nepopisujeme. Forma formuláře není důležitá, lze ho kreslit rukou, návrh ale musí být jasný. Z pohledu funkcí rozlišujeme tyto typy komponent UI (ignorujeme statické texty) – komponenta zobrazuje výsledek funkce, předává parametry funkci, nebo spouští vytváření jiného formuláře.

**ORM, etc.**
##### ORM
Objektově relační mapování (ORM) <br />
Datová vrstva je vrstva mezi databází a programem (informačním systémem). ORM je jedna z možností její implementace – zpřístupňuje relační (či objektově-relační) data pro objektové prostředí (např. C# nebo Java). Vlastnostmi ORM jsou práce s objektovým modelem, rychlejší vytváření aplikací za cenu menšího výkonu a přenositelnost mezi různými DBS oproti využívání specifických vlastností DBS (datové typy, funkce, bezpečnost atd.).

ORM nástroje a rámce <br />
Techniky implementace ORM jsou tři: ORM rámce (Hibernate, JPA, Entity Framework), ORM mikrorámce (Dapper, MyBatis) a vlastní implementace.

V ORM rámcích musíme definovat mapování konfigurační souborem nebo anotacemi ve zdrojovém kódu, pomocí API rámce pak pracujeme s databází.

Některé ORM (Hibernate, LINQ) se navíc pokouší vytvořit vrstvu nezávislosti na konkrétní databázi – je ale otázkou, zda má smysl používat rámec, který ušetří práci, ale může degradovat výkon, když se některé DBS vyvíjejí desítky let.

Vlastní ORM vs ORM rámce <br />
Výhodami ORM rámců jsou rychlejší tvorba aplikace a jednoduchá změna používaného SŘBD. Nevýhodami jsou pouze částečná kontrola nad generovanými SQL příkazy a často nižší výkon.

Mikrorámce a rámce specifické pro konkrétní SŘBD problémy s výkonem spíše nemají (LINQ pro SQL Server, ADF pro Oracle). Při opakovaném spouštění ORM rámce ukládají data do interní cache, ale musí řešit aktualizace a transakce mimo DBS. Ani v takovém případě nejsou oba rámce lepší než vlastní ORM. Rámce pro ORM nicméně nabízejí implementaci některých částí ORM a zrychlují vývoj – z pohledu výkonu je většinou lepší volbou mikrorámec ORM.

Úkolem datové vrstvy je poskytnout maximální propustnost operací nad databází. Příklad nevhodného přístupu: dotaz počítající celkovou sumu převáděných částek tabulky Prevod přes SELECT * FROM Prevod načte milion záznamů, vytvoří kolekci milionu objektů v paměti a teprve pak spočítá součet – správně se má použít agregační funkce přímo v SQL dotazu.

Návrh ORM <br />
Používá se jednoduché mapování dvou typů tříd.

První typ – aplikační objekt / doménový objekt / DTO (Data Transfer Object) – reprezentuje jeden entitní typ; jeden objekt reprezentuje jeden záznam tabulky, je součástí aplikační vrstvy. Například třída Person pro tabulku Person. Obecně lze mapovat jeden entitní typ na více doménových objektů nebo více entitních typů na jeden doménový objekt.

Druhý typ – DAO (Data Access Object) – reprezentuje implementaci funkcí (většinou) nad jednou tabulkou, je součástí datové vrstvy. Jedna DAO třída může zahrnovat operace pro více tabulek (tiskové sestavy, transakce). Například třída PersonDao se statickými metodami Select, Insert atd. pro tabulku Person; funkce pracující s více tabulkami se umísťují do společných tříd jako QueriesDao nebo TransactionsDao. Dále existují pomocné třídy pro přístup k databázi, správu připojení a transakcí.

Transakce z funkční analýzy se implementují buď jako uložené procedury volané z metody DAO třídy, nebo jako metody v aplikaci (i s potřebnými DAO a DTO třídami). Je nutné použít parametrizované operace, zapouzdření kódu do DTO a DAO a API pro přístup k datům jako ADO.NET nebo JDBC. <br />
![image](https://hackmd.io/_uploads/S1gc1m1gGx.png) <br />
WIP skok na programko java a csharp <br />
![image](https://hackmd.io/_uploads/ryPoJmJezg.png) <br />
![image](https://hackmd.io/_uploads/ByRoJXkxfl.png) <br />
![image](https://hackmd.io/_uploads/BkH3J7keGg.png) <br />
![image](https://hackmd.io/_uploads/Bk32yQ1efg.png) <br />
![image](https://hackmd.io/_uploads/r1Up1X1xzx.png) <br />
![image](https://hackmd.io/_uploads/S10pkmJezx.png) <br />
![image](https://hackmd.io/_uploads/Byr0yXkeMx.png) <br />

### 1.8) SWI čistě
Tady jsou na jistotu pouze věci z předmětů SWI a VIS, zlinkované pretty much jen na části textu, které se zabývají OOPečkem, nebo ukazují vzory. Referuju hodně na mou reálnou praxi.

#### Co je SWI, modely, ULM a UC, objetky, doména
**SW** je **program + dokumentace + operační procedury**. Asociace s **požadavky (requirements)**, design **modely** a user **manuály**. Pro konkrétního zákazníka nebo general market. Unlike CS jde o praktické aspekty vývoje. Chceme **quality SW**, které **meetuje requirements** whilst being **cost effective** a **ez to maintain**. Developuje se SW **infrastruktura**, řeší se **control**, **aplikace** a **databáze** systému. SW engineers jsou involved ve system **specific.**, **architectural designu**, integraci a **deploymentu**. U nás je takový SW inženýr / architekt involved ve specifikaci systému, architektuře, deploymentu jako třeba DevOps nebo installs, v "integraci" asi upe ne.
##### SWI_START

**Architektura:**
##### DB_IS_ARCHIT
Základní **organizace softwarového systému** zahrnující jeho **komponenty**, jejich **vzájemné vztahy a vztahy s okolím** systému, **principy návrhu** takového systému a jeho vývoje. <br />
![image](https://hackmd.io/_uploads/Hy1RFov1Gg.png) <br />
**JAKO EXAMPLE:**
• Potřebujeme persistenci (programy se mění, data zůstávají).
• Mnoho dat (paměť nestačí).
• Přístup k datům (mnoho uživatelů a z různých míst, konkurence).

**Analýza – technické požadavky** <br />
• Konceptuální model [domény](#####DOMENY) jako vstup.
• Odhad velikostí entit a jejich množství.
• Odhad počtu uživatelů současně pracujících se systémem.
• Typy interakcí uživatelů se systémem a odhad jejich náročnosti.
• První představa o rozložení systému a volba platforem. <br />
[Skip na architektury do hloubky](#####ARCHIT) <br />

![image](https://hackmd.io/_uploads/SymeV9Dkzl.png) <br />
![image](https://hackmd.io/_uploads/SyMLv5wyGg.png) <br />

**SDLC** je SW dev **life cycle**, fáze:
* **requirements** gather and analysis
* **design** - **structured** (based on functions) nebo **obj** (based on objects) oriented
* **implementation** - code review, unit tests, testy v DevOps pipelině z praxe
* **testing** - func., performance, secur. tests, , testy v DevOps pipelině z praxe
* **deployment**... čiže DevOps
* **maintanence** - corrective, adapt., perfective... SW testing, bug reports v Jiře, releases

**GENERAL MODELY:**
* **Waterfall** (above phases sequentially), taková klasika
* **Evolutionary** (**spec., dev., valid. rapidly** from abstract specification)
* **Formal** (**formal math. system specification** and using **math. methods** to program, sure to meet specifications)
* **System assembly** from reusables (integr.), třeba PLC systém ze starých modules

![image](https://hackmd.io/_uploads/SysSUYv1Mg.png) <br />

Trochu víc tam, kde to může být nejasné:
* **Iterative:** **first version of SW** developed **w/ some specifications**, new versions **iterate in an exact fixed period**. **req gathering + feasibility, design in diagrams, impl and testing** of mostly black and white or gray box, deploy, **review + validation or start again from req to maintanence**. not for small projects, needs more resources and design can be changed all the time, **could go over budget on reqs, project completion might not be set from changing reqs**
* **Incremental:** errs ez to be recognized, easy to test and debug, flexible, simple to manage risk, **important functionality early**, needs good planning, total cost high, needs well defined modules
* **V Model:** easy to understand, **testing** and their design **happens** well **before coding** and avoids flow of defects down, works for small plans with ez reqs, rigid, not good for complex projects, **no early prototypes produced, midway changes** require test docs and required docs **to be updated**
* **Agile:** freq. **delivery**, **face to face comm w/ customers**, efficient design and **fullfills business reqs**, anytime **changes** r acceptable, reduces total dev time, **shortage of formal docs creates confusion** at various phases + **maintanence** can prove **difficult** later on. Tbf z praxe ty ez changes, quick delivery a reduced dev time nejsou nutně real, bohužel problémy s dokumentací accurate jsou
* **DevOps:** highly violatile impl. not suitable for all apps, agile dev., continuous integration and deployment not suitable for safety, security and reliability focused projects
###### ZAKLADNI_ARCH
[Pokud tě nezajímají use cases, vztahy v ULM, yapping o objektech a basics z OOP, přeskoč na další mentions of models zde](#####DALSI_ARCH) <br />
![image](https://hackmd.io/_uploads/S1fTw5DJzl.png) <br />

##### UML
**Use cases** transform user needs to func. reqs, defines **scope** and **boundary** and behaviour of system, what will interact with it, **verifies** and **validates** sys. requirements, **help with dev planning** all in **natural language**. In a Use Case, you describe the use of a system for a given work task. Purpose is **discover the func. reqs**, analyse **what functionality is needed**, uncover and **describe all tasks** of the system. UCs are good analytical tools, notation ez for everyone, market standard, joint work of customer and supplier, brings structure. Documented by UC diagrams or verbal descriptions. UC defines the **sequence of the actions performed by the system that has a visible result** for the particular actor. K UC diagramu a scenarios i activity diagramy.

![image](https://hackmd.io/_uploads/H1C5Ytw1zg.png) <br />
![image](https://hackmd.io/_uploads/BkIiKFvJfe.png) <br />
![image](https://hackmd.io/_uploads/Hk9oFYPkMg.png) <br />
![image](https://hackmd.io/_uploads/BJehFFDkze.png) <br />

**GENERALIZACE je dědičnost!!!** Dál se používají další OOP termíny v kontextu tříd.
WIP ZDE LINK NA OOP

**A complete use case is delivered in one release very occasionally.**
* Deliver the **simple case** in release 1
* Add **high-risk handling (extensions)** in release 2
* Put **preferred customer handling** in release 3

**Diagramy aktivit**
* **Diagram popisující průběh (scénář) jednoho use-case, a to včetně alternativních scénářů - např. scénář, kde zadáme špatný vstup a dostanem chybu.**
* Diagram popisující časovou návaznost několika akcí v čase (tedy např. přes více use-case).
* Podstatnou vlastností diagramu aktivit je, že na rozdíl od use-case diagramu popisuje časové návaznosti aktivit.

[Skok aaaaaž na vzory spojené s UML](#####UML_VZORY) <br />

![image](https://hackmd.io/_uploads/HJ3uaKPkzg.png) <br />

Objects are **enablers of a sequence of transactions** required by the use case. An object can therefore typically participate in several use cases. A set of **interconnected objects constitutes the system**. Interactions between objects result in:
* Collective behavior
* Changes in the logical configurations and states

An obj is an **identifiable individual entity** with **identity** and **behaviour** that **interacts w/ other objs**. Secondarily it may have some **attributes**, it has a **lifetime** and a **state** in different phases of its life cycle. Amongst **external views** are its **properties, responsibilities, services, associations, interactions** and **protocol**. **Internal view** of **how data is represented** and **implemented behaviours**. A **link** is a physical / conceptual **connection between objs**. Matematicky **tuple** nebo **ordered list**. WIP ZDE SKOK NA FPR

A **class diagram** is a graphic view of the **static structural model**. A **class / třída** **describes a set of objs** with **common structure, behaviour, relationships and semantics**, s tím že **objekt** je **instance** té třídy, **named** using the **domain vocab**ulary.

###### DOMENY
![image](https://hackmd.io/_uploads/S1IabiPJze.png) <br />
![image](https://hackmd.io/_uploads/r1Ox8jP1Mg.png) <br />
![image](https://hackmd.io/_uploads/Hk6iKhvkGg.png) <br />
![image](https://hackmd.io/_uploads/S176Fhvyze.png) <br />
* **Improving productivity** for developers.
* **Improving communication** with domain experts. <br />
[PL/SQL a jmenný prostor](#####JMENNY) <br />

**ISSUE: Ghetto Language**
* Company that's built a lot of its systems on an in-house language which is not used anywhere else. This makes it **difficult** for them **to find new staff** and to **keep up with technological changes**.
* **DO NOT BUILD CUSTOM GENERAL PURPOSE LANGUAGES.**
* **Blinkered Abstraction** allows you to **express** the **behavior of a domain** much more easily than if you think **in terms of** **lower-level constructs**. However, any abstraction, be it a DSL or a model, always carries with it a **danger** - that of **putting blinkers on your thinking**.

**Role** is a **named specific behaviour** of an object **in a context**, **presented to** the **world**. **Type** specifies a **domain of objs** together with **operations applicable to them** **without defining** the **physical implem**. **Interface** is a **named set** of externally **visible operations**. **Notions of role, type and interface are interchangable somehow.** V tomto odstavci jsou sice mentions of **sets / množiny** + **operace**, ale není relevantní zde linkovat matematiku, jde stále o praktické věci.

**Typy vztahů:**
* **Asociace** - **group** of **bidirectional links** with **common structure** and **semantics**, the **same way** as a **class** **is linked to** its **objs**. **Example: a Person works for a Company**
* **Agregace** - **"a part of" relationship** where **objs representing components** are **associated w**ith **another obj** that **represents** an entire **big thing**, fomally called an **assembly**.
* **Závislost / dependency** **slabší** vztah, **např. client a supplier**.
* **Generalizace / dědičnost** - **generický element** neboli **rodič** a jeho **vzta**h se **specifickým elementem** neboli **dítětem**, které je **konzistentní** právě **se** svým **rodičem**, ale **přidá info navíc**.

![image](https://hackmd.io/_uploads/r1XKl9DkMx.png) <br />
![image](https://hackmd.io/_uploads/HkVje9Pkzg.png) <br />
![image](https://hackmd.io/_uploads/r1Dsl9D1zg.png) <br />
![image](https://hackmd.io/_uploads/Sy0ol5P1fg.png) <br />
![image](https://hackmd.io/_uploads/rJ9NWiDJGg.png) <br />
![image](https://hackmd.io/_uploads/rJICeqPyGg.png) <br />
**KOMPOZICE JE AGREGACE, jen aby nedošlo k zmatení, ale je to jiný typ.** <br />
![image](https://hackmd.io/_uploads/SykfmcDyfe.png) <br />
![image](https://hackmd.io/_uploads/HyoGm9vyGx.png) <br />
![image](https://hackmd.io/_uploads/HJaOFowJzg.png) <br />

**Rational Unified Process (RUP)** is a **software development process** for o**bject-oriented models**. It is also known as the Unified Process Model. It is created by Rational Corporation and is designed and documented **using UML (Unified Modeling Language)**. This process is included in the IBM Rational Method Composer (RMC) product. IBM (International Business Machine Corporation) **allows** us t**o customize, design, and personalize the unified process.** **UC driven, arch. centric and risk focused.** <br />
![image](https://hackmd.io/_uploads/ryCLYhv1zx.png) <br />
![image](https://hackmd.io/_uploads/HyfDF3w1Gl.png) <br />

* **Inception** - **communication, planning, scope, requirements, milestone criteria check, plan, goals, UC model... PRETTY MUCH JEN MEETINGY**
* **Elaboration** - **development plan**, **revision of the UC model**, **business cases** and **risks**, **milestone criteria check** again, **architecture**... basically už víc konkrétní plán, model, requirements na byznys cases a architektura
* **Construction** - **development** and **completion**, **testing done**... **IMPLEMENTACE HOTOVA**
* **Transition** - public **release** + **beta testing**, updated **documentation**, **defect removal**
* **Production** - **maintanence**

**Good docs** and **risk management**, **reuse of components**. However **requires experts**, can be **complex** and **hard to integrate** again and again. **Incremental dev** or **iterative approach with** project **releases**, **UC** and **scenario** use, **modular architecture**, checks **performance of** the **system** or **app**, needs **consistent sync work** and **validation**.

![image](https://hackmd.io/_uploads/ryBqPcDyGg.png) <br />
##### DALSI_ARCH

[Pokud ses chtěl podívat na advanced modely, tady je skok zpátky na ty základní](#####ZAKLADNI_ARCH) <br />

#### Informační systémy, architektura víc in depth a vzory
**IS:** jde o **interakci mezi lidmi, procesy a daty.** Informační systém je **určen ke zpracování (získávání, přenos, uložení, vyhledávání, manipulace, zobrazení) info**rmací. 
**Agendy** jako **ekonomické, osobní, skladové, dokumentové a školní**. **Architektura** informačního systému leží na **vyšší úrovni abstrakce**:
* **pohled** na **doménu**, i.e. **souvisejicích věcí z POV customera**
* **pohled vývojáře** na **globální strukturu** a **chování** jeho **částí / komponent**, **propojení** a **synch.**
* **pohled** na **přístup k datům** jejich **tok**
* **pohled** na **komponenty fyzicky**

**Má pomůcka, je to jako v sítích, máš fyzické káble, pak linkovou vrstvu s daty, pak komponenty sítě s nějakým syncem a chováním, jenž dávají smysl network engineerovi a pak upe nahoře abstrakci sítě pro users.**

Toto je ovšem rakovina: <br />
![image](https://hackmd.io/_uploads/SJ2fLswJGl.png) <br />
![image](https://hackmd.io/_uploads/Hk8NUovJMe.png) <br />
**Pomůcka... Rámec, vizi má vizionář, nějaký chytrolín stratég CEO. Pod vizí je important byznys - jakýsi kapitalista vlastník. Pro systémový model jako takový je už vyčleněná trošku vyšší společnost - architekt, návrhář, něco jako nepo baby, co si může dělat, co chce zábavného. Technologický model má taky návrhář nebo technolog, taky vyšší společnost. Detailní reprezentace pro specialistu nebo programátora dělníka. Provoz pro proletariát, vyčleněný pracovník nebo uživatel nebo chudáček pan správce.**

**Important asociace architektury IS: prezentace, doménová logika, přístup k datům, servisní vrstvy.** <br />
[Co je doména zas? Já zabudor](#####DOMENY) <br />

**Tři klíčové kompetence:**
* **Komunikace s uživatelem** (**prezentace info**rmací, **předání požadavků**)
* Zpracování informací a jejich (**dočasné**) **uchování**
* **Trvalé uchování** informací (**dat**)
* => **Třívrstvá architektura** (první se stává druhou, pokud je fyzicky oddělena od toho, kdo ji používá... uhhh upřímně nevím co toto má znamenat v tom kontextu xdddd byeee)

**Klient – server, p-vrstvá architektura.**

##### ARCHIT
* **statická architektura** – umožňuje **zachytit pouze pevnou strukturu SW systému** **bez možnosti změn**, struktura systému je **daná při návrhu** a **neměnná za běhu**
* **dynamická architektura** – oproti statické architektuře navíc **podporuje vznik a zánik komponent a vazeb za běhu** systému **podle pravidel určených při návrhu**, **struktura** systému **se dynamicky mění**
* **mobilní architektura** – **rozšiřuje dynamickou arch**itekturu o **mobilní prvky**, kdy se **komponenty a vazby přesouvají za běhu** systému **podle stavu výpočtu**

**OK tvořím architekturu:** <br />
![image](https://hackmd.io/_uploads/r1Mm5iD1Mg.png) <br />
[Zpátky na start SWI, kde je první mention achitektury](#####SWI_START) <br />
![image](https://hackmd.io/_uploads/rJrzaoD1Gx.png) <br />
**MVC komunikuje v jakémsi trojuhelníku, ale v 3 layer arch. komunikace jde jedním směrem napříč vrstvama.**

**Stav struktury systému, navazující na sebe:**
* **Komponenty** – **části** systému **s** daným **rozhraním** (programming **interfaces**)
* **Konektory** – **komunikační kanály** pro **propojení komponent s** daným **rozhraním**
* **Konfigurace** – **konkrétní způsob** vzájemného **propojení** komponent **pomocí konektorů**

WIP SKOK NA OOP ZASE <br />

![image](https://hackmd.io/_uploads/B1UrLoP1zl.png) <br />

**Life cycle IS questions:**
* Staré vs nové přístupy
* Požadavky a parametry
* Přírustky a iterace
* Kdy se začíná vs kdy se končí
* Jak a proč dokumentovat

**IS dev metodiky:**
* **Unified process neboli RUP, SCRUM, ***TDD (test driven dev, nejdřív testy a pak se dopíše passing code)***, EP neboli extreme programming**
* Robustní vs agilní
* Zaměření na procesy nebo lidi
[Základní modely pro připomínku](#####ZAKLADNI_ARCH) <br />
[Advanced modely zas a znova](#####DALSI_ARCH) <br />

SCRUM je zmíněn hned pod zákl. architekturou btw

**Formalizovaný IS ne ve smyslu matematickém, ale jde o to, že se s informacemi nepracuje v neformální bázi, máme předefinované a závazné formy práce s něma, i.e. zadáváme nějakou žádost v IS formulářem s definovanýma políčkama, které jsou validovány + evidence.**

![image](https://hackmd.io/_uploads/BJtL-owJfe.png) <br />
![image](https://hackmd.io/_uploads/ByqOXivJMg.png) <br />
[Doména link pro lidi, co si nedali gingko dneska](#####DOMENY) <br />
**Struktura vzorů**
* Výstižné jméno (**název**)
* **Problém** (Co)
* **Souvislosti (Kdo, Kdy, Kde, Proč)**
* **Řešení** včetně **UML** diagramů (**Jak**)
* **Příklady** včetně **zdrojových kódů**

• Vzory se nikdy nevyskytují osamoceně.
• Propojování vzorů je obvyklé zejména při spolupráci
různých vrstev (logik).
• Každý katalog vzorů souvislosti popisuje.

**Vzory pro doménovou logiku**
* **Table module**
* **Transaction script**
* **Domain model**
* **Service layer** <br />
![image](https://hackmd.io/_uploads/SJC6Civkze.png) <br />
![image](https://hackmd.io/_uploads/B1uxLhvJMe.png) <br />
![image](https://hackmd.io/_uploads/rJzFAoPyMx.png) <br />
![image](https://hackmd.io/_uploads/Sy1pH3PJMl.png) <br />
![image](https://hackmd.io/_uploads/BysYCjwyzg.png) <br />
![image](https://hackmd.io/_uploads/rkjb8nvJGe.png) <br />
![image](https://hackmd.io/_uploads/rkLgy2wyfg.png) <br />
![image](https://hackmd.io/_uploads/HkLu13v1zl.png) <br />
**K tomu service layeru, máme webovou aplikaci, která umí pracovat s file systémem - file service a má uživatele se specifickými právy, kteří se musí přihlašovat - auth. service. Ty mají nějaké funkce / operace a koordinují response.**

Historicky nejdřív přišel Gang of Four a po nich Fowler, ti vymysleli:
* **Creational** patterns
* **Structural** patterns
* **Behavioural** patterns
***Zde končí GoF, hodně basic coding stuff, pak ale s popularitou internetu a hlavně webů***
* **Base** patterns
* **Domain logic** patterns
* **Distribution** patterns
* **Data source architect.** patterns
* **Object-relational behavioural / structural / metadata mapping** patterns
* **Web presentation** patterns
* **Offline** concurrency patterns
* **Session** patterns <br />
![image](https://hackmd.io/_uploads/Byu2O3vyze.png) <br />
![image](https://hackmd.io/_uploads/B1o3d3DkGx.png) <br />
![image](https://hackmd.io/_uploads/H18lF2PJGg.png) <br />
![image](https://hackmd.io/_uploads/HkqeK2DJzg.png) <br />

![image](https://hackmd.io/_uploads/rkFyCsP1zl.png) <br />
**View totiž observuje Model, zbytek patterns je jednoznačný.**

**Jak se připojit k relačnímu datovému
zdroji?**
**Zákl**adní **požadavek** je **nezávislost doménové logiky na** logice **přístupu k datům**...
* **Table data gateway**
* **Row data gateway**
* **Active record**
* **Data mapper** <br />
![image](https://hackmd.io/_uploads/SJR0B3D1Gg.png) <br />
![image](https://hackmd.io/_uploads/SySNI2wyze.png) <br />
![image](https://hackmd.io/_uploads/H1A4Unvyzl.png) <br />
**ACTIVE RECORD PRIDAVA DOMENOVOU LOGIKU** <br />
![image](https://hackmd.io/_uploads/B16UL3vJfg.png) <br />
![image](https://hackmd.io/_uploads/rJtwU2vkGe.png) <br />
![image](https://hackmd.io/_uploads/B1I5U3Pkfe.png) <br />
![image](https://hackmd.io/_uploads/B1o583w1Ml.png) <br />
![image](https://hackmd.io/_uploads/SkgjI3Dkfx.png) <br />
![image](https://hackmd.io/_uploads/HysmInw1Gl.png) <br />

**Objektově-relační chování**
* **Unit of Work** A **list of objects** **affected by** a **business transaction** and **coordinates** the **writing** out of **changes** **and** the **resolution** **of concurrency** problems.
* **Identity Map** **Each object** gets **loaded only once** by keeping every **loaded object in a map**. **Looks up objects** using the map **when referring to them**.
* **Lazy Load** An object that **doesn't contain all** of the **data** you need but **knows how to get it when needed**. <br />
![image](https://hackmd.io/_uploads/ByHeO2P1Ge.png) <br />
![image](https://hackmd.io/_uploads/ryClunwkfg.png) <br />
![image](https://hackmd.io/_uploads/r1fWuhwkMe.png) <br />
![image](https://hackmd.io/_uploads/HkdbO3D1fl.png) <br />

[Skok na databáze](####Databáze) <br />
![image](https://hackmd.io/_uploads/rJIM_3w1fe.png) <br />
![image](https://hackmd.io/_uploads/B1qz_3vyzx.png) <br />
![image](https://hackmd.io/_uploads/S1r7OnD1Gg.png) <br />

**Common patterny, třetí screen víc niché a ne upe nutné znát.** <br />
![image](https://hackmd.io/_uploads/HkeAW2vJMx.png) <br />
![image](https://hackmd.io/_uploads/ryr0W2P1zx.png) <br />
![image](https://hackmd.io/_uploads/r15AbnPkGe.png) <br />

##### UML_VZORY
[Zpátky na UML, protože toto je jejich extension](#####UML) <br />
**Sekvenční diagramy pro klíčové operace (zejména kooperace objektů v rámci vzorů).**

**Možno v diagramech oddělit čistě doménový návrh od návrhu se vzory.** <br />
![image](https://hackmd.io/_uploads/rkoYd2v1zg.png) <br />
![image](https://hackmd.io/_uploads/SyZq_2D1fx.png) <br />
![image](https://hackmd.io/_uploads/SJV5d3D1fl.png) <br />
![image](https://hackmd.io/_uploads/Sy_qdnPJfl.png) <br />
![image](https://hackmd.io/_uploads/HJmjunDkze.png) <br />
![image](https://hackmd.io/_uploads/B1xJYnPJMe.png) <br />

#### Práce s lidmi a yap o standardech, asi ne uplně nutné honestly. až na Agile principy na konci
Co je potřeba a co je podstatné?
* Lidé a jejich spolupráce
* Plány, pravidla, procesy, řízení
* Dokumentace
* Techniky a technologie
* Dlouhý čas
* Cílem je produkt (software) a jeho kvalita měřená více faktory

• Základem jsou lidé, jejich kvalita a kvalita jejich výstupů.
• Je nutné umět organizovat práci a koordinovat lidi v týmu. Je otázkou, s jakou mírou administrativní zátěže.
• Je nutná dokumentace, kdo nedokumentuje, neváží si vlastní práce. Je otázkou, v jakém
množství.
• Je nutný plán (čas a náklady). Je otázkou, zda je možné odhadnout všechno dopředu.
• Jsou nutná dobrá rozhodnutí na začátku (technologie, architektura). Je otázkou, zdá máme vždy dostatek informací.

Aspekty práce v týmu
* Stačí dva a už se musí na lecčems dohodnout.
* Je rozdíl pracovat ve velkém a malém týmu.
* Robustní x agilní (čilý, aktivní, horlivý) přístup k projektu.
* Vždy musíme definovat role a odpovědnosti, ze kterých vyplývá způsob řešení úkolů.

![image](https://hackmd.io/_uploads/B1Myc2PJGg.png) <br />

**12 principu je k agile**
![image](https://hackmd.io/_uploads/H131qhPJfx.png) <br />

Obecné principy
• Komunikace
• Jednoduchost
• Zpětná vazba
• Odvaha

![image](https://hackmd.io/_uploads/HkoOb2Pkze.png) <br />

#### Testování, verifikac a validace, rizika a kvalita
Programy jsou složité, těžko pochopitelné a těžko dokážeme správnost. Snažíme se ale najít chyby a zjistit, zda splnujeme specifikace. Uplne testovani je omezeno exponencionalnim poctem stavu SW, daunting. Pouziva se treba unit testing individualnich komponent v izolaci.

Verifikace neboli ověření a validace neboli potvrzení zahrnují statické (matematické) techniky jako důkaz správnosti. Případně dynamické techniky, což je soulad code a specifications, čím víc k low level code, tím těžší provést.
![image](https://hackmd.io/_uploads/B1k_QnP1zg.png) <br />
![image](https://hackmd.io/_uploads/SJMOX3w1fx.png) <br />
![image](https://hackmd.io/_uploads/HyKOm2vJMx.png) <br />
![image](https://hackmd.io/_uploads/r16dm2wyMx.png) <br />
![image](https://hackmd.io/_uploads/HyxqX2vkMx.png) <br />

TODO asi lépe popsat verifikace vs validace pokud to není jinde?

### 1.9) URO a ZPG
Nepohoda či unava pro usera, kterou si sám ani neuvědomí kolikrát. Některá rozhrání vyhovují lidem více a jiná méně, neobjektivnější jsou výzkumy studující zákonitosti lidského vnímání. <br />
![image](https://hackmd.io/_uploads/Skco9H7lMe.png) <br />
![image](https://hackmd.io/_uploads/Hk5wYr7eGg.png) <br />
![image](https://hackmd.io/_uploads/SyCPYrXlGg.png) <br />
![image](https://hackmd.io/_uploads/HJVKKBQlzl.png) <br />
![image](https://hackmd.io/_uploads/H1KYYB7gGl.png) <br />
![image](https://hackmd.io/_uploads/S16FFSmeze.png) <br />
![image](https://hackmd.io/_uploads/SJk5KrQgMl.png) <br />
![image](https://hackmd.io/_uploads/BJmqtH7eGx.png) <br />
![image](https://hackmd.io/_uploads/BkI5YHQlMx.png) <br />
![image](https://hackmd.io/_uploads/HJt6qSQgGl.png) <br />
![image](https://hackmd.io/_uploads/Hk3pcH7lzl.png) <br />
![image](https://hackmd.io/_uploads/B1ZCqSmxMx.png) <br />
![image](https://hackmd.io/_uploads/HJECcBQlfg.png) <br />
![image](https://hackmd.io/_uploads/SJO09SXeGg.png) <br />
![image](https://hackmd.io/_uploads/r1j0qrXxze.png) <br />
![image](https://hackmd.io/_uploads/Hy1liH7gfg.png) <br />
Zkušený uživatel chce plnou kontrolu nad produktem, jinak nemusí být spokojený, když nemá pocit "přečtenosti". Pocit nespokojenosti hlavně při neočekávaném chování produktu v některých situacích, když něco nejde udělat, není jasné, proč produkt vyžadujě nějaké data, proč musí být v určitém formátu atd. <br />
![image](https://hackmd.io/_uploads/rJW22BXgGl.png) <br />
![image](https://hackmd.io/_uploads/ryzxormxMl.png) <br />
![image](https://hackmd.io/_uploads/ryEDorXgGx.png) <br />
![image](https://hackmd.io/_uploads/Bk3PjBXeGe.png) <br />
![image](https://hackmd.io/_uploads/SkkdsHmezg.png) <br />
![image](https://hackmd.io/_uploads/BJmOsrQxGx.png) <br />
![image](https://hackmd.io/_uploads/S1BdsSmxMl.png) <br />
![image](https://hackmd.io/_uploads/B1Y_oH7lzx.png) <br />
![image](https://hackmd.io/_uploads/ryhOsrXgfe.png) <br />
![image](https://hackmd.io/_uploads/rkrFjB7eze.png) <br />
![image](https://hackmd.io/_uploads/S1_KiHQlMg.png) <br />
![image](https://hackmd.io/_uploads/SyTFjHXgfg.png) <br />
![image](https://hackmd.io/_uploads/ryy9iS7efx.png) <br />
![image](https://hackmd.io/_uploads/HJBcsSmxfe.png) <br />
![image](https://hackmd.io/_uploads/By_qiHXgze.png) <br />
![image](https://hackmd.io/_uploads/B1i5srmlMe.png) <br />
![image](https://hackmd.io/_uploads/BJA9iS7xfg.png) <br />
![image](https://hackmd.io/_uploads/BJgiiHmezl.png) <br />
![image](https://hackmd.io/_uploads/Hk7soB7eze.png) <br />
![image](https://hackmd.io/_uploads/ryOioSXeGg.png) <br />
![image](https://hackmd.io/_uploads/HkoioSmgGl.png) <br />
![image](https://hackmd.io/_uploads/HyAsjS7eMe.png) <br />
![image](https://hackmd.io/_uploads/r1e2orXxGg.png) <br />
![image](https://hackmd.io/_uploads/SkN0iS7ezl.png) <br />
![image](https://hackmd.io/_uploads/HyLRoBQezx.png) <br />
![image](https://hackmd.io/_uploads/Hy6RsS7xzx.png) <br />
![image](https://hackmd.io/_uploads/Hkey3SXxze.png) <br />
![image](https://hackmd.io/_uploads/BJzJ3BXxGl.png) <br />
![image](https://hackmd.io/_uploads/SyuJ2rmefx.png) <br />
![image](https://hackmd.io/_uploads/Skx5k3rXxMg.png) <br />
![image](https://hackmd.io/_uploads/BkaknSQeGx.png) <br />
![image](https://hackmd.io/_uploads/rJ4xnr7lMg.png) <br />
![image](https://hackmd.io/_uploads/ByZVhHQxfx.png) <br />
![image](https://hackmd.io/_uploads/rJNV3rQlMx.png) <br />
![image](https://hackmd.io/_uploads/S1D42r7lMe.png) <br />
![image](https://hackmd.io/_uploads/Hy542BQxzg.png) <br />
![image](https://hackmd.io/_uploads/Hkp4hB7lzx.png) <br />
![image](https://hackmd.io/_uploads/HJeS3SQeGe.png) <br />
![image](https://hackmd.io/_uploads/Bk7B3SmeGe.png) <br />
![image](https://hackmd.io/_uploads/HJ8B2H7eze.png) <br />
![image](https://hackmd.io/_uploads/SkKBnB7lzl.png) <br />
![image](https://hackmd.io/_uploads/rk2H2HXeGg.png) <br />
![image](https://hackmd.io/_uploads/SyaLhB7xGl.png) <br />
![image](https://hackmd.io/_uploads/SylPnr7lMx.png) <br />
![image](https://hackmd.io/_uploads/ByXDnSmlzl.png) <br />
![image](https://hackmd.io/_uploads/SkSwnr7gzx.png) <br />
![image](https://hackmd.io/_uploads/BynPnrXezx.png) <br />
![image](https://hackmd.io/_uploads/H1TDnrXefe.png) <br />
![image](https://hackmd.io/_uploads/r1lO3H7lGx.png) <br />
![image](https://hackmd.io/_uploads/rJ4_3r7xfe.png) <br />
![image](https://hackmd.io/_uploads/r1LOnrXezl.png) <br />
![image](https://hackmd.io/_uploads/HytdhB7lMg.png) <br />
![image](https://hackmd.io/_uploads/BJCOhSmeMe.png) <br />
![image](https://hackmd.io/_uploads/HyetnHQgMl.png) <br />
![image](https://hackmd.io/_uploads/BkzFhrXgGl.png) <br />
![image](https://hackmd.io/_uploads/ry3K2SQlMe.png) <br />
![image](https://hackmd.io/_uploads/HkAtnSmlGx.png) <br />
![image](https://hackmd.io/_uploads/H1QanHmgze.png) <br />
![image](https://hackmd.io/_uploads/SJwahS7eMe.png) <br />
![image](https://hackmd.io/_uploads/S1qanr7gfe.png) <br />
![image](https://hackmd.io/_uploads/Bk3phBmlMg.png) <br />
![image](https://hackmd.io/_uploads/SJ-Anr7lfx.png) <br />
![image](https://hackmd.io/_uploads/HyNR3B7gMe.png) <br />
![image](https://hackmd.io/_uploads/SkLC2SmxGx.png) <br />
![image](https://hackmd.io/_uploads/B1_A2BQxze.png) <br />
![image](https://hackmd.io/_uploads/HJsRhrXefg.png) <br />
![image](https://hackmd.io/_uploads/Sk0CnSmlGl.png) <br />
![image](https://hackmd.io/_uploads/SkLypBQgGg.png) <br />
![image](https://hackmd.io/_uploads/r1_1armxMx.png) <br />
![image](https://hackmd.io/_uploads/r1qkpSXeGe.png) <br />
![image](https://hackmd.io/_uploads/Sk1gTSXxzl.png) <br />
![image](https://hackmd.io/_uploads/Hk-g6BQxMg.png) <br />
![image](https://hackmd.io/_uploads/B1Nl6rmxze.png) <br />
![image](https://hackmd.io/_uploads/BkPgaH7xze.png) <br />
![image](https://hackmd.io/_uploads/HkcgTSmeMx.png) <br />
![image](https://hackmd.io/_uploads/BJagTrXgMl.png) <br />
![image](https://hackmd.io/_uploads/rkJ-6BQefl.png) <br />
![image](https://hackmd.io/_uploads/rJdG6SXgGg.png) <br />
![image](https://hackmd.io/_uploads/rknMarQgGl.png) <br />
![image](https://hackmd.io/_uploads/rykXpBQeGl.png) <br />
![image](https://hackmd.io/_uploads/B1z76H7gfg.png) <br />
![image](https://hackmd.io/_uploads/SkrmpHXlMe.png) <br />
![image](https://i.imgur.com/ljxra06.png) <br />
![image](https://i.imgur.com/EIQ1336.png) <br />
![image](https://i.imgur.com/Qdob7Tm.png) <br />
![image](https://i.imgur.com/xOIMfS4.png) <br />
![image](https://i.imgur.com/s11tvFA.png) <br />
![image](https://i.imgur.com/e6O62Em.png) <br />
![image](https://i.imgur.com/UgYh6GX.png) <br />
![image](https://i.imgur.com/XrwRkIi.png) <br />
![image](https://i.imgur.com/EiwECrK.png) <br />
![image](https://i.imgur.com/GNt4o3B.png) <br />
![image](https://i.imgur.com/qLDbotZ.png) <br />
![image](https://i.imgur.com/svSm0yy.png) <br />
![image](https://i.imgur.com/FwEMhua.png) <br />

[Link / skok úplně nahoru](#Předmluva)
