# Twój Asystent AI - Instrukcja Konfiguracji

## Po co to robimy

Każdy product builder powinien mieć swojego asystenta AI. Myśl o nim jak o szefie sztabu, cyfrowym partnerze, który jest tu żeby:

- Kwestionować twoje założenia i szukać luk w myśleniu
- Pomagać z researchem, analizą danych i dokumentacją
- Wspierać w tworzeniu konceptów i prototypów
- Pamiętać kontekst twojego produktu i firmy

W pierwszym tygodniu zbudujesz projekt LLM z pełnym kontekstem FashionHero. Kiedy go skonfigurujesz, będziesz mieć lepsze środowisko do pracy produktowej niż większość ludzi w branży.

Dzielimy się z tobą sprawdzonymi w praktyce sposobami na konfigurację: właściwy system prompt (konstytucja twojego projektu, którą AI czyta ZANIM odpowie na jakiekolwiek pytanie) oraz struktura i typ plików które dają projektowi pełny kontekst twojego produktu.

Robimy to na bazie FashionHero. W ramach kursu dostajesz też generyczny szablon do konfiguracji asystenta dla twojej własnej firmy - to osobny projekt, żeby konteksty się nie mieszały.

> **W drugim tygodniu** poznasz koncept "drugiego mózgu" - AI który nie tylko rozmawia z tobą, ale też zarządza plikami, buduje i wykonuje skrypty, i utrzymuje rosnącą bazę wiedzy o twoim produkcie. Do tego będziesz potrzebować Claude Code (desktop) lub Cursor. Ale o tym za tydzień.

---

## Wybierz swoje narzędzie

Instrukcje poniżej są dla trzech platform. Zasada jest ta sama - różnią się szczegóły. Wybierz swoją:

