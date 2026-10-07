# Near a Hospital, Near a Pharmacy?

A data-visualization assignment examining geographic proximity to
hospitals and pharmacies across urban centres.

## Empirical story

Among 2,345 urban centres with both measurements available, median
hospital proximity is 31.8%, compared with 18.8% for pharmacies.

A within-city comparison shows that hospital proximity is higher in
68.7% of urban centres. Pharmacy proximity is higher in 717 cities,
and 18 have equal proximity. The median within-city hospital-minus-
pharmacy difference is 9.47 percentage points.

The hospital advantage is common, but not universal. Results describe
the available-data sample, not all urban centres worldwide.

## Two presentation versions

The website tells the same empirical story for two audiences:

- Scientific article: static, greyscale figures showing the full
  distributions and paired differences.
- Accessible explainer: directly labelled summaries, plain-language
  explanations, and takeaway-oriented headings.

## Project files

- `index.qmd`: complete Quarto source, including data preparation,
  calculations, figures, explanatory text, and AI Prompt Appendix.
- `index.html`: rendered assignment webpage.
- `urban_health_access.Rproj`: RStudio project file.
- `README.md`: project overview, reproduction instructions, and
  generative AI disclosure.

Earlier exploration scripts are not required to render the final document.

## Data source

The analysis uses `health.csv` from the TidyTuesday release of
29 September 2026:

https://github.com/rfordatascience/tidytuesday/blob/main/data/2026/2026-09-29/readme.md

The source document downloads the CSV directly. Internet access is
therefore required when rendering.

Only urban centres with both hospital and pharmacy proximity
measurements are retained. Missing values are not treated as zero.
The supplied proximity values are already on a 0–100 percentage scale.

Each urban centre receives equal weight. The analysis measures
geographic proximity within 1 km, not healthcare quality,
affordability, service capacity, actual travel time, or utilization.

## Reproducing the website

Requirements:

- R
- Quarto
- R packages `tidyverse` and `janitor`
- Internet access to download the data

Install the required R packages once:

```r
install.packages(c("tidyverse", "janitor"))
```

Open the project in RStudio, open `index.qmd`, and click Render.

Alternatively, run this command in a terminal from the project folder:

```bash
quarto render index.qmd
```

No exploration script or previously created R objects are required.

## Generative AI disclosure

I used Perplexity, a generative AI assistant, to support this assignment.
AI assistance contributed to dataset selection and initial exploration;
development and revision of the narrative; R code for data import,
cleaning, descriptive calculations, and visualization; interpretation
of summary results; and preparation of the Quarto document.

I requested help adapting the same empirical story for scientific and
public-facing audiences, drafting and revising the story summary,
explanatory prose, figure captions, accessibility text, and data/source
note. I also requested step-by-step RStudio and Quarto guidance and
troubleshooting of package compatibility, percentage scaling,
missing variables, plot labelling, axis limits, and document rendering.

The assistance included proposed code and text that I incorporated
into the deliverable, rather than only editing material I had written.
I ran the code and inspected the resulting outputs. Some initial
AI-generated suggestions and code required correction during the
workflow.

AI also assisted with drafting the repository README and organizing
the disclosure and prompt appendix.

The AI Prompt Appendix is included in `index.qmd` and the rendered
website. The complete conversation, including responses and supplied
screenshots, will be retained until the end of the semester for
instructor or TA review.