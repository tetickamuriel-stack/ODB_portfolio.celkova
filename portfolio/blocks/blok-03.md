# Blok 3 – 3D grafika (Blender)

## Cíl
3D scéna představující menší rodinný dům se zahradou – rybníček s koi kapry, ohniště s lehátky a bazén se zeleninovou zahrádkou. Příjemné prostředí pro rodinu i starší lidi v důchodu.
---

## Postup
 - Dům už jsem měla z předchozího projektu hotový, takže stačilo přidat zahradu. Na trávu jsem přidala obrázek trávy a dala na něj particle system – hair, 10 000 particles, advanced, brownian 0.3.
 - Na rybníček jsem odstranila kus trávy a přidala další plochu, kterou jsem udělala hnědou do tvaru misky. Přidala jsem Bezier curve – depth 0.1 m – tím jsem vyrobila stonek na lekníny, které jsem pomocí edit modu upravila do požadovaného tvaru. Květy leknínů jsem vytvořila pomocí plane (plochy) a v edit modu ji upravila. Dala jsem lístek na lístek a duplikovala je, po zmenšení jsem vytvořila několik vrstev okvětních lístků tvořících květ.
 - Ryba byla složitá, pomocí sculpting modu jsem bojovala s každou křivkou, až později mi došlo, že sculpting mode je velmi náročný na moji grafickou kartu. Nakonec jsem ale rybu dokončila a následně ji duplikovala. Duplikáty jsem zmenšila/zvětšila a umístila je na různá místa. Každou rybu jsem potom zvlášť nabarvila, abych nastínila diverzitu a zakryla, že jsou to prakticky identické duplikáty.
 - Ohniště bylo pomocí modifieru boolean celé ponořené do země. Pak jsem vytvořila schody – add cube, array – 20 pieces, -0.1 m po ose z, add Bezier circle, deform – circle – object Bezier circle. Pak jsem na schody přidala barvu a podobným způsobem jsem udělala kachličky, akorát jsem nechala array po ose z na nule. Ohraničení ohniště byly vlastně jen kachličky, akorát jich bylo míň a byly vyšší.
Velmi jednoduše jsem vytvořila kastrol visící na řetězu nad ohništěm – přidala jsem válec a ten v edit modu upravila, duplikovala ho, zmenšila a zneviditelnila jsem menší duplikát podle boolean, aby vytvořil vnitřek kastrolu. Pomocí Bezier curve jsem vytvořila stojan a řetěz jsem měla již z předchozího projektu připravený.
 - Dřevo byl jen válec, kterému jsem přidala v shading modu texturu a vnitřek jsem nahradila jiným válcem s texturou světlého vnitřku.
 - Lehátka byla podle tutoriálu s pomocí Bezier path a následně jsem přidala texturu tmavého dřeva, kterou už dlouho používám, pak jsem je duplikovala a posunula kolem ohniště.
 - Pro bazén jsem znovu vymazala trochu trávy a místo toho jsem přidala čtverec se zaoblenými rohy, udělala duplikát, který jsem zmenšila a zneviditelnila jsem ho pomocí boolean, aby vytvořil vnitřek. Schody jsem vyrobila stejně jako kachličky a pak duplikáty zvětšovala a posouvala, aby tvořily půlkruhové schody. Na bazén i schody jsem následně přidala texturu modrých bazénových kachliček a přidala poloprůhlednou plochu na vrch s modrým odstínem a viditelným zčeřením, aby to tvořilo iluzi vody. K bazénu jsem přidala dva duplikáty lehátka a velmi primitivní slunečník.
 - Vedle bazénu jsem umístila obdélníkový, vyvýšený záhon, mírně zvětšený v průměru v horní polovině. V květináči je plocha s texturou hlíny. Pak jsem do tří z osmi květináčů dala tyče s kovovou texturou, aby simulovaly podporu pro rajčata. Z malé plochy jsem pomocí edit módu vytvořila siluetu listu a s pomocí módu solidify jsem vytvořila list rajčete. Na stonek jsem použila válec, který jsem prodloužila a přidala mu sekce, aby měl víc faces a byl ohebnější. Konec válce jsem zmenšila a vytvořila konečný stonek. V edit módu jsem z různých částí prodloužila jednotlivé faces a ohnula je, aby vypadaly jako větvičky. Listy jsem potom duplikovala a pečlivě je umístila na větvičky. Pod jednotlivé větévky jsem umístila malé kuličky, nebylo je třeba upravovat, jelikož budou viděny jen z dálky. Rajčata jsem postupně zmenšovala směrem ke konci větvičky. Čím menší byla rajčata, tím zelenější jsem jim dala barvu. Celou rostlinu s listy, stonkem a plody jsem duplikovala a umístila do dalších dvou záhonů. V každém záhonu byly tři rostliny rajčat, takže celkově 9. U posledního záhonu jsem rostliny zmenšila, abych dodala diverzitu a vypadala jako cherry rajčátka.
 - Do dvou největších záhonů jsem se rozhodla dát salát. Jako první jsem přidala sphere jako prostředek a dala jí zelenou barvu. Podobně jako listy u rajčat jsem z malé plochy pomocí edit módu vyrobila list salátu. Sculpting módem jsem přidala mírně low poly texturu salátového listu. Jednotlivé listy jsem duplikovala a rotací je obrátila, aby vše sedělo, pak jsem jeden list za druhým skládala na sebe a vytvořila vrstvení.
 - U okurek jsem jen vytvořila stonek stejně jako u rajčat a duplikovala jsem listy rajčat. Dala jsem kovovou mřížku, o kterou se má rostlina „opírat“, a plody jsem nedělala kvůli vysoké hustotě listů, takže by stejně nebyly vidět.