- [Claude](#claude) (rekomendowany)
- [ChatGPT](#chatgpt)
- [Gemini](#gemini)

---

## Claude

### 1. Otwórz Claude

Wejdź na [claude.ai](https://claude.ai) lub otwórz aplikację desktopową Claude. Zaloguj się na swoje konto.

### 2. Stwórz nowy projekt

Na lewym panelu znajdź opcję **Projects** i kliknij **New Project**.

- **Nazwa:** FashionHero
- **Opis:** Asystent produktowy do pracy nad FashionHero

Nazwa i opis nie wpływają na odpowiedzi AI - są tylko dla ciebie.

### 3. Wygeneruj system prompt

Otwórz chat w swoim nowym (pustym) projekcie i wrzuć do niego plik `00b-system-prompt-generator-fashionhero.md`.

AI zada ci 2 pytania:
- Jak chcesz żeby z tobą współpracował (styl komunikacji)
- W jakich obszarach potrzebujesz wsparcia (twoje ślepe punkty)

Odpowiedz szczerze. Na koniec AI wygeneruje system prompt dopasowany do ciebie. **Skopiuj go.**

### 4. Wklej system prompt w instrukcjach projektu

- Kliknij ikonę **ustawień projektu** (w prawym górnym rogu, obok nazwy projektu)
- Znajdź sekcję **Instructions**
- Wklej wygenerowany system prompt

To jest "konstytucja" twojego projektu. AI przeczyta te instrukcje PRZED każdą odpowiedzią.

### 5. Dodaj pliki kontekstowe

W ustawieniach projektu znajdziesz sekcję **Project Knowledge**.

Weź pliki od `01` do `09` i wrzuć je tam:

| Plik | Co zawiera |
|---|---|
| `01-company-overview.md` | Kim jest FashionHero, skala, zespół |
| `02-product-strategy.md` | Strategia, priorytety, jak podejmujemy decyzje |
| `03-target-segments.md` | Segmenty kupujących |
| `04-user-research-buyers.md` | Badania kupujących, NPS, tickety supportu |
| `05-competitive-landscape.md` | Konkurencja, rynek, trendy |
| `06-experiment-log.md` | Co próbowaliśmy i jak poszło |
| `07-decision-log.md` | Kluczowe decyzje i dlaczego |
| `08-seasonal-calendar.md` | Kalendarz sezonowy fashion |
| `09-revenue-metrics.md` | Przychody, koszty, metryki |

### 6. Gotowe

Otwórz nowy chat w projekcie i zacznij rozmowę. Na start możesz rozejrzeć się po kontekście ("Opowiedz mi o FashionHero") albo od razu przejść do Quest 1.1.

---

## ChatGPT

### 1. Otwórz ChatGPT

Wejdź na [chatgpt.com](https://chatgpt.com) lub otwórz aplikację desktopową. Zaloguj się.

### 2. Stwórz nowy projekt

Na lewym panelu znajdź opcję **Projects** i stwórz nowy projekt.

- **Nazwa:** FashionHero

### 3. Wygeneruj system prompt

Otwórz chat w swoim nowym projekcie i wrzuć plik `00b-system-prompt-generator-fashionhero.md`.

AI zada ci 2 pytania (styl komunikacji + obszary wsparcia). Odpowiedz. Na koniec dostaniesz wygenerowany system prompt. **Skopiuj go.**

### 4. Wklej system prompt

- W prawym górnym rogu strony projektu kliknij **trzy kropki** (...)
- Wybierz **Project settings** (ustawienia projektu)
- Wklej system prompt w sekcji instrukcji

### 5. Dodaj pliki kontekstowe

Pod oknem chatu zobaczysz dwie zakładki: **Chats** (historia rozmów) i **Sources** (źródła).

Kliknij **Sources** i dodaj pliki od `01` do `09`. To są twoje źródła wiedzy - ChatGPT będzie się do nich odwoływał w każdej rozmowie w tym projekcie.

### 6. Gotowe

Wróć do zakładki Chats, otwórz nowy chat i zacznij rozmowę.

---

## Gemini

### 1. Wygeneruj system prompt

W Gemini kolejność jest inna niż w Claude i ChatGPT. **Zacznij od zwykłego chatu** (nie od Gema).

Otwórz [gemini.google.com](https://gemini.google.com), stwórz nowy chat i wklej zawartość pliku `00b-system-prompt-generator-fashionhero.md`.

AI zada ci 2 pytania. Odpowiedz. Dostaniesz system prompt. **Skopiuj go.**

### 2. Stwórz Gema

Na lewym panelu znajdź **Gems** (Gemy) i kliknij **Create a new Gem** (Stwórz nowego Gema).

- **Nazwa:** FashionHero
- **Opis:** Asystent produktowy do pracy nad FashionHero
- **Instrukcje:** Wklej wygenerowany system prompt w pole **Instrukcje**

### 3. Dodaj pliki kontekstowe

Poniżej instrukcji znajdziesz sekcję **Knowledge** (wiedza). Dodaj tam pliki od `01` do `09`.

### 4. Zapisz i zacznij rozmowę

Kliknij **Save** (Zapisz). Gem jest gotowy - otwórz go i zacznij rozmowę.

### Ograniczenie Gemini: max 10 plików

Gemini pozwala dodać maksymalnie 10 plików do Gema. Przy 9 plikach kontekstowych mieścisz się, ale nie masz zapasu. Jeśli Gemini jest twoim głównym narzędziem i chcesz dodawać więcej plików w przyszłości, masz dwa wyjścia:

1. **Łącz mniejsze pliki w jeden** - np. experiment log + decision log w jeden plik "historia decyzji i eksperymentów"
2. **Użyj NotebookLM jako bazy wiedzy** - stwórz notebook w [NotebookLM](https://notebooklm.google.com), wrzuć tam wszystkie pliki kontekstowe (możesz je edytować, dodawać nowe, dorzucać źródła zewnętrzne), a potem podłącz ten notebook jako źródło wiedzy do swojego Gema. Nie będziemy pokazywać tego flow na kursie, ale jeśli Gemini to twoje główne narzędzie - to jest obejście limitu 10 plików.

---

## Utrzymywanie wiedzy projektu

Pliki 01-09 to typy dokumentów które warto utrzymywać na bieżąco w każdym projekcie produktowym. Na przykład:

- Podjąłeś ważną decyzję? → Dopisz ją do decision log
- Skończyłeś eksperyment? → Dopisz wyniki do experiment log
- Zmieniła się strategia? → Zaktualizuj product strategy

Im bardziej aktualne pliki, tym lepsze odpowiedzi od AI. Nieaktualne pliki = nieaktualne rady.

### Edycja plików

Ani Claude, ani ChatGPT, ani Gemini nie pozwalają edytować plików wiedzy z poziomu chatu. Jeśli chcesz zmienić lub uzupełnić plik:

1. Pobierz go lub skopiuj zawartość do notatnika
2. Wprowadź zmiany
3. Usuń stary plik z projektu
4. Wrzuć zaktualizowaną wersję

To ograniczenie zniknie w drugim tygodniu kiedy przejdziemy na Claude Code / Cursor - tam AI bezpośrednio edytuje pliki na twoim dysku.

### Pamięć (opcjonalnie)

Claude i ChatGPT mają funkcję pamięci która działa MIĘDZY projektami - AI zapamiętuje informacje z rozmów i odwołuje się do nich w przyszłości.

- **Claude:** Settings → Features → Memory
- **ChatGPT:** Settings → Personalization → Memory
- **Gemini:** Na chwilę obecną nie ma funkcji pamięci dostępnej w Polsce / UE

**Uwaga:** Pamięć to miecz obosieczny. Jeśli w rozmowie powiesz hipotezę jako fakt ("nasi duzi sprzedawcy są nierentowni") - AI może to zapamiętać jako fakt i powtarzać w przyszłych rozmowach. Jeśli włączasz pamięć:

- Dbaj o higienę rozmów - usuwaj chaty które zawierają błędne informacje
- Zaznaczaj kiedy mówisz o hipotezach vs faktach
- Regularnie sprawdzaj co AI zapamiętał (w ustawieniach)

Dla kursu wystarczą pliki. Pamięć jest opcjonalna.

---

## A co z moją własną firmą?

W paczce masz też plik `00-system-prompt-generator.md` - generyczny generator. Działa tak samo ale zamiast kontekstu FashionHero, zapyta cię o twoją firmę, rolę i produkty.

**Stwórz osobny projekt** dla swojej firmy. Nie mieszaj kontekstów - FashionHero to case study, twoja firma to twoja firma. Osobne projekty, osobne pliki, osobne instrukcje.

Struktura plików 01-09 jest wzorem. Przygotuj analogiczne dokumenty dla swojej firmy i wrzuć je do swojego projektu. Nie musisz mieć wszystkich od razu - zacznij od company overview i product strategy, resztę dodawaj w miarę jak będziesz je mieć.
