# Bayesian Analysis of Soccer Penalty Kicks

Dailin Pan · STATS 551 Final Project

How should we compare penalty takers when many have attempted only one or two kicks? This project uses a hierarchical Beta–Binomial model to estimate player-level conversion probabilities with partial pooling. The report analyzed 482 kicks from 180 players in Serie A, the Premier League, and Primeira Liga.

[`penalty-kick-analysis.Rmd`](penalty-kick-analysis.Rmd) contains the complete workflow from data cleaning to player rankings, predictive checks, and shrinkage plots. The Stan model is embedded in the notebook.

## Reproduce the analysis

1. Download the [Penalty Kick Dataset (2020–2025)](https://www.kaggle.com/datasets/rodrigoarede2003/penalty-kick-dataset-20202025) and place `real_data.csv` next to the notebook. If the download is an Excel workbook, export the data worksheet as a UTF-8 CSV named `real_data.csv`, keeping the original column names. If you already have the report's cleaned CSV, you can use it at `data/pen_clean.csv` in place of the raw file.
2. Use R with Pandoc and a C++ toolchain compatible with RStan. Install the required R packages once.

   ```r
   install.packages(c("rmarkdown", "tidyverse", "janitor", "gridExtra", "rstan"))
   ```

3. From the project directory, render the notebook to generate `penalty-kick-analysis.html`.

   ```r
   rmarkdown::render("penalty-kick-analysis.Rmd")
   ```
