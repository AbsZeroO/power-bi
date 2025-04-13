# ENG

## 📊 WTA Tour Tennis Tournament Dashboard 2025

### 🔍 Project
An interactive **Power BI** report based on the 2025 **WTA Tour** tennis tournament data. The dashboard is designed to present comprehensive insights about upcoming tournaments, focusing on their category, location, date range, and court surface.

---

### 📁 Dataset
- **Source:** WTA Tour 2025 tournament dataset  
- **Columns:**  
  - `Tournament`: Tournament name  
  - `Category`: Tournament category  
  - `City`: City or cities hosting the tournament  
  - `Country`: Country hosting the tournament  
  - `Start Date`: Tournament start date  
  - `End Date`: Tournament end date  
  - `Surface`: Court surface type

---

### ⚙️ Tools & Technologies
- **Power BI** (DAX, custom visuals, bookmarks, slicers)  
- **Custom Gantt Visual** for timeline display

---

### ✅ Features
- Count of completed tournaments vs. total  
- Chronological listing of tournaments  
- Unique tournament name count  
- Monthly time-axis visualization  
- Full-width schedule layout  
- Real-time tournament completion percentage  
- Legend for tournament categories  
- Hover tooltips showing surface type  
- Filtering by:  
  - Category *(multi-select)*  
  - Country *(multi-select)*  
  - Surface *(multi-select)*  
  - Date range *(includes tournaments partially within selected dates)*
- Additional features:  
  - Interactive world map showing tournament locations  
  - Filter for tournament completion status

---

### 🧹 Missing Data Handling
- Missing entries default to **"Not Specified"** (notably for Billie Jean King Cup qualifiers)  
  - Numeric visuals default to **0** instead of blanks or negatives  
  - Tournament visuals display **"Nothing Scheduled At This Date"** if applicable  
  - Layout remains fully responsive even with no matching data

---

### 🌟 Key Highlights
- Clear, responsive, one-page design  
- Clean data storytelling focusing on tournament dynamics  
- UX/UI tested for edge cases: any tournament with dates overlapping the selected range appears correctly (e.g., no tournaments shown for June 29, 2025 if none are scheduled)



# PLN

## 📊 ## 📊 WTA Tour Tennis Tournament Dashboard 2025

### 🔍 Projekt
Raport stworzony w **Power BI** na podstawie danych dotyczących turniejów tenisowych WTA Tour, które odbędą się w 2025 roku. Celem raportu jest przedstawienie szczegółowych informacji o nadchodzących turniejach, z uwzględnieniem ich kategorii, lokalizacji, dat oraz nawierzchni.

---

### 📁 Zbiór Danych
- **Źródło:** Zbiór danych turniejów tenisowych WTA Tour 2025  
- **Kolumny:**  
  - `Tournament`: nazwa turnieju  
  - `Category`: kategoria turnieju  
  - `City`: miasto lub miasta, w których odbywa się turniej  
  - `Country`: kraj, w którym odbywa się turniej  
  - `Start Date`: data rozpoczęcia turnieju  
  - `End Date`: data zakończenia turnieju  
  - `Surface`: nawierzchnia, na której rozgrywany jest turniej

---

### ⚙️ Narzędzia i Technologie
- **Power BI** (DAX, niestandardowe wizualizacje, zakładki, filtry)
- **Wizualizacja Gantt** niestandardowa 

---

### ✅ Funkcjonalności
- Liczba zakończonych turniejów w stosunku do wszystkich
- Chronologiczna lista turniejów
- Liczba wierszy odpowiadająca liczbie unikalnych nazw turniejów
- Oś czasu w skali miesięcznej
- Terminarz wyświetlany w pełni na szerokość ekranu
- Aktualny procent ukończenia danego turnieju
- Legenda rozróżniająca turnieje według kategorii
- Informacje o nawierzchni turnieju po najechaniu na niego kursorem
- Filtrowanie danych względem:
  - Kategorii *(wielokrotny wybór)*
  - Kraju *(wielokrotny wybór)*
  - Nawierzchni *(wielokrotny wybór)*
  - Zakresu dat *(jednoczesne uwzględnienie daty rozpoczęcia i zakończenia)*
- Dodatkowe
  - Mapa świata z dokładną lokalizacją turniejów
  - Filtrowanie po Completed
---

### 🧩 Obsługa brakujących danych
- Dane zostają zamienione na `"Not Specified"` (brakujące dane głównie w turnieju billie jean king cup w kwalfiakcjach)
  - Wizualizacje numeryczne (np. karty, wykresy) wyświetlają **0** zamiast pozostawać puste lub pokazywać wartości ujemne
  - Wizualizacje turniejów pokazują `"Nothin Sheduled At This Date"` jako tytuł zastępczy
  - Układ jest responsywny, nawet jeśli brak danych w wybranym zakresie

---

### 🌟 Kluczowe obszary
- Klarowność wizualizacji i responsywność
- Zasady UX i UI w układzie na jednej stronie
- Opowiadanie historii z uwzględnieniem kategorii, lokalizacji i dynamiki turniejów
- Warunki brzegowe przetestowane, gdzie filtr powinien uwzględniać jednocześnie datę rozpoczęcia i datę zakończenia turnieju, tzn. powinny wyświetlić się wszystkie turnieje, których chociaż jeden dzień mieści się w podanym zakresie dat oraz dla daty 29.06.2025 nie ma nic zaplanowanego
---

### 🖼️ Podgląd dashboardu
<p align="center">
  <img src="MainPage.png" alt="WTA Tour Tennis Tournament Power BI Dashboard Screenshot" width="700"/>
</p>

<p align="center">
  <img src="NothingScheduled.png" alt="WTA Tour Tennis Tournament Power BI Dashboard Screenshot" width="700"/>
</p>

<p align="center">
  <img src="MapPage.png" alt="WTA Tour Tennis Tournament Power BI Dashboard Screenshot" width="700"/>
</p>
