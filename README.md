
# 🚂 Harmonogram Pracy v1.34

Zaawansowany system do wizualizacji, edycji i precyzyjnego rozliczania czasu pracy, stworzony z myślą o specyfice pracy na kolei. Aplikacja przekształca surowe dane z kalendarza (pliki ICS) w czytelny, profesjonalny i gotowy do wydruku dokument (sztywne 2 strony A4).

## 🌟 Główne Funkcje (index.html)

* **Gwarantowany Layout A4:** Specjalna struktura CSS wymusza sztywny podział na dwie strony – pierwsza zawiera kalendarz miesięczny i sumy, druga szczegółowy rejestr. Zapobiega to rozjeżdżaniu się wydruku na 3 i więcej stron.
* **Inteligentne Zarządzanie Bazą:**
    * **Auto-pobieranie:** Aplikacja automatycznie próbuje wczytać plik `szczegoly_sluzb.json` z serwera.
    * **LocalStorage:** Zapamiętuje ostatnio wgrany plik bazy w pamięci przeglądarki, dzięki czemu nie trzeba go wybierać przy każdym uruchomieniu.
* **Precyzyjne Rozliczenia:**
    * Wyliczanie czasu pracy, godzin nocnych oraz pracy w niedziele i święta co do minuty.
    * **Alert Odpoczynku:** Automatyczne ostrzeżenia (⚠️) w przypadku naruszenia 12-godzinnej przerwy między służbami.
* **Dostępność i Standardy:** Kod zgodny z **EAA** (European Accessibility Act) oraz **WCAG**, w pełni responsywny i przygotowany na urządzenia mobilne.

## 🛠️ Kreator Bazy (edytor.html)

Kompletne narzędzie do zarządzania szczegółami pociągów i regułami kursowania:
* **Inteligentne Reguły:** Ustawianie stałych dni kursowania (np. Pn-Pt) jednym kliknięciem.
* **Multi-Date Picker:** Interaktywny kalendarz do wyboru wielu dat wyłączeń (kiedy służba nie jedzie) oraz dodatkowych dni kursowania.
* **Funkcja Duplikowania:** Błyskawiczne kopiowanie istniejących zmian w celu tworzenia nowych wariantów.
* **Widok Excela:** Czytelny podgląd całej bazy administratora w formie tabeli.

## 📋 Instrukcja Obsługi

### Dla Użytkownika:
1. Otwórz `index.html`.
2. Wgraj plik harmonogramu **.ics** (pobrany z kalendarza służbowego).
3. Aplikacja automatycznie dopasuje pociągi, jeśli baza JSON znajduje się w folderze lub została wcześniej wgrana.
4. Wpisz swoje dane w ramce "Pracownik" (jeśli pole pozostanie puste, na wydruku pojawi się pusta ramka na wpis ręczny).
5. Kliknij **Drukuj Harmonogram**.

### Dla Administratora:
1. Otwórz `edytor.html`.
2. Zaimportuj istniejący plik JSON lub stwórz nową bazę.
3. Skonfiguruj kody służb, przypisz pociągi i określ ich typy (PNP, W, L).
4. Wyeksportuj plik i umieść go na serwerze/w folderze jako `szczegoly_sluzb.json`.

## 📂 Struktura Projektu
* `index.html` – Główny moduł wyświetlający i drukujący.
* `edytor.html` – Moduł administracyjny do zarządzania bazą.
* `szczegoly_sluzb.json` – Plik bazy danych (pociągi, relacje, wyjątki).

## ⚠️ Nota Prawna (Disclaimer)
Prezentowane w sekcji "Szczegółowy Rejestr Służb" informacje dotyczące numerów pociągów, miejsc rozpoczęcia oraz godzin poszczególnych czynności mają charakter wyłącznie **poglądowy**. Podstawowym, nadrzędnym i jedynym obowiązującym dokumentem określającym szczegółowy plan pracy oraz wytyczne operacyjne jest aktualny plan pracy zamieszczony w aplikacji **Teczka Konduktora** oraz systemie **IVU**.

## 🏗️ Autorzy i Wersja
* **Piotr M 🚂** – Pomysłodawca, autor zależności merytorycznych i logiki kolejowej.
* **Gemini** – Implementacja techniczna, UI/UX i optymalizacja kodu.

**Wersja:** v1.34  
**Data wydania:** 31.03.2026
**Status:** Stabilna (2 strony A4)

***