# Blok 3 – 3D grafika (Blender)

## Cíl

Chtěla jsem vytvořit 3D scénu představující menší rodinný dům se zahradou – rybníček s kapry koi, ohniště s lehátky a bazén se zeleninovou zahrádkou. Chtěla jsem utvořit příjemné prostředí pro rodinu i starší lidi v důchodu nebo snad jsako chata na kterou se každé léto těšíme.

---

## Postup

- dům už jsem měla z předchozího projektu hotový takže stačilo přidat zahradu
na trávu jsem přidala obrázek trávy a dala na něj patickle system - hair, 10 000 particles, advanced, brownian 0.3
- na rybníček jsem odstranila kus trávy a přidala další plochu kterou jsem udělala hnědou do tvaru misky, přidala jsem beziér curve - depth 0.1m - tím sem vyrobila stonek na lekníny které jsem pomocí edit modu upravila do požadovaného tvaru. květy leknínů jsem vytvořila pomocí plane (plochy) a v edit modu ji upravila, dala jsem lístek na lístek a duplikovala je, po zmanšení jsem vytvořila několik vrstev okvětních listů tvořící květ.
- ryba byla složitá, pomocí sculpting modu jsem bojovala s každou křivkou, až později mi došlo že sculpting mode je velmi náročný na moji grafickou kartu. Nakonec jsem ale rybu dokončila a následně ji duplikovala. Duplikáty jsem zmenšila/zvětšila a umístila je na různá místa. každou rybu jsem potom zvlášť nabarvila abych nastínila diversitu a zakryla že jsou to prakticky identické duplikáty.
- ohniště bylo pomocí modifieru boleen celé ponořené do země. pak jsem vytvořila schody - add cube, araay - 20 pieses, -0.1 m po ose z, add beziér circle, deform - circle - object beziér circle, pak jsem na schody přidala barvu a podobným způsobem jsem udělala kachličky akorát jsem nechala array po ose z na nule. ohraničení ohniště byly vlastně jen kachličky akorát jich bylo míň a byli vyšší
- velmi jednoduše jsem vytvořila kastrol visící na řetězu nad ohništěm - přidala jsem válec a ten v edit modu upravila, duplikovala ho, zmenšila a zneviditelnila jsem menší duplikát podle boleen aby vytvořil vnitřek kastrolu, pomocí beziér curve jsem vytvořila stojan a řetěz jsem měla již z předchozího projektu připravený
- dřevo byl jen válec kterému jsem přidala v shading modu texturu a vniřrek jsem nahradila jiným válcem s texturou světlého vnitřku
- lehátka byla podle tutoriálu s pomocí beziér path a následně jsem přidala texturu tmavého dřeva kterou už dlouho používám, pak jsem je duplikovala a posunula kolem ohniště
- pro bazén jsem znovu vymazala trochu trávy a místo toho jsem přidala čtverec se zaoblenými rohy, udělala duplikát který jsem zmenšila a zneviditelnila jsem ho pomocí boleen aby vytvořil vnitřek. Schody jsem vyrobila  stejně jako kachličky a pak duplikáty zvětšovala a posouvala aby tvořili půlkruhové schody. Na bazén i schody jsem následně přidala texturu modrých bazénových kachliček a přidala poloprůhlednou plochu na vrch s modrým odstínem a viditelným zčeřením aby to tvořilo iluzi vody. K bazénu jsem přidala dva duplikáty lehátka a velmi primitivní slunečník.
- 

Renderoval jsem v Cycles, protože jsem chtěl realistické odrazy na skle. Trvalo to přibližně 8 minut na 512 vzorcích.

---

## Výstupy

- Soubor scény `kavarna.blend`
- Renderovaný výsledek:

![Render scény](../assets/images/blok3_render.png)

- Render bez a se světly (srovnání):

![Srovnání osvětlení](../assets/images/blok3_srovnani.png)

---

## Reflexe

Jsem spokojený s výsledným osvětlením – teplé světlo z výlohy na dlažbě vypadá dobře. Modelování samotné bylo rychlejší, než jsem čekal. Co mi zabralo nejvíce času, bylo nastavení materiálu skla – průhlednost v Blenderu vyžaduje správné nastavení průhlednosti v render settings, jinak je sklo černé. Příště bych si scénu lépe naplánoval dopředu – přidával jsem objekty chaoticky a pak bylo těžké je v Outlineru najít, protože jsem je nepojmenoval.

---

## Teoretické pozadí (stručně)

3D objekty se skládají z vrcholů, hran a ploch (faces) – dohromady tvoří mesh. Tvar objektu upravuji v Edit Mode, kde pracuji přímo s geometrií. Materiály definují, jak povrch reaguje na světlo – použil jsem Principled BSDF, který kombinuje různé vlastnosti povrchu (barva, lesk, průhlednost). Renderování je výpočet výsledného obrazu ze 3D scény, přičemž Cycles simuluje fyzikálně korektní pohyb světelných paprsků. Podrobnosti v `teorie.md`.

---

## Zdroje

- [https://docs.blender.org/](https://docs.blender.org/) – dokumentace Blenderu
- [https://www.youtube.com/@blenderguru](https://www.youtube.com/@blenderguru) – Blender Guru, tutoriál na zátiší
- [https://polyhaven.com/](https://polyhaven.com/) – HDRI pro okolní osvětlení (CC0)
