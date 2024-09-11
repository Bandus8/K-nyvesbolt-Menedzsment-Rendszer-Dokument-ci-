

# Könyvesbolt Menedzsment Rendszer Dokumentáció

## Tartalomjegyzék

1. [Bevezetés](#bevezetes)
    - [Projekt Háttér](#projekt-hatter)
    - [A Projekt Céljai](#a-projekt-celjai)
    - [A Projekt Hatóköre](#a-projekt-hatokore)
    - [A Projekt Alkalmazhatósága](#a-projekt-alkalmazhatosaga)
2. [Követelmények és Elemzés](#kovetelmenyek-es-elemzes)
    - [Probléma Megfogalmazása](#problema-megfogalmazasa)
    - [Követelmények Meghatározása](#kovetelmenyek-meghatarozasa)
    - [Hardver Követelmények](#hardver-kovetelmenyek)
    - [Szoftver Követelmények](#szoftver-kovetelmenyek)
3. [Rendszer Tervezés](#rendszer-tervezes)
    - [Általános Rendszerterv](#altalanos-rendszerterv)
    - [Adat Szótár](#adat-szotar)
    - [Bemenet/Kimenet Tervezés](#bemenet-kimenet-tervezes)
4. [Tesztelés és Megvalósítás](#teszteles-es-megvalositas)
    - [Alkalmazott Tesztelési Módszerek](#alkalmazott-tesztelesi-modszerek)
    - [Teszt Esetek](#teszt-esetek)
5. [Következtetés](#kovetkeztetes)
    - [A Rendszer Korlátai](#a-rendszer-korlatai)
    - [A Rendszer Jövőbeli Fejlődési Irányai](#a-rendszer-jovobeli-fejlodesi-iranyai)
    - [Irodalomjegyzék](#irodalomjegyzek)

---

## Bevezetés

### Projekt Háttér

Ez a szoftver lehetővé teszi az Admin számára, hogy könyv- és ügyféladatokat tároljon, könnyebb hozzáférést biztosítva az olyan adatokhoz, mint az ügyfelek nyilvántartásai és a könyvek elérhetősége. A projekt célja a könyvesbolt menedzsmentjének számítógépesítése.

### A Projekt Céljai

- A papírmunkák csökkentése és a rendszer számítógépesítése.
- Működési sebesség növelése, gyorsabb és pontosabb keresést biztosítva.
- Nagy mennyiségű adat tárolása adatbázisban.
- A könyvvásárlás manuális folyamatának egyszerűsítése és automatizálása.

### A Projekt Hatóköre

A rendszer célja a túlóra fizetések csökkentése és a pontos nyilvántartások biztosítása, valamint helyes keresési eredmények nyújtása. Rugalmasságot biztosít az adminisztrátorok számára, és minden szinten felhasználók számára elérhető.

### A Projekt Alkalmazhatósága

- Az ügyfelek bármikor, bárhonnan vásárolhatnak könyveket.
- Az adminisztrátorok hozzáadhatják a könyvek adatait a rendszerhez.
- Az adatbázis biztosítja a könyvnyilvántartások biztonságos tárolását.

---

## Követelmények és Elemzés

### Probléma Megfogalmazása

- Túl sok papírmunka.
- Időigényes folyamatok.
- Magasabb költségek a manuális nyilvántartások karbantartásában.
- A rekordok manuális keresése fárasztó.
- A manuális folyamatok lassúak és pontatlanok.

### Követelmények Meghatározása

A rendszer két fő modult tartalmaz:

1. **Admin Modul**:
    - Könyvkategóriák bejegyzése.
    - Új könyvek hozzáadása.
    - Ügyfélüzenetek megtekintése.

2. **Ügyfél Modul**:
    - Könyvek megtekintése.
    - Könyvek kosárba helyezése.
    - Könyvek keresése.

### Hardver Követelmények

| Követelmény        | Specifikáció              |
|--------------------|---------------------------|
| Operációs Rendszer | Windows 7/8/10, Linux, Mac |
| RAM                | 350MB                      |
| Processzor         | Kétmagos vagy jobb         |

### Szoftver Követelmények

- WAMP Szerver
- MySQL
- PHPMyAdmin
- Böngésző (Firefox, Chrome, IE)

## Rendszer Tervezés

### Általános Rendszerterv

A rendszerterv magában foglalja a **Fizikai Tervezést** és az **Adatbázis Tervezést**. Az elsődlegesen használt eszközök az Adatfolyam Diagramok (DFD) és a Kapcsolati-Entitás (ER) diagramok.

### Adat Szótár

| Tábla Név  | Mezők                         | Leírás                 |
|------------|-------------------------------|------------------------|
| Admin      | a_id, a_unm, a_pwd             | Admin bejelentkezési információkat tárol|
| Könyv      | b_id, b_nm, b_cat, b_desc, stb.| Könyv részletek tárolása |
| Kategória  | cat_id, cat_nm                 | Kategóriák neveinek tárolása |

### Bemenet/Kimenet Tervezés

A bemenet/kimenet rendszer megtervezi a felhasználói felületet a könyvválasztás, regisztráció, bejelentkezés és rendelések számára. Az oldalak tartalmazzák:

- Főoldal
- Bejelentkezés Oldal
- Könyv Részletek
- Kosár Oldal

---

## Tesztelés és Megvalósítás

### Alkalmazott Tesztelési Módszerek

Az alkalmazott tesztelési módszerek:

1. **Fekete Doboz Tesztelés**: Tesztelés specifikációk alapján.
2. **Fehér Doboz Tesztelés**: Tesztelés a program szerkezetének vizsgálatával.
3. **Szürke Doboz Tesztelés**: Tesztelés korlátozott ismeretekkel a rendszer belső felépítéséről.

### Teszt Esetek

1. **Admin Bejelentkezés**:
    - Bemenet: Admin hitelesítő adatok.
    - Várt: Hibaüzenet hibás mezők esetén.

2. **Felhasználói Regisztráció**:
    - Bemenet: Regisztrációs adatok.
    - Várt: Hibaüzenet hiányzó/érvénytelen mezők esetén.

---

## Következtetés

### A Rendszer Korlátai

- Jelenleg nincs súgó funkció.
- Nincs online fizetési lehetőség.
- Többnyelvű támogatás még nincs megvalósítva.
- Nincs biztonsági mentés vagy helyreállítás funkció.

### A Rendszer

 Jövőbeli Fejlődési Irányai

- Súgó és online fizetési modulok bevezetése.
- Többnyelvű támogatás hozzáadása.
- A felhasználói élmény javítása további funkciók bevezetésével.

### Irodalomjegyzék

- Weboldalak: Google, StackOverflow, W3Schools.
- Alkalmazások: YouTube.

---

