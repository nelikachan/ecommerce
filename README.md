# Analiza zachowań użytkowników w e-commerce

Celem projektu jest analiza zachowań użytkowników na platformie e-commerce oraz identyfikacja kluczowych wzorców w ścieżce zakupowej na podstawie danych Kaggle https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store (dane wykorzystane w celach edukacyjnych)

Analiza koncentruje się na konwersji użytkowników w lejku sprzedażowym (view ->cart -> purchase), retencji użytkowników w czasie oraz identyfikacji miejsc utraty użytkowników (drop-off) i możliwości optymalizacji.

---

## Wykorzystane przeze mnie marzędzia to:

* SQL (Google BigQuery),
* Python (pandas, matplotlib, seaborn),
* Power BI.

---


## Wstępne przygotowanie danych

Dane zostały oczyszczone i przetworzone przy użyciu SQL w BigQuery: usunięcie nieprawidłowych rekordów (price ≤ 0), obsługa brakujących wartości, poprawne typowanie danych i konwersja czasu.

---

## Analiza lejka konwersji

Lejek konwersji przedstawia przejście użytkowników przez kluczowe etapy view -> cart ->purchase

### Wyniki są następujące:

* Użytkownicy, którzy obejrzeli produkty: 3021273, którzy dodali do koszyka: 336481, którzy dokonali zakupu: 167986.

### Współczynniki konwersji są następujące:

* View -> cart: 11.1%, cart -> purchase: 49.9%

### Można więc dojść do kilku wniosków:

* Największy spadek użytkowników występuje na etapie view -> cart,
* Tylko niewielka część użytkowników przechodzi do dodania produktu do koszyka,
* Użytkownicy, którzy dodają produkty do koszyka często finalizują zakup.

---

## Analiza retencji

Retencja została przeanalizowana przy użyciu analizy kohortowej na podstawie daty pierwszej interakcji użytkownika.

### Wyniki:

* Retencja gwałtownie spada po pierwszym dniu (do ok 10–17%),
* Po 2–3 dniach stabilizuje się na poziomie ok 6–8%,
* Istnieje niewielka grupa lojalnych użytkowników powracajacych do platformy,
* Brak istotnych różnic między kohortami.

---

## Wizualizacja danych

### Python

* wizualizacja lejka konwersji,
* heatmapa retencji,
* wykres średniej retencji.

### Power BI

Dashboard zawiera:

* wskaźniki KPI (konwersje),
* wykres lejka,
* wykres retencji.


---

## Wnioski
Podsumowując:

* Główne ograniczenie konwersji występuje na etapie view -> cart
* Poprawa prezentacji produktu, ceny lub UX może zwiększyć konwersję
* Niska retencja wskazuje na potrzebę poprawy zaangażowania użytkowników
* Istnieje grupa lojalnych użytkowników jednak jest ona niewielka

