## 📊 Disney Movies Revenue Dashboard (Power BI)

### 🔍 Project Overview
Interactive dashboard created in **Power BI** based on historical revenue data of Disney movies released between **1937 and 2016**. The report was built as part of an analytical challenge and adheres to a strict set of **functional and non-functional requirements**.

---

### 📁 Dataset
- **Source:** Disney Movies dataset  
- **Fields:**  
  - `Movie Title`  
  - `Date Released`  
  - `Genre`  
  - `MPA Rating`  
  - `Total Gross`  
  - `Inflation Adjusted Gross`

---

### ⚙️ Tools & Technologies
- **Power BI** (DAX, custom visuals, bookmarks, slicers)
- **Power Query** for data transformation and API integration
- **OMDb API** integration to fetch movie posters dynamically using movie title and release year

```powerquery
= (Tytul as text, Rok as nullable date) =>
let
    ApiKey = "APIKEY",
    YearText = if Rok <> null then Text.From(Date.Year(Rok)) else null,
    BaseUrlWithYear = "http://www.omdbapi.com/?apikey=" & ApiKey & "&t=" & Uri.EscapeDataString(Tytul) & "&y=" & Uri.EscapeDataString(YearText),
    BaseUrlWithoutYear = "http://www.omdbapi.com/?apikey=" & ApiKey & "&t=" & Uri.EscapeDataString(Tytul),

    ResponseWithYear = Json.Document(Web.Contents(BaseUrlWithYear)),
    PosterURLWithYear = try ResponseWithYear[Poster] otherwise null,

    ResponseWithoutYear = if PosterURLWithYear = null then Json.Document(Web.Contents(BaseUrlWithoutYear)) else ResponseWithYear,
    PosterURL = try ResponseWithoutYear[Poster] otherwise null
in
    PosterURL
```

---

### ✅ Functionalities
- Total number of Disney movies
- Total gross revenue (with and without inflation adjustment)
- Genre-based revenue share (excluding "Unknown")
- Line chart showing revenue trends over the years
- Top 10 movies by inflation-adjusted revenue difference
- Filters by:
  - Genre *(multi-select, excluding "Unknown")*
  - Age rating *(multi-select, excluding "Unknown")*
  - Release year *(multi-select range)*  
- Dynamic movie poster integration from OMDb API
- Movie identification through title (or title + release year if not unique)

---

### 🧩 Missing Data Handling
- If a selected year has no movie data:
  - Numeric visualizations (e.g. cards, charts) return **0** instead of remaining blank
  - Movie-related visuals display `"No Data"` as a placeholder title
  - Layout remains responsive and informative even with no relevant data

---

### 🌟 Key Focus Areas
- Data visualization clarity and responsiveness
- Strong UX & UI principles in a one-page layout
- Business storytelling with emphasis on revenue growth and genre dynamics

---

### 🖼️ Dashboard Preview
<p align="center">
  <img src="image-1.png" alt="Disney Movies Power BI Dashboard Screenshot" width="700"/>
</p>

