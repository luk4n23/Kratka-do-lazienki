# Kratka narożna — obudowa pionu instalacyjnego

Interaktywna wizualizacja 3D detalu do cięcia laserowego. Obracanie, przybliżanie,
przełączanie ściany, wkrętów i perforacji, zbliżenie na naroże.

## Uruchomienie

Strona jest w pełni samodzielna — wystarczy otworzyć `index.html` w przeglądarce.

Żeby udostępnić ją online przez GitHub Pages:

1. Wrzuć zawartość tego katalogu do repozytorium (gałąź `main`, katalog główny).
2. W repozytorium: **Settings → Pages → Source: Deploy from a branch → main / (root)**.
3. Po kilkudziesięciu sekundach strona jest pod `https://<użytkownik>.github.io/<repo>/`.

Biblioteka three.js wczytuje się z cdnjs, więc strona wymaga połączenia z internetem.

## Zawartość

```
index.html                                        wizualizacja 3D
pliki/kratka-naroznik_rysunek-techniczny_DC01.pdf rysunek techniczny A3
pliki/kratka-naroznik_gr1.5mm_1szt_DC01.pdf       szybki podgląd detalu
pliki/kratka-naroznik_gr1.5mm_1szt_DC01.dxf       rozwinięcie do cięcia
```

## Parametry detalu

| | |
|---|---|
| Materiał | DC01, grubość 1,5 mm |
| Wykończenie | malowanie proszkowe RAL 9003 (biały) |
| Gabaryt po gięciu | 140 × 90 × 2430 mm (szer. × głęb. × wys.) |
| Rozwinięcie | 309,57 × 2430 mm |
| Masa | 6,76 kg / szt. |
| Perforacja | otwory ⌀16, podziałka 23 mm, układ przestawny 60° |
| Mostek | 7,0 mm (4,7 × grubości blachy) |
| Powierzchnia otwarta | 38 % |
| Gięcie | 4 × 90°, promień wewnętrzny R1,5 mm |
| Cięcie laserowe | 50,2 m konturu, 900 przebić |
| Mocowanie | 2 × 7 otworów ⌀6,5 w kołnierzach przyściennych |

Profil: kołnierz 20 — bok 90 — lico 100 — bok 90 — kołnierz 20. Jeden element gięty,
bez spawania i bez nitowania.

## Kolejność gięcia

| nr | element | linia x [mm] | kąt | kierunek |
|---|---|---|---|---|
| 1 | kołnierz A | 18,70 | 90° | w dół |
| 2 | kołnierz B | 290,88 | 90° | w dół |
| 3 | naroże lewe | 106,09 | 90° | w górę |
| 4 | naroże prawe | 203,48 | 90° | w górę |

Najpierw oba kołnierze na płasko, dopiero potem oba naroża — kołnierze gną się
w przeciwną stronę niż naroża.

Rozwinięcie policzone przy R1,5 mm i współczynniku K = 0,44 (odcięcie na gięcie
2,607 mm). Przy innym K-factorze prasy rozwinięcie trzeba przeliczyć.

Perforacja kończy się 12,7 mm przed każdym narożem, przy wymaganym minimum
R + 2t = 4,5 mm — gięcie jej nie deformuje.

## Uwagi produkcyjne

- Plik DXF zawiera **wyłącznie warstwę `CIECIE`**, wszystkie kontury zamknięte.
  Linii gięcia w DXF nie ma — są opisane w rysunku technicznym i w podglądzie PDF.
- Prasa krawędziowa musi mieć długość roboczą min. 2430 mm.
- Z arkusza 1250 × 2500 wychodzą 3 szt., z 1500 × 3000 — 4 szt.

---

ULAMEX · Zawada 144 · 97-200 Tomaszów Mazowiecki
