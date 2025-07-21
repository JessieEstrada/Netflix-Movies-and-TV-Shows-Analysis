# 📊 Netflix Data Analysis Project

This project explores the global Netflix catalog using a dataset of movies and TV shows. It demonstrates the full data analysis pipeline—from cleaning and structuring raw data in MySQL, to transforming it in Excel, and visualizing key insights in Power BI.

---

## 📁 Dataset Overview

- **Source**: [Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Rows**: ~7,000 titles  
- **Fields**: `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

---

## ⚙️ Tools & Technologies

- **MySQL Workbench** – SQL queries, data cleaning, schema design  
- **Microsoft Excel** – Splitting normalized tables into clean `.csv` files  
- **Power BI** – Interactive dashboards and visual storytelling  
- **GitHub** – Version control, project documentation  

---

## 🧹 Step 1: Data Preparation (MySQL)

The raw dataset was first imported into **MySQL Workbench**. I separated multivalued fields (`cast`, `director`, `country`, `listed_in`, `description`) into individual tables while preserving referential integrity via `show_id`.

### Tables Created:

- `netflix_titles`
- `netflix_cast`
- `netflix_directors`
- `netflix_country`
- `netflix_listed_in`
- `netflix_descriptions`

This allowed for more efficient querying and filtering in downstream analysis.

---

## 📄 Step 2: Data Normalization (Excel)

Each cleaned table was exported to `.csv` and reviewed in **Excel**:
- Verified all `show_id` references were consistent
- Removed trailing spaces and null rows
- Split into 6 clean, normalized CSVs ready for Power BI import

### Structured CSVs:
- `netflix_titles.csv`
- `cast.csv`
- `directors.csv`
- `descriptions.csv`
- `listed_in.csv`
- `countries.csv`

---

## 📊 Dashboard 1 – High-Level Insights

This Power BI dashboard provides a macro-level view of Netflix’s content library.

### Visuals:
- 🔝 **Top 10 Genres**  
  Bar chart showing the most common genres by content count.

- 📈 **Productions Over Time**  
  Line chart showing content added from 2014 to 2020, split into Movies and TV Shows.

- 📊 **Ratings Breakdown**  
  Stacked bar chart showing the number of shows/movies per rating (e.g., TV-MA, R), grouped by type.

- 🗺️ **Global Production Map**  
  World map highlighting where Netflix content was produced. Circle size = content count per country.

---

## 🎬 Dashboard 2 – Title Detail Viewer

An interactive Netflix-style detail page, dynamically updating based on the selected title.

### Features:
- 🔽 **Dropdown Selector**  
  Choose any title from the dataset and update the visuals in real time.

- 🆔 **Title Metadata**  
  Displays title, release year, rating, and synopsis.

- 📖 **Genre Tags**  
  Lists categorized genres for the selected title.

- 🎬 **Production Credits**  
  Lists director(s) and cast members.

- 🌍 **Geographic Context**  
  Map visualization showing country of origin for the title.

---

## 🚀 Project Highlights

- ✅ End-to-end ETL: SQL → Excel → Power BI  
- ✅ Fully normalized data model using `show_id` as a consistent key  
- ✅ Clean, dynamic, and interactive visual dashboards  
- ✅ Real-world structure and logic inspired by professional BI workflows
