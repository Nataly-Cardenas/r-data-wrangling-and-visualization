# Data Wrangling and Visualization in R

A collection of data analysis case studies in R, published as an interactive
book with bookdown. Each chapter takes a real dataset, cleans and reshapes it
with the tidyverse, and communicates the results through summary tables and
custom-styled visualizations.

📖 **Read the book online:** https://nataly-cardenas.github.io/r-data-wrangling-and-visualization/

*The book is written in Spanish; this README is in English for a wider audience.*

## What's inside

| Chapter | Topic | What it covers |
|---|---|---|
| 1 | **Wildfires in Idaho** | Filtering 439,362 wildfire records down to Idaho, selecting and renaming columns, grouping by cause and year, computing mean, median and IQR of acres burned, and plotting the trend over time with `ggplot2` |
| 2 | **Rio 2016 Olympic medalists** | Identifying the top 5 sports by medals, comparing age distributions with boxplots, finding the leading national team per sport, and analyzing weight differences by sex |
| 3 | **Reshaping US state population data** | Converting a wide table (2010–2018) to long format with `gather()` to create `Year` and `population` columns, then combining and splitting columns with `unite()` and `separate()` |
| 4 | **Distribution of acres burned** | Building a histogram (bin width = 500 acres) of large wildfires (over 1,000 acres, 2010–2016) and interpreting its strong right skew |

## Selected findings

- **Idaho wildfires:** the mean acres burned per fire varies widely by cause and year, while medians stay low. Most fires are small, and a few very large fires pull the means up.
- **Rio 2016:** Athletics (192 medals) and Swimming (191) led the medal count, followed by Rowing, Football and Hockey. The United States led both Athletics (46) and Swimming (71).
- **Athlete profiles:** medalists in Swimming were the youngest of the top 5 sports (mean age 23.2) and in Rowing the oldest (28.1). Male medalists were heavier than female medalists in every one of the five sports.
- **Large wildfires:** the distribution of acres burned is highly right-skewed, with many small fires and a few extreme ones.

## Skills demonstrated

- Data manipulation with `dplyr`: `filter`, `select`, `rename`, `group_by`, `summarise`, `slice_max`, `arrange`
- Reshaping with `tidyr`: `gather`, `unite`, `separate`
- Descriptive statistics: mean, median, standard deviation, quartiles and IQR
- Data visualization with `ggplot2`: line charts, boxplots, histograms and a custom color palette
- Publication-ready tables with `gt`
- Reproducible reporting with R Markdown and bookdown

## Tools

- R and RStudio
- `tidyverse` (`dplyr`, `tidyr`, `ggplot2`, `readr`)
- `gt`, `scales`, `knitr`
- `bookdown` (GitBook output)

## Data sources

| Dataset | File | Used in |
|---|---|---|
| US wildfire records (439,362 rows, 14 variables) | `StudyArea.csv` | Chapters 1 and 4 |
| Olympic athlete events | `athlete_events.csv`, loaded from [cdeoroaguado/Datos](https://github.com/cdeoroaguado/Datos) | Chapter 2 |
| US state population, 2010–2018 (51 rows) | `us_state_population.tsv` | Chapter 3 |

## Run it locally

1. Clone the repository:
```bash
   git clone https://github.com/nataly-cardenas/r-data-wrangling-and-visualization.git
```
2. Open the project in RStudio.
3. Install the required packages:
```r
   install.packages(c("tidyverse", "gt", "scales", "knitr", "bookdown"))
```
4. Place `StudyArea.csv` and `us_state_population.tsv` in a local folder and
   update the file paths in the `.Rmd` files (chapters 1, 3 and 4) to point
   to them.
5. Build the book:
```r
   bookdown::render_book("index.Rmd")
```

## Authors

- Nátaly Cárdenas Izáquita
- Laura Rivera
