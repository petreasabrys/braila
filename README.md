# Brăila 2028 – Simulator de reorganizare administrativă

Simulator de reorganizare administrativă pentru cele 44 de unități administrativ-teritoriale din județul Brăila.
Arată, pentru fiecare UAT și pentru orice grupare de UAT-uri, cât din cheltuieli poate fi acoperit din venituri proprii.

## Ce face

- **Hartă actuală** – UAT-urile colorate după ce acoperă veniturile proprii: aparatul primăriei, tot personalul sau toată funcționarea. Atingi o comună și vezi fișa completă de indicatori.
- **Construiește zone** – grupezi comunele cu un clic și vezi indicatorii zonei după comasare, inclusiv economia estimată la aparatul primăriilor.
- **Propunere automată** – comasează UAT-urile vecine până trec de un prag de populație.
- **Surse** – metodologia, sursele și importul opțional de date proprii.

## Date și metodologie

Toate datele financiare sunt calculate din rapoartele oficiale ale **Ministerului Finanțelor**: execuție bugetară COFOG3, agregat la nivel de ordonator principal, bugetul local, la 31.12.2025. Câte un raport pentru fiecare dintre cele 44 de UAT. Valorile calculate sunt în `date_mf_2025.csv`.

| Indicator | Definiție |
|---|---|
| Venituri proprii | art. 5 din Legea 273/2006: capitolele de venituri 01–03, 05–07, 12, 14–16, 18, 30–31, 33–36 + cote defalcate din impozitul pe venit (04.01) |
| Aparatul primăriei | cheltuieli de personal (titlul 10) ale autorităților executive (cap. 51.01) |
| Personal total | cheltuieli de personal (titlul 10), toate capitolele |
| Funcționare / Dezvoltare | secțiunile de funcționare și de dezvoltare ale bugetului local |
| Cheltuieli descentralizate | sume defalcate din TVA (11.02) pentru învățământ, asistență socială, protecția copilului |
| Sume de echilibrare | 04.02, 04.04, 04.05, 11.06 |

Populație: INS, Recensământul Populației și Locuințelor 2021. Contururi: © OpenStreetMap contributors.

Ideea unei hărți interactive a comasării UAT pornește de la proiectul [Reformă Administrativă](https://cosettechichirau.github.io/reformaadm/) realizat de Cosette Chichirău. Datele și calculele din această aplicație sunt refăcute integral din sursele oficiale de mai sus.

## Contururile UAT

La prima pornire aplicația descarcă limitele comunelor din OpenStreetMap. Ca să pornească instant pentru toți vizitatorii: fila **Surse → Salvează braila_uat.geojson**, apoi urcă fișierul în repository lângă `index.html`.

## Publicare

GitHub Pages: Settings → Pages → Deploy from a branch → `main` / `(root)`.
