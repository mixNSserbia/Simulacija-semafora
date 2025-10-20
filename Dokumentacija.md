# 📘 Dokumentacija projekta: Simulacija semafora na četvorostranoj raskrsnici

## 1. 🧩 Opis projekta

Ovaj projekat predstavlja vizuelnu simulaciju rada semafora za vozila i pešake na četvorostranoj raskrsnici. Simulacija je razvijena u programskom jeziku C++ uz korišćenje SFML biblioteke. Sistem prikazuje rad semafora sa tajmerima, pešačkim senzorima i dinamičkim prelaskom faza u realnom vremenu.

## 2. 🎯 Ciljevi

- Prikazati rad semafora za 4 strane raskrsnice (Sever, Jug, Istok, Zapad)
- Upravljati vozilskim i pešačkim semaforima
- Aktivirati pešački prelaz putem senzora (tastera)
- Vizuelno prikazati stanje svetala i tajmera koristeći SFML

## 3. 🧠 Arhitektura sistema

### 3.1 Komponente

| Komponenta         | Opis |
|--------------------|------|
| `TrafficSignal`    | Struktura koja sadrži stanje svetala za vozila i pešake, tajmer i senzor |
| `VisualSignal`     | SFML elementi za prikaz semafora i tajmera |
| `setupVisual()`    | Funkcija za inicijalizaciju grafičkih elemenata |
| `main()`           | Glavna petlja simulacije i upravljanje ciklusima |

### 3.2 Tok simulacije

1. Svaka strana raskrsnice ima svoj semafor
2. Vozila dobijaju zeleno svetlo po redosledu
3. Pešaci mogu aktivirati senzor (taster 0–3 ili Space)
4. Kada vozila dobiju crveno, pešaci dobijaju zeleno ako je senzor aktiviran
5. Tajmer prikazuje preostalo vreme faze

## 4. 💻 Tehnički detalji

- **Jezik:** C++
- **Biblioteka:** SFML (Simple and Fast Multimedia Library)
- **Font:** `arial.ttf` za prikaz tajmera
- **Platforma:** Desktop aplikacija (Windows/Linux)

## 5. 🎮 Kontrole

- `0`, `1`, `2`, `3` → Aktiviraj pešački senzor za Sever, Jug, Istok, Zapad
- `Space` → Aktiviraj pešački senzor za trenutno aktivnu stranu
- `Esc` ili zatvaranje prozora → Izlaz iz simulacije

## 6. 🧪 Testiranje

Testiranje se vrši pokretanjem aplikacije i posmatranjem:
- Da li se pešački semafor aktivira samo kada je senzor uključen
- Da li se tajmeri pravilno odbrojavaju
- Da li se ciklusi pravilno smenjuju
- Da li se vizuelni prikaz ažurira u realnom vremenu

## 7. 🔄 Mogućnosti proširenja

- Dodavanje animacije vozila i pešaka
- Integracija sa fizičkim komponentama (Arduino + LED + senzori)
- Logovanje događaja u fajl
- Vizuelizacija toka semafora u web aplikaciji
- Dodavanje zvučnih signala za pešake

## 8. 📎 Zaključak

Projekat je modularan, edukativan i lako proširiv. Pruža osnovu za razumevanje rada semafora i upravljanja saobraćajem kroz programski kod. Namenjen je studentima, hobistima i svima koji žele da uče kroz vizuelnu simulaciju.
