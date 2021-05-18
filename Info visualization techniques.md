# Info visualization techniques




| Names               | Plots                                                        |
| ------------------- | ------------------------------------------------------------ |
| **Distribution**    | [Violin](#violin), Density, Histogram, Boxplot, Ridgeline               |
| **Correlation**     | Scatterplot, heat map, Correlogram, Bubble, Connected Scatter, 2D density |
| **Ranking**         | Barplot, Spider / Radar, Word Cloud, Parallel, Lollipop, Circular Barplot |
| **Part-of-Whole**   | Treemap, Venn diagram, Donut, PieChart, Dendogram, Circular Packing |
| **Evolution**       | Line chart, Area chart, Stacked area, Streamgraph            |
| **Maps**            | Maps, Choropleth, Hexbin, Cartogram, Connection, Bubble      |
| **Flow**            | Chord Diagram, Network, Sankey, Arc Diagram, Edge Bundling   |
| Commons Conventions |                                                              |

> Documented by following definitions and examples from:
>
> - https://www.data-to-viz.com/
>
> - https://datavizcatalogue.com
>
> - https://www.python-graph-gallery.com/



## Distribution													

Visualization methods that display frequency, how data spread out over an interval or is grouped.

###  Violin plot

Violin plot is a method of visualizing the distribution of data and its probability density. It is a combination of box plot and density plot that is rotated and placed on each side to show distribution shape of data. The difference with boxplot is particularly useful when the data distribution is multimodal (more than one peak)

Violins are particularly adapted when the amount of data is huge and showing individual observations gets impossible. For small datasets, a [boxplot with jitter](http://www.data-to-viz.com/caveat/boxplot.html#boxplotjitter) is probably a better option since it really shows all the information.

<u>Libs/Examples for plotting them:</u> 

- [Seaborn](https://seaborn.pydata.org/generated/seaborn.violinplot.html)

- [ggplot2](http://www.r-graph-gallery.com/95-violin-plot-with-ggplot2)

- [D3.js](http://bl.ocks.org/z-m-k/5014368)

### Density plot

As known as *Kernel Density Plots, Density Trace Graph*. A density plot is a representation of the distribution of a numeric variable. It uses a kernel density estimate to show the probability density function of the variable. It can be thought of as a smoothed version of the [histogram](https://www.data-to-viz.com/graph/histogram.html) and is used in the same concept. They are very well adapted for large dataset, as stated in data-to-viz.com

An advantage Density Plots have over Histograms is that they're better at determining the [distribution shape](https://en.wikipedia.org/wiki/Shape_of_the_distribution) because they're not affected by the number of bins used (each bar used in a typical histogram). Don’t compare more than 3 groups on the same density plot. The graphic gets cluttered and hardly understandable. Instead use a violin plot, a boxplot, a ridgeline plot or use small multiple.

<u>Libs/examples for plotting them:</u>

- [D3.js](https://www.d3-graph-gallery.com/histogram.html)
- [Seaborn](https://www.python-graph-gallery.com/density-plot/)



### Histogram

A Histogram visualises the distribution of data over a continuous interval or certain time period. Each bar in a histogram represents the tabulated frequency at each interval/bin. It allows to compare the distribution of **a few** variables. Don’t compare more than 3 or 4, it would make the figure cluttered and unreadable.

Don’t confound it with a [barplot](https://www.data-to-viz.com/graph/histogram.html). A barplot gives a value for each group of a categoric variable. Here, we have only a numeric variable and we chack its distribution.

### Boxplot

It is a method for graphically depicting groups of numerical data through their [quartiles](https://en.wikipedia.org/wiki/Quartile). Box plots may also have lines extending from the boxes (*whiskers*) indicating variability outside the upper and lower quartiles

### Ridgeline

Ridgeline plots are partially overlapping line plots that create the impression of a mountain range. They can be quite useful for visualizing changes in distributions over time or space. An exellent [article](https://cran.r-project.org/web/packages/ggridges/vignettes/introduction.html#:~:text=Ridgeline%20plots%20are%20partially%20overlapping,distributions%20over%20time%20or%20space.).

## Correlation

### Scatterplot

### Heatmaps

### Correlogram

### Bubble

### Connected Scatter

### 2D density

