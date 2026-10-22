# Deelname aan het vrijdaggebed (Jumuʿah): belemmeringen, verplichting en deelname

Statistische analyse van een enquête onder volwassen moslims in Nederland (n = 35).
Toetst het mediatiemodel **praktische belemmeringen (X) → ervaren religieuze verplichting (M) → deelname aan Jumuʿah (Y)** met Hayes PROCESS Model 4. Daarnaast bevat het rapport KMO/Bartlett, factoranalyse, betrouwbaarheidsanalyse, kruistabellen en regressieanalyse.

> **Bekijk het rapport als webpagina:** https://yciftci111.github.io/jumuah/
>
> Alle cijfers in dit rapport worden opnieuw berekend door `scripts/` (zie [Reproduceren](#reproduceren)). De tabellen staan ook als CSV in [`output/tabellen`](output/tabellen).

![Padmodel](output/figuren/hayes_model4_padmodel.png)

## Inhoud
1. [Kernbevindingen](#1-kernbevindingen)
2. [Data en meetinstrument](#2-data-en-meetinstrument)
3. [KMO en Bartlett](#3-kmo-en-bartlett)
4. [Factoranalyse](#4-factoranalyse)
5. [Betrouwbaarheidsanalyse](#5-betrouwbaarheidsanalyse)
6. [Kruistabellen](#6-kruistabellen)
7. [Regressieanalyse](#7-regressieanalyse)
8. [Hayes PROCESS Model 4](#8-hayes-process-model-4)
9. [Beperkingen](#9-beperkingen)
10. [Reproduceren](#reproduceren)

---

## 1. Kernbevindingen

- **De schalen zijn bruikbaar.** De KMO-waarden per schaal zijn middelmatig tot verdienstelijk (0,71–0,81), Bartlett is overal significant en elke schaal is eendimensionaal volgens parallelle analyse. Belemmeringen (α = 0,83) en Deelname (α = 0,91) zijn goed betrouwbaar. Verplichting zit met α = 0,70 op de grens, en item M2 ("vooral iets wat ik zelf kan kiezen") is het zwakste item.
- **Meer belemmeringen gaan samen met minder deelname** (r = −0,56). **Meer ervaren verplichting gaat samen met meer deelname** (r = 0,76).
- **Er is sprake van gedeeltelijke mediatie.** Het indirecte effect via ervaren verplichting is klein maar betrouwbaar: ab = -0.218, 95%-bootstrap-BI [-0.448, -0.037]. Het directe effect van belemmeringen blijft ook significant (c′ = -0.42). Ongeveer 34% van het totale effect loopt via M.
- **Het a-pad is zwak.** Belemmeringen voorspellen ervaren verplichting maar marginaal (a = -0.20, p = .086). De mediatie hangt dus vooral af van het sterke b-pad. In de gevoeligheidsanalyse met het **feitelijk aantal bijgewoonde gebeden** als uitkomst is het indirecte effect niet significant.
- **Kruistabellen:** volledige deelname (4 van de laatste 4 vrijdagen) hangt samen met de vrijheid om werk of studie te onderbreken (73% tegenover 12%), met een lage score op belemmeringen en met een hoge score op verplichting. De vier vrouwen woonden geen van allen alle vier de gebeden bij, wat aansluit bij het fiqh-standpunt dat Jumuʿah voor vrouwen niet verplicht is.

## 2. Data en meetinstrument

Van de 37 ingevulde formulieren zijn er 2 uitgesloten omdat er geen toestemming was of de respondent niet tot de doelgroep behoorde. Er blijven **35 respondenten** over. Elke schaal bestaat uit zes Likert-items (1 = helemaal mee oneens … 5 = helemaal mee eens). Negatief geformuleerde items zijn omgescoord (aangeduid met `_r`). De schaalscore is het gemiddelde van de zes items. Hogere scores betekenen meer belemmeringen, meer verplichting en meer deelname.

| Schaal | Items | Omgescoord |
|---|---|---|
| X Praktische belemmeringen | X1–X6 | X2, X5 |
| M Ervaren religieuze verplichting | M1–M6 | M2, M4, M6 |
| Y Deelname aan Jumuʿah | Y1–Y6 | Y2, Y3 |
| Gedragsmaat | "Hoeveel van de afgelopen vier vrijdaggebeden heb je bijgewoond?" (0–4) | – |

### Steekproef
| Kenmerk               | Categorie                                       | n   | %    |
|:----------------------|:------------------------------------------------|:----|:-----|
| Geslacht              | Man                                             | 31  | 88.6 |
|                       | Vrouw                                           | 4   | 11.4 |
| Leeftijd              | 35–44 jaar                                      | 10  | 28.6 |
|                       | 25–34 jaar                                      | 9   | 25.7 |
|                       | 18–24 jaar                                      | 7   | 20.0 |
|                       | 45–54 jaar                                      | 6   | 17.1 |
|                       | 55–64 jaar                                      | 3   | 8.6  |
| Achtergrond           | Turks                                           | 18  | 51.4 |
|                       | Marokkaans                                      | 9   | 25.7 |
|                       | Nederlands                                      | 3   | 8.6  |
|                       | Anders                                          | 2   | 5.7  |
|                       | Egyptisch                                       | 1   | 2.9  |
|                       | Afghaans                                        | 1   | 2.9  |
|                       | Surinaams                                       | 1   | 2.9  |
| Gebruikelijke vrijdag | Ik werk op vrijdag                              | 18  | 51.4 |
|                       | Ik heb doorgaans geen werk of studie op vrijdag | 9   | 25.7 |
|                       | Mijn vrijdag wisselt per week                   | 5   | 14.3 |
|                       | Ik werk en studeer op vrijdag                   | 3   | 8.6  |
| Rechtsschool          | Hanafi                                          | 22  | 62.9 |
|                       | Maliki                                          | 8   | 22.9 |
|                       | Ik volg geen specifieke rechtsschool            | 2   | 5.7  |
|                       | Ik weet het niet                                | 1   | 2.9  |
|                       | Shafi‘i                                         | 1   | 2.9  |
|                       | Hanbali                                         | 1   | 2.9  |

### Beschrijvende statistiek
| Schaal                           | n   | M    | SD   | Min   | Max   | Scheefheid   |
|:---------------------------------|:----|:-----|:-----|:------|:------|:-------------|
| Praktische belemmeringen         | 35  | 2.05 | 0.85 | 1.0   | 3.83  | 0.65         |
| Ervaren religieuze verplichting  | 35  | 4.32 | 0.59 | 2.67  | 5.0   | -1.02        |
| Deelname aan Jumuʿah             | 35  | 4.14 | 0.96 | 2.0   | 5.0   | -0.93        |
| Bijgewoond (laatste 4 vrijdagen) | 34  | 3.15 | 1.28 | 0.0   | 4.0   | -1.42        |

M en Y zijn links-scheef: de meeste respondenten ervaren Jumuʿah als verplichting en wonen het vaak bij (plafondeffect).

### Correlaties (Pearson)
|                  | X Belemmeringen   | M Verplichting   | Y Deelname   | Bijgewoond (0–4)   |
|:-----------------|:------------------|:-----------------|:-------------|:-------------------|
| X Belemmeringen  | —                 |                  |              |                    |
| M Verplichting   | -0.29             | —                |              |                    |
| Y Deelname       | -0.56***          | 0.76***          | —            |                    |
| Bijgewoond (0–4) | -0.43*            | 0.43*            | 0.64***      | —                  |

\* p < .05 \*\* p < .01 \*\*\* p < .001

![Spreidingsdiagrammen](output/figuren/spreidingsdiagrammen.png)

## 3. KMO en Bartlett

| Schaal                          | Items   | KMO   | Bartlett χ²   | df   | p      |
|:--------------------------------|:--------|:------|:--------------|:-----|:-------|
| Praktische belemmeringen        | 6       | 0.707 | 91.2          | 15   | < .001 |
| Ervaren religieuze verplichting | 6       | 0.771 | 58.4          | 15   | < .001 |
| Deelname aan Jumuʿah            | 6       | 0.814 | 159.1         | 15   | < .001 |
| Alle 18 items                   | 18      | 0.657 | 516.2         | 153  | < .001 |

**Interpretatie.** Volgens Kaiser (1974) geldt een KMO ≥ 0,70 als "middelmatig" en ≥ 0,80 als "verdienstelijk". Alle drie de schalen zijn afzonderlijk geschikt voor factoranalyse, en Bartlett's toets is overal significant: de items correleren genoeg. Over alle 18 items samen is de KMO lager (0,66, "matig"). Daar liggen meerdere item-KMO's onder 0,50 (X4, X5_r, X1). Met n = 35 en 18 items (minder dan 2 respondenten per item) is een gezamenlijke factoranalyse daarom alleen verkennend te interpreteren.

## 4. Factoranalyse

Methode: principale-assenfactoranalyse (principal axis factoring). Het aantal factoren is bepaald met parallelle analyse (Horn, 95e percentiel, 1000 simulaties).

### 4a. Per schaal (eendimensionaliteit)

- **X Belemmeringen:** eigenwaarde factor 1 = 3.29 (55% verklaarde variantie); parallelle analyse adviseert 1 factor(en)
- **M Verplichting:** eigenwaarde factor 1 = 2.90 (48% verklaarde variantie); parallelle analyse adviseert 1 factor(en)
- **Y Deelname:** eigenwaarde factor 1 = 4.24 (71% verklaarde variantie); parallelle analyse adviseert 1 factor(en)

| Schaal   | Item   | Omschrijving                                       | Lading   | Communaliteit   | KMO item   |
|:---------|:-------|:---------------------------------------------------|:---------|:----------------|:-----------|
| X        | X1     | Werk/studie/verplichtingen maken Jumuʿah lastig    | 0.82     | 0.67            | 0.7        |
| X        | X2_r   | Kan vrijdag zo indelen dat er tijd is (r)          | 0.72     | 0.52            | 0.6        |
| X        | X3     | Bezwaard om ruimte te vragen                       | 0.83     | 0.69            | 0.69       |
| X        | X4     | Reis kost te veel tijd                             | 0.6      | 0.36            | 0.81       |
| X        | X5_r   | Geschikte plek goed bereikbaar (r)                 | 0.57     | 0.32            | 0.77       |
| X        | X6     | Tijdstip botst met andere verplichtingen           | 0.85     | 0.73            | 0.77       |
| M        | M1     | Meer dan gewoonte; religieuze plicht               | 0.8      | 0.64            | 0.8        |
| M        | M2_r   | Vooral iets wat ik zelf kan kiezen (r)             | 0.41     | 0.17            | 0.9        |
| M        | M3     | Ook bij volle agenda gaat Jumuʿah voor             | 0.89     | 0.8             | 0.71       |
| M        | M4_r   | Drukke dag is voldoende reden om over te slaan (r) | 0.75     | 0.56            | 0.76       |
| M        | M5     | Missen zonder geldige reden zit me dwars           | 0.55     | 0.3             | 0.77       |
| M        | M6_r   | Een keer missen religieus niet zo belangrijk (r)   | 0.67     | 0.44            | 0.84       |
| Y        | Y1     | Woon vrijwel iedere vrijdag bij                    | 0.84     | 0.7             | 0.78       |
| Y        | Y2_r   | Kom regelmatig voor dat ik niet bijwoon (r)        | 0.82     | 0.67            | 0.76       |
| Y        | Y3_r   | Bij drukke vrijdag sla ik soms over (r)            | 0.87     | 0.75            | 0.84       |
| Y        | Y4     | Regel vooraf waar en wanneer                       | 0.83     | 0.69            | 0.9        |
| Y        | Y5     | Zoek andere plek als ik onderweg ben               | 0.77     | 0.59            | 0.81       |
| Y        | Y6     | Zoek alsnog een manier bij onverwachte zaken       | 0.92     | 0.84            | 0.81       |

Elke schaal is eendimensionaal. Alle ladingen liggen ≥ 0,55, behalve M2_r (0,41, communaliteit 0,17).

### 4b. Alle 18 items samen (verkennend)

Kaiser-criterium (eigenwaarde > 1): 5 factoren; parallelle analyse (95e percentiel, 1000 simulaties): 2 factor(en). Eerste drie eigenwaarden: 7.90, 2.61, 1.33

![Scree-plot](output/figuren/scree_plot.png)

Hieronder staat de theoretisch verwachte 3-factoroplossing, met oblimin-rotatie en alleen ladingen ≥ |0,30|:

|                        | Omschrijving                                       | F1   | F2   | F3    |
|:-----------------------|:---------------------------------------------------|:-----|:-----|:------|
| X1                     | Werk/studie/verplichtingen maken Jumuʿah lastig    |      |      | 0.89  |
| X2_r                   | Kan vrijdag zo indelen dat er tijd is (r)          |      |      | 0.9   |
| X3                     | Bezwaard om ruimte te vragen                       |      | 0.76 | 0.31  |
| X4                     | Reis kost te veel tijd                             |      | 0.83 |       |
| X5_r                   | Geschikte plek goed bereikbaar (r)                 |      | 0.61 |       |
| X6                     | Tijdstip botst met andere verplichtingen           |      | 0.44 | 0.53  |
| M1                     | Meer dan gewoonte; religieuze plicht               | 0.72 |      |       |
| M2_r                   | Vooral iets wat ik zelf kan kiezen (r)             | 0.56 |      | 0.38  |
| M3                     | Ook bij volle agenda gaat Jumuʿah voor             | 0.96 |      |       |
| M4_r                   | Drukke dag is voldoende reden om over te slaan (r) | 0.7  |      |       |
| M5                     | Missen zonder geldige reden zit me dwars           |      |      | -0.35 |
| M6_r                   | Een keer missen religieus niet zo belangrijk (r)   | 0.61 | 0.36 |       |
| Y1                     | Woon vrijwel iedere vrijdag bij                    | 0.53 |      | -0.52 |
| Y2_r                   | Kom regelmatig voor dat ik niet bijwoon (r)        | 0.4  |      | -0.6  |
| Y3_r                   | Bij drukke vrijdag sla ik soms over (r)            | 0.77 |      |       |
| Y4                     | Regel vooraf waar en wanneer                       | 0.76 |      |       |
| Y5                     | Zoek andere plek als ik onderweg ben               | 0.8  |      |       |
| Y6                     | Zoek alsnog een manier bij onverwachte zaken       | 0.87 |      |       |
| % verklaarde variantie |                                                    | 31.8 | 12.3 | 16.7  |

Factorcorrelaties:

|    | F1    | F2    | F3    |
|:---|:------|:------|:------|
| F1 | 1.0   | -0.18 | -0.39 |
| F2 | -0.18 | 1.0   | 0.31  |
| F3 | -0.39 | 0.31  | 1.0   |

**Interpretatie.** De verwachte drie-schalenstructuur komt niet zuiver terug:
- **Verplichting en Deelname laden samen op F1.** Ze zijn empirisch slecht van elkaar te onderscheiden (r = 0,76). Dat komt deels door inhoudelijke overlap. Zo lijken M4 ("drukke dag is voldoende reden om over te slaan") en Y3 ("bij een drukke vrijdag sla ik soms over") sterk op elkaar.
- **Belemmeringen splitst in twee facetten:** *rooster/tijdsconflict* (X1, X2, X6; F3) en *toegang/drempel* (X3 bezwaard om te vragen, X4 reistijd, X5 bereikbaarheid; F2).
- Parallelle analyse adviseert maar 2 factoren. Bij deze steekproefgrootte is dat een advies om de schalen niet als volledig onafhankelijke constructen te behandelen. De schalen zijn wel inhoudelijk afzonderlijk gedefinieerd.

Voor de verdere analyses gebruiken we de theoretische schalen. Elke schaal is op zichzelf eendimensionaal en betrouwbaar. De overlap tussen M en Y nemen we mee als beperking (§9).

## 5. Betrouwbaarheidsanalyse

| Schaal                          | Items   | α     | 95%-BI       | Gem. inter-item r   |
|:--------------------------------|:--------|:------|:-------------|:--------------------|
| Praktische belemmeringen        | 6       | 0.828 | [0.72, 0.90] | 0.45                |
| Ervaren religieuze verplichting | 6       | 0.697 | [0.51, 0.83] | 0.36                |
| Deelname aan Jumuʿah            | 6       | 0.91  | [0.85, 0.95] | 0.65                |

95%-betrouwbaarheidsinterval volgens Feldt.

### Itemstatistieken
| Schaal   | Item   | M    | SD   | Item-rest r   | α als verwijderd   |
|:---------|:-------|:-----|:-----|:--------------|:-------------------|
| X        | X1     | 2.11 | 1.41 | 0.68          | 0.783              |
| X        | X2_r   | 1.8  | 1.02 | 0.57          | 0.806              |
| X        | X3     | 2.6  | 1.31 | 0.72          | 0.772              |
| X        | X4     | 1.97 | 1.12 | 0.47          | 0.825              |
| X        | X5_r   | 1.77 | 1.03 | 0.44          | 0.83               |
| X        | X6     | 2.06 | 1.0  | 0.74          | 0.776              |
| M        | M1     | 4.69 | 0.53 | 0.62          | 0.637              |
| M        | M2_r   | 3.71 | 1.47 | 0.27          | 0.772              |
| M        | M3     | 4.4  | 0.81 | 0.71          | 0.575              |
| M        | M4_r   | 4.2  | 0.76 | 0.54          | 0.631              |
| M        | M5     | 4.57 | 0.88 | 0.34          | 0.682              |
| M        | M6_r   | 4.37 | 0.91 | 0.44          | 0.653              |
| Y        | Y1     | 4.0  | 1.39 | 0.78          | 0.892              |
| Y        | Y2_r   | 4.03 | 1.32 | 0.76          | 0.894              |
| Y        | Y3_r   | 4.06 | 1.24 | 0.79          | 0.888              |
| Y        | Y4     | 4.17 | 1.1  | 0.73          | 0.896              |
| Y        | Y5     | 4.29 | 0.86 | 0.66          | 0.908              |
| Y        | Y6     | 4.31 | 0.96 | 0.86          | 0.883              |

**Interpretatie.** Belemmeringen (α = 0,83) en Deelname (α = 0,91) zijn goed tot uitstekend. Ervaren verplichting (α = 0,70) is net acceptabel. Zonder item **M2_r** stijgt α naar **0.772**. Item M2 ("Ik zie Jumuʿah vooral als iets wat ik zelf kan kiezen") meet waarschijnlijk iets anders, namelijk *autonomie/keuzebeleving* in plaats van verplichting. Respondenten kunnen het tegelijk als plicht én als eigen keuze ervaren. De gevoeligheidsanalyse in §8 laat zien dat de conclusies standhouden zonder M2.

## 6. Kruistabellen

Uitkomst: **volledige deelname** = alle 4 van de laatste 4 vrijdaggebeden bijgewoond (ja/nee). Categorieën zijn samengevoegd tot 2×2-tabellen omdat de celvullingen anders te klein worden. Getoetst is met Fisher's exacte toets, met φ als effectmaat (0,10 klein, 0,30 middelgroot, 0,50 groot).

| Rij × kolom                        | n   | χ²   | Toets        | p    | φ / Cramér's V   | % cellen E<5   |
|:-----------------------------------|:----|:-----|:-------------|:-----|:-----------------|:---------------|
| Geslacht × Volledige deelname      | 34  | 6.48 | Fisher exact | .022 | 0.44             | 50%            |
| Vrijdag × Volledige deelname       | 34  | 0.31 | Fisher exact | .704 | 0.1              | 25%            |
| Vrijheid × Volledige deelname      | 30  | 8.67 | Fisher exact | .009 | 0.54             | 50%            |
| Reistijd × Volledige deelname      | 34  | 2.33 | Fisher exact | .171 | 0.26             | 0%             |
| Moskeebezoek × Volledige deelname  | 34  | 1.2  | Fisher exact | .458 | 0.19             | 25%            |
| Belemmeringen × Volledige deelname | 34  | 7.2  | Fisher exact | .013 | 0.46             | 0%             |
| Verplichting × Volledige deelname  | 34  | 6.28 | Fisher exact | .017 | 0.43             | 0%             |
| Madhhab × Verplichting             | 30  | 6.14 | Fisher exact | .035 | 0.45             | 50%            |

**Geslacht × Volledige deelname** (n = 34; Fisher exact p = .022; φ = 0.44)

| Geslacht   | < 4      | 4 van 4   | Totaal   |
|:-----------|:---------|:----------|:---------|
| Man        | 10 (33%) | 20 (67%)  | 30       |
| Vrouw      | 4 (100%) | 0 (0%)    | 4        |

**Vrijdag × Volledige deelname** (n = 34; Fisher exact p = .704; φ = 0.10)

| Vrijdag                | < 4      | 4 van 4   | Totaal   |
|:-----------------------|:---------|:----------|:---------|
| Geen werk/studie       | 3 (33%)  | 6 (67%)   | 9        |
| Werk/studie op vrijdag | 11 (44%) | 14 (56%)  | 25       |

**Vrijheid × Volledige deelname** (n = 30; Fisher exact p = .009; φ = 0.54)

| Vrijheid      | < 4     | 4 van 4   | Totaal   |
|:--------------|:--------|:----------|:---------|
| Hooguit enige | 7 (88%) | 1 (12%)   | 8        |
| Veel/volledig | 6 (27%) | 16 (73%)  | 22       |

**Reistijd × Volledige deelname** (n = 34; Fisher exact p = .171; φ = 0.26)

| Reistijd   | < 4      | 4 van 4   | Totaal   |
|:-----------|:---------|:----------|:---------|
| < 10 min   | 4 (27%)  | 11 (73%)  | 15       |
| ≥ 10 min   | 10 (53%) | 9 (47%)   | 19       |

**Moskeebezoek × Volledige deelname** (n = 34; Fisher exact p = .458; φ = 0.19)

| Moskeebezoek         | < 4     | 4 van 4   | Totaal   |
|:---------------------|:--------|:----------|:---------|
| Minder dan wekelijks | 6 (55%) | 5 (45%)   | 11       |
| Minstens wekelijks   | 8 (35%) | 15 (65%)  | 23       |

**Belemmeringen × Volledige deelname** (n = 34; Fisher exact p = .013; φ = 0.46)

| Belemmeringen    | < 4      | 4 van 4   | Totaal   |
|:-----------------|:---------|:----------|:---------|
| Hoog (> mediaan) | 10 (67%) | 5 (33%)   | 15       |
| Laag (≤ mediaan) | 4 (21%)  | 15 (79%)  | 19       |

**Verplichting × Volledige deelname** (n = 34; Fisher exact p = .017; φ = 0.43)

| Verplichting     | < 4      | 4 van 4   | Totaal   |
|:-----------------|:---------|:----------|:---------|
| Hoog (> mediaan) | 3 (19%)  | 13 (81%)  | 16       |
| Laag (≤ mediaan) | 11 (61%) | 7 (39%)   | 18       |

**Madhhab × Verplichting** (n = 30; Fisher exact p = .035; φ = 0.45)

| Madhhab   | Hoog (> mediaan)   | Laag (≤ mediaan)   | Totaal   |
|:----------|:-------------------|:-------------------|:---------|
| Hanafi    | 14 (64%)           | 8 (36%)            | 22       |
| Maliki    | 1 (12%)            | 7 (88%)            | 8        |

**Interpretatie.**
- **Vrijheid om werk/studie te onderbreken** is de sterkste praktische factor (φ = 0,54). Van de mensen met hooguit enige vrijheid woonde maar 1 op de 8 alle vier gebeden bij.
- **Of iemand op vrijdag werkt** maakt op zichzelf weinig uit (p = .70). Het gaat dus om *flexibiliteit*, niet om het hebben van werk.
- Een **korte reistijd** (< 10 min) en **wekelijks moskeebezoek** wijzen in de verwachte richting, maar zijn niet significant bij deze n.
- **Geslacht:** geen van de vier vrouwen woonde alle vier gebeden bij. Dat past bij het fiqh-standpunt dat Jumuʿah voor vrouwen niet verplicht is. Daarom is de mediatieanalyse in §8 ook voor alleen mannen herhaald.
- **Madhhab:** Hanafi-respondenten scoren vaker hoog op verplichting dan Maliki-respondenten. Met 8 Maliki's, onder wie 2 vrouwen, en een overlap met achtergrond (Turks/Marokkaans) is dit verband niet causaal te duiden. Het is wel een interessant punt voor vervolgonderzoek.

## 7. Regressieanalyse

Hiërarchische OLS-regressie met **Y Deelname (schaal)** als afhankelijke variabele (n = 35). Standaardfouten zijn HC3-robuust. β is gestandaardiseerd (voor dummy's: B / SD<sub>Y</sub>).

| Predictor                       | Model 1 B (SE)   | Model 1 β   | Model 2 B (SE)   | Model 2 β   | Model 3 B (SE)   | Model 3 β   |
|:--------------------------------|:-----------------|:------------|:-----------------|:------------|:-----------------|:------------|
| Constante                       | 5.45 (0.25)***   |             | 0.40 (0.61)      |             | 0.20 (1.23)      |             |
| X Belemmeringen                 | -0.64 (0.14)***  | -0.56       | -0.42 (0.09)***  | -0.37       | -0.32 (0.17)     | -0.28       |
| M Verplichting                  |                  |             | 1.06 (0.11)***   | 0.65        | 1.01 (0.31)**    | 0.62        |
| Geslacht (man = 1)              |                  |             |                  |             | 0.47 (0.76)      | 0.49        |
| Werk/studie op vrijdag (ja = 1) |                  |             |                  |             | -0.27 (0.30)     | -0.28       |
| R² (adj. R²)                    | 0.317 (0.296)    |             | 0.707 (0.688)    |             | 0.736 (0.701)    |             |
| ΔR²                             | 0.317            |             | 0.390            |             | 0.030            |             |

\* p < .05 \*\* p < .01 \*\*\* p < .001 (HC3)

R²-verandering: Model 1 → 2: F(1, 32) = 42.53, p < .001; Model 2 → 3: F(2, 30) = 1.68, p = .203.

**Interpretatie.** Belemmeringen verklaren 32% van de variantie in deelname. Ervaren verplichting voegt daar nog eens 39% aan toe, tot R² = 0,71. Beide predictoren zijn uniek significant, en verplichting is de sterkste (β = 0,65 tegenover −0,37). Geslacht en vrijdagwerk voegen niets significants toe (ΔR² = 0,03). In Model 3 is het effect van belemmeringen met robuuste SE's niet meer significant (p ≈ .06), omdat dummy's met kleine groepen (4 vrouwen) de schattingen instabiel maken.

**Assumpties (Model 2):** VIF = 1.10 (beide predictoren); Shapiro-Wilk residuen W = 0.750, p < .001; Breusch-Pagan χ²(2) = 0.38, p = .829; maximale Cook's D = 0.16 (2 cases boven 4/n). Er is geen multicollineariteit en geen heteroscedasticiteit. De residuen zijn niet normaal verdeeld door het plafondeffect in Y. Daarom zijn HC3-standaardfouten gebruikt, en voor het indirecte effect bootstrapping (§8), dat geen normaliteit veronderstelt.

### Robuustheid: gedragsmaat (aantal bijgewoond, 0–4; n = 34)

| Predictor       | OLS B (SE)   | OLS p   | Binomiaal OR [95%-BI]   | Binomiaal p   |
|:----------------|:-------------|:--------|:------------------------|:--------------|
| X Belemmeringen | -0.50 (0.28) | .075    | 0.45 [0.26, 0.76]       | .003          |
| M Verplichting  | 0.71 (0.46)  | .127    | 2.90 [1.41, 5.99]       | .004          |

Met een binomiaal model (k van 4 gebeden), dat bij deze uitkomst past, zijn beide predictoren significant. Elk punt meer op belemmeringen halveert ruwweg de odds om een gebed bij te wonen (OR = 0,45). Elk punt meer op verplichting verdrievoudigt ze ongeveer (OR = 2,90). De lineaire OLS-schatting (R² = 0.285) is met HC3 niet significant. Dat komt door de scheve, begrensde verdeling van deze maat.

## 8. Hayes PROCESS Model 4

Eenvoudige mediatie. Het is een OLS-padanalyse, gelijk aan PROCESS v4 Model 4 in SPSS/R. Het indirecte effect is getoetst met **5000 percentiel-bootstrapsteekproeven** (seed 20261022). Een indirect effect is significant als het 95%-BI geen 0 bevat.

| Pad                           | B      | SE    | t     | p      | 95%-BI           |
|:------------------------------|:-------|:------|:------|:-------|:-----------------|
| a  (X → M)                    | -0.205 | 0.116 | -1.77 | .086   | [-0.440, 0.030]  |
| b  (M → Y | X)                | 1.065  | 0.163 | 6.52  | < .001 | [0.732, 1.398]   |
| c' (X → Y | M, direct)        | -0.419 | 0.114 | -3.69 | < .001 | [-0.650, -0.188] |
| c  (X → Y, totaal)            | -0.637 | 0.163 | -3.91 | < .001 | [-0.969, -0.306] |
| ab (indirect, bootstrap)      | -0.218 | 0.104 |       |        | [-0.448, -0.037] |
| ab volledig gestandaardiseerd | -0.193 |       |       |        | [-0.396, -0.033] |

Model M: R² = 0.087, F(1, 33) = 3.14, p = .086; Model Y: R² = 0.707, F(2, 32) = 38.53, p < .001.

![Bootstrapverdeling](output/figuren/hayes_bootstrap_verdeling.png)

### Gevoeligheidsanalyses
| Specificatie                          | n   | a      | b     | c'     | ab [95%-BI]             | Indirect ≠ 0?   |
|:--------------------------------------|:----|:-------|:------|:-------|:------------------------|:----------------|
| Hoofdanalyse (Y = deelnameschaal)     | 35  | -0.20  | 1.06* | -0.42* | -0.218 [-0.448, -0.037] | ja              |
| Met covariaten geslacht + vrijdagwerk | 35  | -0.24  | 1.01* | -0.32* | -0.248 [-0.671, -0.019] | ja              |
| Alleen mannen                         | 31  | -0.22* | 1.03* | -0.43* | -0.225 [-0.512, -0.025] | ja              |
| Y = aantal bijgewoond (0–4)           | 34  | -0.21  | 0.71* | -0.50* | -0.145 [-0.424, 0.056]  | nee             |
| M zonder item M2 (schaal 5 items)     | 35  | -0.29* | 1.23* | -0.28* | -0.361 [-0.647, -0.174] | ja              |

\* p < .05 (klassieke OLS-SE's, zoals in PROCESS)

### Interpretatie

1. **Totaal effect (c):** meer praktische belemmeringen hangen samen met minder deelname (c = -0.64, p < .001).
2. **a-pad:** mensen die meer belemmeringen ervaren, voelen Jumuʿah iets minder als bindende verplichting (a = -0.20). Dit pad is in de hoofdanalyse marginaal (p = .086) en alleen bij mannen significant.
3. **b-pad:** bij gelijke belemmeringen voorspelt ervaren verplichting deelname sterk (b = 1.06, p < .001).
4. **Indirect effect (ab):** -0.218, 95%-BI [-0.448, -0.037]. Het BI bevat geen 0, dus er is **significante mediatie**. Volledig gestandaardiseerd: ab<sub>cs</sub> = -0.193, een klein tot middelgroot effect.
5. **Direct effect (c′):** blijft significant (-0.42), dus er is **gedeeltelijke (complementaire) mediatie**. Belemmeringen werken vooral direct op deelname, en voor een kleiner deel (34%) via een verzwakte verplichtingsbeleving.

**Robuustheid.** Het indirecte effect blijft significant met covariaten, bij alleen mannen en zonder item M2. Bij de laatste specificatie is het zelfs sterker. Het effect is **niet** significant als Y het *gerapporteerde aantal* bijgewoonde gebeden is (BI bevat 0). Het indirecte effect is daarom het best te verdedigen voor de attitudinale deelnameschaal, en minder voor het feitelijke gedrag in de afgelopen maand.

**Voorbeeldrapportage (APA).**
> Een mediatieanalyse met PROCESS Model 4 (Hayes, 2022; 5000 bootstraps) liet zien dat praktische belemmeringen negatief samenhingen met deelname aan Jumuʿah, *c* = -0.64, *p* < .001. Belemmeringen voorspelden ervaren religieuze verplichting marginaal, *a* = -0.20, *p* = .086. Ervaren verplichting voorspelde deelname sterk, *b* = 1.06, *p* < .001. Het indirecte effect was significant, *ab* = -0.218, 95%-BI [-0.448, -0.037], en het directe effect bleef significant, *c′* = -0.42, *p* < .001. Dit wijst op gedeeltelijke mediatie.

## 9. Beperkingen

- **Kleine steekproef (n = 35).** Dat geeft weinig power voor het a-pad, onstabiele factoroplossingen en kleine celvullingen in de kruistabellen. Resultaten zijn verkennend.
- **Cross-sectioneel ontwerp.** Mediatie veronderstelt een causale volgorde X → M → Y, maar die is niet aangetoond. Het omgekeerde is ook plausibel: wie vaak gaat, ervaart het sterker als plicht en belemmeringen als kleiner.
- **Overlap M en Y.** De twee schalen correleren 0,76 en laden in de gezamenlijke factoranalyse op één factor. Een deel van het b-pad kan dus gedeelde methodevariantie of inhoudelijke overlap zijn, en geen echte mediatie.
- **Plafondeffecten** in M en Y, en niet-normale residuen.
- **Samenstelling.** Overwegend mannen (89%) met een Turkse of Marokkaanse achtergrond. Werving via eigen netwerk/moskee leidt waarschijnlijk tot een selectie van relatief religieus betrokken respondenten.

## Reproduceren

```bash
pip install -r requirements.txt
python scripts/01_data_voorbereiden.py   # leest data/Antwoorden_Enquete_Jumuah.xlsx
python scripts/02_analyses.py            # alle analyses → output/
python scripts/03_rapport.py             # bouwt deze README opnieuw op
python scripts/04_website.py             # bouwt index.html (GitHub Pages)
```

```
├── data/                  # NIET gepubliceerd (zie Privacy)
├── scripts/
│   ├── 01_data_voorbereiden.py
│   ├── 02_analyses.py
│   ├── 03_rapport.py
│   └── rapport_sjabloon.md
├── output/
│   ├── figuren/           # PNG-figuren
│   └── tabellen/          # alle tabellen als CSV
├── index.html             # webpagina voor GitHub Pages
└── README.md              # dit rapport
```

### Privacy
De ruwe enquêtedata bevat bijzondere persoonsgegevens (religie, AVG art. 9) en open antwoorden. Met n = 35 kunnen respondenten met een unieke combinatie van kenmerken herleidbaar zijn. Daarom staat `data/` in `.gitignore` en publiceert deze repository alleen geaggregeerde resultaten.

### Literatuur
- Hayes, A. F. (2022). *Introduction to mediation, moderation, and conditional process analysis* (3rd ed.). Guilford Press.
- Horn, J. L. (1965). A rationale and test for the number of factors in factor analysis. *Psychometrika, 30*, 179–185.
- Kaiser, H. F. (1974). An index of factorial simplicity. *Psychometrika, 39*, 31–36.
- Feldt, L. S. (1965). The approximate sampling distribution of Kuder-Richardson reliability coefficient twenty. *Psychometrika, 30*, 357–370.
