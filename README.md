# Project of Data Visualization (COM-480)

| Student's name | SCIPER |
| -------------- | ------ |
| Zhiyao Yan | 399669 |
| Ren Yi |395712 |
| Botu Lyu | 396507 |

[Milestone 1](#milestone-1) • [Milestone 2](#Milestone-2) • [Milestone 3](#Milestone-3)

# Milestone 1


### Dataset

Our dataset consists of four key components:

1. [**GDP**](https://opendata.swiss/en/dataset/bruttoinlandsprodukt-bip-nach-grossregion-und-kanton5): Records the GDP variations of each canton from 2008 to 2022, providing insights into economic trends.
2. [**Population**](https://www.bfs.admin.ch/news/en/2024-0234): Includes total population, age structure, and gender distribution of each canton from 2019 to 2023, which are crucial for understanding social development and quality of life.
3. [**Employment**](https://www.bfs.admin.ch/bfs/en/home/statistics/work-income/employment-working-hours/economically-active-population/economically-active-persons-canton.html): Documents the employment status in each canton for 2023, including employed persons, unemployed persons, individuals looking after home or family, and retired persons, reflecting the labor market conditions.
4. [**Portraits-of-the-cantons**](https://www.bfs.admin.ch/bfs/en/home/statistics/regional-statistics/regional-portraits-key-figures/cantons.html): Covers income, economy, agriculture, and tourism statistics from 2019 to 2021, offering a more comprehensive socio-economic background.

#### Data Quality and Preprocessing

- This dataset comes from an official source and includes all Swiss cantons, so we can trust its accuracy.
- Since the datasets cover different periods, we need to align the timelines to make meaningful comparisons.
- We'll convert Excel files into a more manageable format and extract key details for visualization.
- To avoid confusion from different languages, we will map canton names to their standard abbreviations (e.g., Zürich → ZH, Genève → GE).

### Problematic

#### Motivation

Many reports suggest that Switzerland is one of the happiest countries in the world. As international students, we are fascinated by this beautiful country and want to understand what makes it so unique. During our time in Switzerland, we have admired the tranquility of Lake Geneva, experienced the vibrancy of Zurich, and embraced the Italian influence in Ticino. Over time, we realized that the differences between cantons go beyond just the official languages. This led us to a question: How much does happiness vary among the residents of different cantons?

Thus, we created the project **"Happiness Index Across Swiss Cantons"** to explore which cantons may have higher levels of happiness and let data guide our curiosity in uncovering meaningful insights.

#### Visualization Goals

Happiness is complex and cannot be defined by a single number. A high GDP does not guarantee happiness, and low unemployment does not always mean satisfaction. To build a clearer picture, we analyze multiple factors.

Through our visualization, we will:

- **Use an interactive map of Switzerland**, allowing users to hover over cantons and explore key indicators such as economy, population, and employment.
- **Enable direct comparisons** between two cantons, offering a multi-angle perspective on "Which canton is happier?"
- **Display trends over time**, analyzing how social and economic conditions have evolved across different cantons.
- **Present key insights through visualized data**, highlighting potential happiness indicators such as GDP per capita, employment rate, and demographic composition.

Finally, we want this visualization to go beyond raw statistics—we want users to define happiness in their own way through an interactive and insightful experience.

#### Target Audience

- **Residents and Future Settlers**: Understand the quality of life across different cantons and plan for the future.
- **Curious Minds**: Serves as a storytelling tool that reveals Switzerland’s diversity and unique characteristics.
- **Policy Makers and Administrators**: Analyze economic and social conditions to improve well-being.

### Exploratory Data Analysis

In this part, we illustrate our current dataset.

#### GDP

GDP measures the activeness of the economy. The higher GDP is, the wealthier people tend to be. We have the GDP of each canton from 2008-2022. Here's a graph of the GDP trend of each canton.

![gdp](./fig/gdp_per_canton.png)

We can see that from 2008 to 2022, Zürich(ZH) and Bern(BE) have the largest GDP. The GDP of Zürich has a clear lead, which is almost twice and Bern. Generally, the GDP of Zürich and Bern has a steady growth from 2008 to 2022, while the trend of other cantons is quite stable, without a noticeable increase.

#### Population

Population can serve as an indicator of a society’s vibrancy. Here, we present the population of each canton in 2023.

![population](./fig/population_per_canton.png)

From the figure, the top 5 cantons with the most population is Zürich(ZH), Bern(BE), Vaud(VD), Aargau(AG) and St. Gallen(SG). Again, Zürich has a clear lead, with around 1.3 million people, while the second place, Bern, has around 0.8 million.

#### Employment Rate

Employment rate could reflect the society atmosphere and the potential safety risk, which is an important indicator for happiness.

![employ](./fig/employment_rate_per_canton.png)

For employment rate, Appenzell I. Rh.(AI) ranks first, with employment rate around 70%. Zürich(ZH) and Luzern(LU) come next, both of them around 65%. Ticcino(TI) comes last for employment rate, only barely over 50%.


#### Conclusion

Switzerland is a federal state made up of individual cantons, each with its own unique characteristics. Here, we present a preliminary analysis of a portion of our dataset on happiness. As our project progresses, we will incorporate additional data sources to provide a more comprehensive representation of the happiness index across cantons.

### Related work

We drew inspiration from the two main sources:

1. [**Swiss Federal Statistical Office (BFS) Regional Statistics**](https://www.bfs.admin.ch/bfs/en/home/statistics/regional-statistics/regional-portraits-key-figures/cantons.html): Provides key figures on Swiss cantons but focuses on raw data rather than exploring happiness-related factors.

2. [**Statiswiss Project**](https://com-480-data-visualization.github.io/com-480-project-statiswiss/): An interactive visualization of Swiss statistics, but it presents general socio-economic data rather than analyzing happiness.

Originality of Our Approach:

1. **Happiness Focus**: We explore the relationship between economic, demographic, and employment factors and happiness rather than just displaying statistics.
2. **Direct Canton Comparison**: Users can compare different cantons across multiple indicators to assess disparities in happiness.
3. **Time Trend Analysis**: We visualize changes over time to track how economic and social conditions evolve.

This dataset has not been used in any other course or project before.



## Milestone 2

### Project Goal

The goal of our project, **“Happiness Index Across Swiss Cantons,”** is to explore regional variations in quality of life across Switzerland through a multi-dimensional, data-driven lens. Our aim is not to define happiness with a single metric, but rather to let users interactively explore relevant socio-economic factors and derive their own insights.

#### Sketches of visualisation

##### 1. Visualize Socio-Economic Indicators Across Cantons

We will provide an **interactive choropleth map** of Switzerland where users can:

- **Hover over cantons** to view summaries of GDP per capita, population, and employment rate, etc.

- **Use color gradients** to quickly grasp which cantons rank higher or lower on a selected indicator.

  ![single canton](./fig/sketch_single_canton.png)

##### 2. Enable Canton Comparison

Users can:

- Select any two cantons for **side-by-side comparison**.
- **View charts** (e.g., bar charts or radar plots) showing differences in happiness-related indicators.

![compare cantons](./fig/sketch_compare_cantons.png)

##### 3. Explore Trends Over Time

We will visualize how indicators such as GDP and population have **changed over time** for individual cantons, allowing users to:

- Select a canton and view line charts or area plots.
- Compare historical trends between cantons.

![canton details](./fig/sketch_canton_details.png)

##### 4. Happiness Oriented Display

Since happiness is subjective, we aim to:

- Let users **define their own happiness index** by assigning weights to indicators. Display a dynamic “happiness ranking” of cantons based on user preferences.
- Each indicator is represented by a horizontal percentage bar (slider), visually indicating the current weight assigned to that factor. Users can drag the slider left or right to adjust how important that particular indicator is in their personal happiness definition.

![ranking](./fig/sketch_ranking.png)

#### Tools for the Visualizations

So far, we have used the following tools for building the visualizations:

1. **Vue.js** – For building interactive, component-based web interfaces.
2. **Element Plus** – Provides ready-to-use UI components for consistent and responsive layouts.
3. **AntV (G2, G6)** – Used to create high-quality interactive charts and comparison visualizations.
4. **D3.js** – Powers our customizable geographic maps with fine-grained SVG control.

Very helpful related lectures:

- **Lecture: Practical maps** & **Lecture: Maps** – how to build choropleth maps and map interactivity  
- **Lecture: Perception colors** – how to choose perceptually effective gradients  
- **Lecture: Interactions** – influenced map hover/click behavior design
- **Lecture: Mark, channels** – how we encoded values visually in bar/radar charts  

#### Goals Breakdown

**Core Idea: interactive map of Switzerland**

- Illustrating key indicators such as economy, population, and employment.
- Allowing users to hover over cantons to check the specific statistic of the canton
- Using colors to indicate the value of each canton

**Optional Enhancements:**

1. Enable direct comparisons between two cantons, offering a multi-angle perspective on "Which canton is happier?"
2. Display trends over time, analyzing how social and economic conditions have evolved across different cantons.
3. Enable user defined happiness index, by assigning weights to key happiness indicators such as GDP per capita, employment rate.  **Interactive sliders allow users to intuitively adjust preferences, with instant visual feedback and live-updated rankings**, making the experience both exploratory and engaging.

### Functional Prototype

https://com-480-data-visualization.github.io/com-480-project-Ficciones/


## Milestone 3 (30th May, 5pm)

**80% of the final grade**


## Late policy

- < 24h: 80% of the grade for the milestone
- < 48h: 70% of the grade for the milestone

