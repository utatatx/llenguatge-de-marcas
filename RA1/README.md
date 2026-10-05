# RA1 — Activitat Introductòria

Documentació dels fitxers lliurats en l'activitat introductòria de HTML.

## Objectiu de l'activitat

Ampliar els coneixements explicats a classe sobre pàgines web petites, corresponents als
resultats d'aprenentatge:

1. Reconèixer les característiques dels llenguatges de marques analitzant-ne i interpretant-ne
   fragments de codi.
2. Utilitzar llenguatges de marques per a la transmissió d'informació a través del web,
   analitzant l'estructura dels documents i identificant-ne els elements.

Els fitxers es lliuren en format HTML a l'entorn Moodle. Les 12 tasques tenen el mateix pes a la
qualificació.

## Estructura

```
RA1/
├── README.md                       ← aquest document
└── RA1 Activitat Introductoria/
    ├── 1.1_Tim.html                ← exercicis 1-4
    ├── 1.2_tauleta.html        ← exercicis 5-8, 10 i 12
    └── Activitat introductòria.pdf ← enunciat de l'activitat
```

## 1.1_Tim.html — Exercicis 1 a 4

Biografia de Sir Timothy Berners-Lee amb les etiquetes de text vistos a classe.

### Elements utilitzats

| Línia | Elementa | Exercici | Funció |
|-------|----------|-----------|--------|
| 4 | `<meta charset="UTF-8">` | 3 | Declara la codificació de caràcters, necessària perquè els accents i els dígits (`à è é í ò ú ·`) es mostrin correctament. |
| 5 | `<meta name="viewport">` | — | Adapta l'amplada al dispositiu. |
| 10 | `<h1>` | 1 | Encapçalament principal; estableix la jerarquia visual del document. |
| 12 | `<b>` | 1 | Text en negreta. |
| 13-15, 19-28 | `<i>` | 1 | Text en cursiva per a termes i noms d'institucions. |
| 11-34 | `<p>` | 1 | Pàrrafs que estructuren el text en blocs. |
| 37 | `<img>` | 4 | Fotografia de Berners-Lee amb `width="300"` per controlar la mida. |
| 40 | comentari HTML | 2 | Anotació sobre l'enllaç. |
| 43 | `<a href>` | 2 | Hiperenllaç a la Viquipèdia. |

### Com s'han resolt

**Exercici 1 — `<h1>`, `<b>`, `<i>` i `<p>`**
`<h1>` al nom complet, `<b>` als passatges en negreta, `<i>` a les cites i als noms
d'entitats, i `<p>` per separar el text en quatre pàrrafs.

**Exercici 2 — hiperenllaç a la Viquipèdia**
La paraula *Viquipèdia* es va convertir en un enllaç amb l'etiqueta `<a>` i l'atribut `href`:

```html
<a href="https://ca.wikipedia.org/wiki/Tim_Berners-Lee">Viquipèdia</a>
```

**Exercici 3 — declaració de `<meta charset>`**
`<meta charset="UTF-8">` a les primeres línies del `<head>`, abans del títol.

**Exercici 4 — inserció d'una imatge**
```html
<img src="URL_DE_LA_IMATGE" alt="Fotografia de Tim Berners-Lee" width="300">
```
Els dos atributs obligatoris de `<img>` són `src` (ruta de la imatge) i `alt` (text alternatiu).
`width="300"` no és obligatori, però evita que la imatge ocupi tota l'amplada.

### Validació

Sense errors ni avisos al validador W3C.

---

## 1.2_tauleta.html — Exercicis 5 a 8, 10 i 12

Pàgina amb les taules i el formulari de l'enunciat.

### Contingut per secció

| Línies | Secció | Exercici | Contingut |
|--------|--------|-----------|-----------|
| 14-57 | Llistat de pel·lícules | 5 | Taula simple **sense** vores amb 6 pel·lícules. |
| 60-103 | Taula amb vores | 6 | La mateixa taula amb les línies dibuixades. |
| 106-142 | Directors de les pel·lícules | 7 | Taula de pel·lícula, director i any. |
| 145-166 | Horari de projeccions | 8 | Taula de dia, hora i sala. |
| 169-188 | Formulari de contacte | 10 | `<form id="myform">` amb `<label>`, `<input>`, `<textarea>` i `<button>`, més `checkbox` i `radio`. |
| 191-204 | Taula amb cel·les fusionades | 12 | Ús de `colspan` i `rowspan`. |
| 206 | Enllaç de retorn | 9 | Ruta relativa a `index.html`. |

### Les quatre etiquetes de taula

Segons l'enunciat, una taula HTML es defineix amb quatre etiquetes:

```html
<table>   <!-- crea la taula i conté tot el seu contingut -->
  <tr>     <!-- cada fila -->
    <th>   <!-- cel·la de capçalera -->
    <td>   <!-- cel·la de dades -->
  </tr>
</table>
```

**Exercici 6 — les vores.** L'enunciat demana investigar els atributs `border` i `bordercolor`.
Aquest fitxer fa servir CSS:

```html
<style>
    table.borders td, table.borders th { border: 1px solid black; }
</style>
```

```html
<table class="borders" style="border: 3px solid #0066CC; border-collapse: collapse;">
```

- `class="borders"` connecta la taula amb la regla CSS del `<style>`.
- `border-collapse: collapse` fusiona les vores de les cel·les en una sola línia.
- La primera taula (14-57) no duu la classe: correspon a l'estat de l'exercici 5.

**Exercici 12 — `colspan` i `rowspan`.** `colspan="n"` uneix la cel·la amb les `n` següents de la
seva fila; `rowspan="n"` la manté occupant `n` files cap avall.

### Formulari (exercici 10)

```html
<form id="myform">
    <label for="nom">Nom:</label>
    <input type="text" id="nom" name="nom">
    <!-- ... -->
</form>
```

L'`id` permet que el `for` del `<label>` assenyali el control, i el `name` és el que
s'envia. L'atribut `id="myform"` és el que demanava l'enunciat. Sense `action` ni `method`,
el formulari no enviaria la informació enlloc.

---

## Validació (exercici 11)

Valoració amb el validador oficial W3C.

**`1.1_Tim.html`** → 0 errors, 0 avisos.

**`1.2_tauleta (1).html`** → 0 errors, 0 avisos.

Com és la taula:

```
      col 1      col 2      col 3      col 4
row1  A1         B1         B1         D1
       (rowspan2) (colspan2) (colspan2)
row2  [A1]       B2         B2         D2
row3  A3 i B3    B2         B2
                 (continua) (continua)
```s