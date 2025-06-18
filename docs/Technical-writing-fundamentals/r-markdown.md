# R Markdown Guide

R Markdown is an authoring framework that combines code, output, and narrative text into a single document. It is widely used in data science, research, and reporting for creating dynamic and reproducible documents.

## What You Need to Get Started

- **R**: Download from [CRAN](https://cran.r-project.org/)
- **RStudio**: IDE for working with R Markdown ([Download](https://www.rstudio.com/products/rstudio/download/))
- **rmarkdown package**: Installed via RStudio or `install.packages("rmarkdown")`


## Beginner Level
### What is R Markdown?

R Markdown lets you:

- Combine code (R, Python, SQL, etc.) and its output with markdown-formatted text
- Generate reports in HTML, PDF, Word, and more

### Basic Syntax

```markdown
# This is a heading

**Bold text** and *italic text*

- Bullet list item
- Another item
```

## Code Chunks

```r
# This is an R code chunk
summary(cars)
```

### Rendering the Document
Click the **Knit** button in RStudio, or run:

```r
rmarkdown::render("my_file.Rmd")
```
### Output Formats
`.html` (default)

`.pdf` (requires LaTeX)

`.docx`

## Intermediate Level
### YAML Header
```yaml
---
title: "My Report"
author: "Your Name"
date: "2025-06-10"
output:
  html_document:
    toc: true
    number_sections: true
---
```
### Code Chunk Options
```r
# Custom chunk behavior
plot(cars)
```
### Inline Code

```markdown
The mean speed is `r mean(cars$speed)` mph.
```
### Including Plots & Tables

```r
library(ggplot2)
ggplot(cars, aes(speed, dist)) + geom_point()
```

### Parameters in R Markdown

```r
params:
  dataset: "cars"

data(get(params$dataset))
summary(get(params$dataset))
```

## Expert Level
### Custom Templates

Use the `rmarkdown::draft()` function to create custom templates:

```r
rmarkdown::draft("new_report.Rmd", template = "html_vignette", package = "rmarkdown")
```
### R Markdown with Python (reticulate)

```python
import pandas as pd
data = pd.read_csv('data.csv')
data.head()
```
### Interactive Documents

```r
output:
  html_document:
    code_folding: show
    theme: readable
```

### Dashboards with `flexdashboard`

```r
install.packages("flexdashboard")
---
title: "My Dashboard"
output: flexdashboard::flex_dashboard
---
```
### Bookdown and Blogdown
- **Bookdown**: Create books and reports

- **Blogdown**: Create websites/blogs with R Markdown

```r
install.packages("bookdown")
bookdown::render_book("index.Rmd")
```

### Next Steps:
- Explore the [R Markdown Cookbook](https://bookdown.org/yihui/rmarkdown-cookbook/)
- Check out [RStudio's official R Markdown page](https://rmarkdown.rstudio.com/)
- Practice by creating your own `.Rmd` documents and rendering them into different formats
