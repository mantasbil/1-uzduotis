# 1 užduotis

# Visos programos veikimas

1. Pasirenkama, ar bus automatiškai generuojamas failas ir matuojama jo nuskaitymo ir duomenų surūšiavimo į dvi grupes sparta. Jei taip, įvedamas norimas duomenų kiekis, programa sukuria failą su nurodytu skaičiumi studentų (faile saugomi studento vardas, pavardė ir galutinis balas), jį nuskaito. Į ekraną išvedamas failo nuskaitymo laikas.
2. Pasirenkama studentų rūšiavimo į dvi grupes pagal galutinį pažymį strategija: 1) kuriami du vektoriai 'vargsiukai' ir 'galvociai'; 2) studentai, su mažesniu už 5 galutiniu pažymiu, perkeliami į konteinerį 'vargsiukai' ir ištrinami iš pradinio konteinerio. Į ekraną išvedamas studentų dalijimo į atskiras grupes laikas. Surūšiuoti duomenys išvedami į du atskirus failus.
3. Jei pasirenkama nematuoti spartos, prašoma pasirinkti, ar duomenys bus nuskaitomi iš failo, ar įvedami ranka.
4. Jei pasirenkamas nuskaitymas iš failo, duomenys nuskaitomi iš failo, kurio pavadinimas privalo būti "kursiokai.txt" ir kuris privalo būti patalpintas toje pačioje direktorijoje kaip ir programa. Jei toks failas randamas, duomenys nuskaitomi į vektorių ir dviem būdais suskaičiuojamas galutinis pažymys - pagal namų darbų pažymių vidurkį ir pagal medianą.
5. Jei pasirenkamas įvedimas ranka, prašoma pasirinkti, ar namų darbų ir egzamino pažymiai bus įvedami ranka, ar generuojami automatiškai.
6. Abiem atvejais įvedamas studentų kiekis; Prašoma įvesti studento vardą ir pavardę. Pasirinkus automatinį generavimą kiekvienam studentui reikia įvesti namų darbų pažymių kiekį, pasirinkus rankinį įvedimą veiksmas stabdomas įvedus bet kokį simbolį, kuris nėra skaičius. Abiem atvejais kiekvieno studento galutinis pažymys suskaičiuojamas dviem būdais - pagal namų darbų pažymių vidurkį ir pagal medianą.
7. Prašoma pasirinkti, kokio tipo galutinis balas bus išvedamas į ekraną.
8. Į ekraną išvedamas studentų sąrašas, surūšiuotas abėcėlės tvarka pagal pavardes, su pasirinkto tipo galutiniais pažymiais.

## v0.1

