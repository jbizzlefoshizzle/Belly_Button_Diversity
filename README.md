# Interactive Dashboard - Belly Button Biodiversity

![Bacteria by filterforge.com](images/bacteria.jpg)

For this project, I built an interactive dashboard to explore the [Belly Button Biodiversity dataset](http://robdunnlab.com/projects/belly-button-biodiversity/), which catalogs the microbes that colonize human navels.

The dataset reveals that a small handful of microbial species (also called operational taxonomic units, or OTUs, in the study) were present in more than 70% of people, while the rest were relatively rare.

## Using Plotly
### Horizontal Bar Chart
Using the d3.js library to read in `samples.json`, 
I created a horizontal bar chart with a dropdown menu to display the top 10 OTUs found in that individual.

* `sample_values` defined the values for the bar chart.

* `otu_ids` are the labels for the bar chart.

* `otu_labels` as the hovertext for the chart.

  ![bar Chart](images/horizontal-bar-chart.png)
### Gauge Chart
* Adapted the Gauge Chart from <https://plot.ly/javascript/gauge-charts/> to plot the weekly washing frequency of every individual,
modifying the example gauge code to account for values ranging from 0 through 9.
![gauge-chart](images/gauge.png)
### Bubble Chart
A colorful bubble chart that displays each sample.

* `otu_ids` for the x values, `sample_values` for the y values.

* `sample_values` for the marker size.

* `otu_ids` for the marker colors.

* `otu_labels` for the text values.

![Bubble Chart](images/bubble_chart.png)

Each sample's metadata, i.e., an individual's demographic information,
are displayed by highlighting each key-value pair from the JSON object.

![metadata](images/metadata.png)

The dashboard dynamically updates all of the plots any time that a new sample is selected!

The initial dashboard is shown below:

![dashboard](images/complete-layout.png)

## Deployment

The app was deployed to GitHub Pages, a free static page hosting service.

### About the Data

Hulcr, J. et al.(2012) _A Jungle in There: Bacteria in Belly Buttons are Highly Diverse, but Predictable_. Retrieved from: [http://robdunnlab.com/projects/belly-button-biodiversity/results-and-data/](http://robdunnlab.com/projects/belly-button-biodiversity/results-and-data/)

- - -

© 2019 Trilogy Education Services
