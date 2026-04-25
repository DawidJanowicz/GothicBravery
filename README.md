# ⚔ GOTHIC BRAVERY

Randomizer buildu do **Gothic II Noc Kruka** - narzędzie które losuje zestaw atrybutów dla gracza przed rozgrywką, wymuszając ograniczenia i wymagania które utrudniają i urozmaicają przejście gry.

---

## 🎲 Jak używać

1. Otwórz plik `GothicBravery.html` w przeglądarce
2. Kliknij przycisk **✦ Losuj ✦**
3. Karty odkrywają się jedna po drugiej — poznaj swój los

Nie wymaga instalacji, serwera ani połączenia z internetem. Działa lokalnie jako pojedynczy plik HTML.

---

## 📋 Losowane kategorie

| Kategoria | Opis |
|---|---|
| **Gildia** | Gildia do której należy postać |
| **Pomoc Laresa z Gildią** | Czy postać otrzymuje pomoc Laresa(TAK/NIE) |
| **Szpon Beliara** | Czy postać używa Szponu Beliara (TAK/NIE) |
| **Używana Broń** | Typ broni którego gracz musi używać |
| **Zabroniona Broń** | Typ broni którego gracz nie może używać |
| **Zwoje** | Dostępne zwoje magiczne |
| **Wymagana Umiejętność** | Umiejętność którą gracz musi zdobyć jak najszybciej|
| **Zabroniona Umiejętność** | Umiejętność której gracz nie może się nauczyć |

---

## ⚙️ Reguły i logika

### Broń
- **Używana Broń** i **Zabroniona Broń** nigdy nie są tym samym typem

### Umiejętności — zależności
Niektóre umiejętności wymagają wcześniejszego nauczenia się innych. Randomizer uwzględnia te zależności - **Wymagana Umiejętność** jest zawsze osiągalna pomimo blokady:

- `ekstrakt leczniczy` wymaga → `esencja lecznicza`
- `eliksir leczniczy` wymaga → `ekstrakt leczniczy` → `esencja lecznicza`
- `eliksir życia` wymaga → pełny łańcuch eliksiru leczniczego
- `ekstrakt many` wymaga → `esencja many`
- `eliksir many` wymaga → `ekstrakt many` → `esencja many`
- `eliksir ducha` wymaga → pełny łańcuch eliksiru many
- `eliksir siły`, `eliksir zręczności`, `mikstura szybkości` — wymagają `esencji leczniczej` **lub** `esencji many` (wystarczy jedna ścieżka)

### Umiejętności — gildie
Część umiejętności jest dostępna **wyłącznie** dla gildii **Najemnik/Łowca Smoków**:

- `długi magiczny miecz`
- `magiczny miecz dwuręczny`
- `magiczny miecz półtoraręczny`
- `ciężki magiczny miecz dwuręczny`
- `magiczne ostrze bojowe`
- `ciężkie magiczne ostrze bojowe`
- `magiczne ostrze na smoki`
- `duże magiczne ostrze na smoki`

Dla pozostałych gildi powyższe umiejętności są wykluczone zarówno z **Wymaganej** jak i **Zabronionej** umiejętności.

---

## 🗂️ Dostępne dane

**Gildie:** Strażnik/Paladyn · Najemnik/Łowca Smoków · Nowicjusz/Mag Ognia

**Typy broni:** Jednoręczne · Dwuręczne · Kusza · Łuk · Magia Wody · Magia Ognia

**Zwoje:** Ogień · Woda · Przywoływanie · Przemiana · NIC · WSZYSTKO

**Umiejętności:** alchemia (esencje, ekstrakty, eliksiry), zbieractwo (surowce z potworów), umiejętności złodziejskie, kowalstwo

---

## 🛠️ Technologie

- HTML5
- CSS3 (zmienne, animacje, grid)
- Vanilla JavaScript (bez żadnych zależności)

---

## 📁 Struktura projektu

```
gothic-bravery/
└── gothic-bravery.html   # cały projekt w jednym pliku
```