Programa realizuota dviem būdais:
- Kiekvieno studento namų darbų įvertinimai ir informacija apie visus studentus (vardas, pavardė, namų darbų įvertinimai, egzamino įvertinimas, galutinis pažymys) saugomi dinaminiuose masyvuose [uzd1.cpp](https://github.com/mantasbil/1-uzduotis/blob/v0.1/uzd1/uzd1.cpp).
- Kiekvieno studento namų darbų įvertinimai ir informacija apie visus studentus (vardas, pavardė, namų darbų įvertinimai, egzamino įvertinimas, galutinis pažymys) saugomi vektoriuose [uzd1_vect.cpp](https://github.com/mantasbil/1-uzduotis/blob/v0.1/uzd1_vect/uzd1_vect.cpp).

Programos veikimas:
1. Įvedamas studentų skaičius.
2. Įvedamas studento vardas ir pavardė. Tiek vardas, tiek pavardė turi susidėti tik iš raidžių.
3. Pasirenkama, ar pažymiai bus įvedami vartotojo, ar generuojami automatiškai. Pasirinkus automatinį generavimą, reikia įvesti namų darbų pažymių kiekį. Pasirinkus rankinį įvedimą realizacijoje su masyvu įvedamas stabdomas įvedus -1, realizacijoje su vektoriumi įvedimas stabdomas paspaudus bet kokį simbolį, kuris nėra skaičius. Privaloma įvesti bent vieną pažymį.
4. Programa dviem būdais apskaičiuoja studento galutinį pažymį
   - Galutinis = 0.4 * namų_darbų_vidurkis + 0.6 * egzaminas
   - Galutinis = 0.4 * namų_darbų_vidurkis + 0.6 * mediana
5. Pasirenkama, ar į ekraną bus išvedamas galutinis pažymys, apskaičiuotas pagal namų darbų vidurkį, ar pagal medianą.
6. Į ekraną išvedami visų įvestų studentų vardai ir pavardės kartu su jų galutiniu pažymiu, suapvalintu iki dviejų skaičių po kablelio.

## v0.2

Patobulinta v0.1 realizacija, naudojant vektorius. Išlaikytas visas v0.1 funkcionalumas, pridėta daugiau galimybių.

Naujos galimybės:
- Duomenų nuskaitymas iš failo. Failas, kuriame saugomi duomenys privalo vadintis "kursiokai.txt". Nuskaitant iš failo, visi studentai turi vienodą namų darbų kiekį.
- Studentai išvedami į ekraną pagal pavardes abėcėlės tvarka. Jei kelių studentų pavardės sutampa, jie vedami abėcėlės tvarka pagal vardą.

## v0.3

Kas naujo:
- Patobulintas atsitiktinių pažymių generavimas (panaudota random biblioteka).
- Funkcijos ir struktūros perkeltos į antraštinius (header) failus.
- Pridėtas išimčių valdymas.

## v0.4

Kas naujo:
- Pridėta galimybė matuoti programos spartą. Pasirinkus šią funkciją:
1. Sukuriamas failas su nurodytu įrašų kiekiu;
2. Studentų duomenys iš failo nuskaitomi į vektorių;
3. Studentai surūšiuojami į atskirus vektorius pagal galutinį pažymį (jei pažymys <5, studentas įrašomas į vektorių "vargsiukai", jei >=5 - į vektorių "galvociai");
4. Surūšiuoti duomenys surašomi į du atskirus failus.

Matuojamas visų išvardintų veiksmų atlikimo laikas.
Lentelėje pateiktas veiksmų atlikimo laikas sekundėmis (buvo matuojama 5 kartus ir apskaičiuotas vidurkis).

| Veiksmas | 1000 | 10000 | 100000 | 1000000 | 10000000 |
| :-----------: | :----: | :-----: | :------: | :-------: | :--------: |
| Failo sukūrimas | 0.0149078 s | 0.1488042 s | 1.371526 s | 11.066468 s | 95.23038 s |
| Failo nuskaitymas | 0.0173255 s | 0.05737364 s | 0.3141988 s | 3.35643 s | 26.56298 s |
| Surūšiavimas | 0.00014238 s | 0.00110076 s | 0.00683444 s | 0.3448565 s | 0.6112206 s |
| "Vargšiukų" įrašymas | 0.00661396 s | 0.08006498 s | 0.3971122 s | 4.079972 s | 36.68192 s |
| "Galvočių" įrašymas | 0.01121306 s | 0.0791899 s | 0.5140312 s | 5.04828 s | 45.87368 s |
| Visas testo laikas | 0.05541176 s | 0.4070714 s | 2.610388 s | 23.63446 s | 204.9688 s |

## v0.5

Atliktas Vector ir List struktūrų spartos palyginimas nuskaitant duomenis iš failo ir surūšiuojant juos.

Lentelėse pateikti rezultatai (sparta buvo matuojama 5 kartus ir apskaičiuotas vidurkis).

Sistemos parametrai: CPU - Intel Core i5-4200U @ 1.60GHz 2.30GHz; RAM - 8 GB; SSD - 512 GB

- Duomenų nuskaitymas iš failo:

| Struktūra | 1000 | 10000 | 100000 | 1000000 | 10000000 |
| :-----------: | :----: | :-----: | :------: | :-------: | :--------: |
| Vector | 0.0059696 s | 0.04333816 s | 0.3261778 s | 3.336214 s | 27.04606 s |
| List | 0.0178328 s | 0.04746584 s | 0.3186326 s | 3.369412 s | 28.52392 s |

- Studentų surūšiavimas į dvi grupes:

| Struktūra | 1000 | 10000 | 100000 | 1000000 | 10000000 |
| :-----------: | :----: | :-----: | :------: | :-------: | :--------: |
| Vector | 0.0001387 s | 0.00108648 s | 0.00593302 s | 0.0776995 s | 0.586172 s |
| List | 0.0005563 s | 0.00311996 s | 0.02979978 s | 0.3606842 s | 2.921546 s |

Matome, kad duomenų nuskaitymo iš failo laikas naudojant skirtingas struktūras buvo gana panašus, tačiau duomenų rūšiavimas buvo gerokai spartesnis naudojant Vector struktūrą.

## v1.0

Palygintos dvi studentų dalijimo į dvi grupes strategijos:
1. Studentai dedami į du konteinerius ('vargsiukai' ir 'galvociai') pagal jų galutinį pažymį;
2. Studentai su pažymiu, mažesniu už 5, perkeliami į konteinerį 'vargsiukai' ir ištrinami iš pradinio konteinerio 'studentai'. Konteineryje 'studentai' lieka tik studentai, turintys ne žemesnį nei 5 galutinį balą, tai atitinka 1-oje strategijoje sukurtą konteinerį 'galvociai'.

Rūšiavimo laikai:

| Struktūra | Skirstymo būdas | 1000 | 10000 | 100000 | 1000000 | 10000000 |
| :-----------: | :---: | :----: | :-----: | :------: | :-------: | :--------: |
| Vector | 1 | 0.0000706 s | 0.0008961 s | 0.0057949 s | 0.0535999 s | 0.5808936 s |
| Vector | 2 | 0.0000555 s | 0.0004618 s | 0.0044573 s | 0.0521368 s | 0.437237 s |
| List | 1 | 0.0003194 s | 0.0027364 s | 0.0259439 s | 0.2712942 s | 2.859808 s |
| List | 2 | 0.0001270 s | 0.0009704 s | 0.0188149 s | 0.2496906 s | 2.796786 s |

Skirstant studentas 2-a strategija buvo pasiekti šiek tiek geresni rezultatai.
