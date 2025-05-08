# DAV_CA1
For this project, I have constructed a composite index from at least 4 other sub-indices.
This index is based off the net migration of a country, and tries to rank countries based on the question: “What makes a country more or less attractive to live in?”

# Files of Interest
- [Code Implementation & Structured References](https://github.com/cianashby1337/DAV_CA/blob/main/DAV_CA1_main.ipynb)
- [Documentation](https://github.com/cianashby1337/DAV_CA/blob/main/DAV_CA1_Documentation.pdf)

<br>

# Project Summary

## Theoretical Framework
I have conducted a wide literature review to establish the initial, overarching aspects of migration, as well as researching the indicators that may be formed by considering the individual factors of each aspect.

<br>

## Data Selection
I took data from World Bank Group, and assembled it into a workable dataframe for later processing and analysis.
In my early attempts, I used web scraping to gather data from a more difficult source, which had no simple option to download the dataset.

<br>

## Imputation of Missing Data
I used cluster imputation for an indicator that was highly correlated to net migration, despite it's large amount of missing values.
I filled missing values with regards to data in the years before and/or after. If this was not available, I imputed with the median of the column.

<br>

## Multivariate Analysis
I analysed all pairings of independent and/or dependent variables, as well as generating their scatterplots.
A loop was used for generating these comparisons, in favour of scalability when indicators were added or removed from the project.

<br>

## Normalisation
All values were normalized between 0 and 1.
PCA was used immediately after normalization, in an attempt to work with the political indicators that faced multicolinearity.

<br>

## Weighting and Aggregation
The correlations between indicators and net migration were used to weight the indicators, before being added to their relevant sub-index.
Sub-indices were weighted by their R-Squared Adjusted in regards to net migration, before being combined into the main outcome of this project: the composite migration index.
Three main iterations of the index were created throughout my time working on the project, the current one gives the best result I found.

<br>

## Link to other Indices
The net migration indicator was used throughout the project to develop the composite index.
The resulting composite indices were compared to the net migration indicator. The first successful index had an R-Squared Adjusted of 0.8, but the current iteration boasts a greatly improved 0.144.

<br>

## Visualisation of Results
An interactive map was implemented, allowing for ease of determining where countries are ranked highest, as well as quickly being able to find data for a specific country, hovering over it for a display of index scores.
Radar charts were used to show how global regions fared, displaying the average of their countries for each of the four sub-indices.

<br>

## Version Control
Commits were made with close reference to [https://chris.beams.io/posts/git-commit/](https://chris.beams.io/posts/git-commit/)
VSCode was set to limit the commit subject line to 50 characters, and each line of the commit body to 72 characters.

<br>

## Documentation
The project has been summarized in a document with styling that has been given some effort, yet remains simplistic. 
The main functional aspect of styling in this document is to draw attention to, and provide clarity on, sections of tables that are of interest to the reader.

## References
References can be found either in the documentation, or the main .ipynb file.
The .ipynb file references have been organised under relevant headings, providing context for their usage.