Renderovala jsem v Cycles, protože jsem chtěla realistické odrazy na skle. Trvalo to přibližně 15 minut na 256 vzorcích.

---

## Výstupy

- Soubor scény `zahrada.blend`
- Renderovaný výsledek: <img width="1555" height="877" alt="Snímek obrazovky 2026-06-01 211709" src="https://github.com/user-attachments/assets/f0849a6d-8aa4-44a7-bbe5-62d12331fb95" />
                        <img width="1547" height="877" alt="Snímek obrazovky 2026-06-01 211728" src="https://github.com/user-attachments/assets/9a08e173-1d70-479f-8b73-01fd5c46b5c3" />



---

## Reflexe

Jsem spokojená s výsledkem. Přestože tento projekt byl náročnější, jsem ráda, že jsem se do toho pustila. Naučila jsem se spoustu nových pojmů a zkratek, které mi ulehčí práci v příštích projektech. Naučila jsem se nejen sculpting mode, ale i to, že ne vždy je potřeba, někdy úplně stačí dát texturu, která vypadá podobně. Spoustu jsem se toho naučila i ze shading modu, který upravuje textury.

---

## Teoretické pozadí (stručně)

3D objekty se skládají z vrcholů, hran a ploch (faces) – dohromady tvoří mesh. Tvar objektu upravuji v Edit Modu, kde pracuji přímo s geometrií. Materiály definují, jak povrch reaguje na světlo – použila jsem Principled BSDF, který kombinuje různé vlastnosti povrchu (barvu, lesk, průhlednost). Renderování je výpočet výsledného obrazu ze 3D scény, přičemž Cycles simuluje fyzikálně korektní pohyb světelných paprsků. Podrobnosti: https://github.com/tetickamuriel-stack/ODB_portfolio.celkova/blob/main/portfolio/teorie/teorie-03.md 

---

## Zdroje - inspirace/tutoriály
https://www.youtube.com/watch?v=Lxem4yMs5Dg&t=1341s
https://www.youtube.com/watch?v=xX72ZuCOVVE
https://www.youtube.com/watch?v=Mxwl6STm1h0
https://www.youtube.com/watch?v=y7PdiGXbrD0
https://www.youtube.com/watch?v=KgBuWl_rfuI
https://www.youtube.com/watch?v=Hl8nfblJNF8&t=198s
https://www.youtube.com/shorts/j2_yK81QbJM
https://www.youtube.com/watch?v=QDyGvmq8AMA&t=2s
https://www.youtube.com/watch?v=ygjMX5mSi1Y
https://www.youtube.com/watch?v=60NGcPy_L0w&t=884s
