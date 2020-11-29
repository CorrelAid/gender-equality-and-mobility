gender-equality-and-mobility
==============================

# Analysis of gender differences in Madrid mobility data 

See the blog article with the results here: [xxx](LINK)

## About the project:

Women’s travel patterns differ from men’s in many ways: women are likely to travel shorter distances than men, are more likely to use public transportation, engage in more non-work travel outside rush hours and make more multi-stop trips, run household errands and escort other passengers (usually children or dependent elderly persons). Some of these differences are going to become less relevant once gender differentiation in parental models, the labour market etc. becomes less relevant, but others will continue to play a role.
(also see https://civitas.eu/sites/default/files/civ_pol-an2_m_web.pdf).

### The data

Madrid (CRTM: Consorcio Regional de Transportes de Madrid), unlike most other cities, provides a rich open data set on survey data on mobility behaviour of ~85.000 people with ~220.000 individual trips.

The description and results can be found here (in spanish):
https://www.crtm.es/media/712934/edm18_sintesis.pdf

The data here: https://crtm.maps.arcgis.com/apps/MinimalGallery/index.html?appid=a60bb2f0142b440eadee1a69a11693fc

The shapes:
(different granuality of zones - dataset in fines granulaity of 1259 zones)
https://datos.crtm.es/datasets/zonificacionzt1259
https://datos.crtm.es/datasets/zonificacionzt208
https://datos.crtm.es/datasets/zonificacionzt84

### Research questions:

- Can we reproduce the results on gender differences from other studies?
- Do we find additional differences with an exploratory analysis?
- How large is the effect and how much of the difference can actually be explained by gender - or other socioeconomic factors (e.g. children, age, education, type of employment - part-time, type of job, distance to workplace)?
- Can we find evidence that the existing public transport network is more efficient for one gender group?

## Getting started:

- create a conda env with the environment.yml file:

    conda env create -f environment.yml
    
- run all notebooks on the given order
    
### Notebook overview:

- `00_setup.ipynb`: download data and preprocess for further analysis
- `01_descriptive_analysis.ipynb`: all analyses and plots for descriptive analysis
- `02_ModelPTspeed.ipynb`: regression model to test if speed differs significantly between genders when controlled for distance
- `03_public_transport_routing.ipynb`: test speed difference between genders by comparison of pt routing / car routing ratio

Further analyses that are not part of the blog post are stored in `notebooks/initial_exploration`


Project Organization
------------

    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── environment.yml   <- The yaml file for reproducing the analysis environment

