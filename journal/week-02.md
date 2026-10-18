# Week 2 Journal

**Topic:** From Tables to Visual Arguments: CSV structure and RAWGraphs

## 1. What material did I work with?

The provided CSV file and its key in the data dictionary file, Microsoft Excel, RAWGraph, one dataset provided by RAWGraph (for the independent graph).

## 2.	What transformation did the tool perform?

Upon importing the CSV file, RAWGraphs took that data and transformed it into a table structure, including the creation of a header row. It also automatically assigned data types (number, string or date) to the table fields. One of them I had to manually correct (see my answer to question 3). Once I chose a graph type and started configuring the graph, RAWGraph used the data to create a chart from it.

## 3.	Which decisions did I make?

I changed the format of `year` to string, since there were a couple of values in that column that did not meet the criteria for numeric values (like the numbers being surrounded by square brackets). This is generally not ideal, but since we also have `year_numeric`, it is fine in this exercise, since we can use the values in that column instead.

For the line chart, I decided to use “linear” as the setting for the type of line to create to reflect the actual data a little better instead of smoothing the lines. I also decided to create a second version of the line chart where I switched `year_numeric` to date format to get rid of the thousands separator in the x-axis labels. I left `year_numeric` as a date format for the beeswarm chart.

## 4. What failed, remained unclear, or produced an unexpected result?

I did not find a way to move the description of the x-axis so that it would not appear on top of the rightmost bar, so I decided to change the color of the bar chart to at least make the text more legible.

The beeswarm chart required a lot of tweaking to be displayed correctly, since it originally did not fit the canvas and there was no pre-set colors scheme that was both easily distinguishable and had enough colors.

## 5.	What does the output allow me to infer historically?

Considering the non-representativeness of the dataset, quite little. It does generally provide some titles and printers and languages from the Swiss Confederation and the Holy Roman Empire, so it is possible to make some very basic judgements like "there were books published in Latin in the Holy Roman Empire" (with varying amounts of additional data).

## 6.	What does the output not allow me to infer?

Considering the data is not exhaustive nor representative, it is not possible to infer the actual proportions/ratios of languages, formats or any other data point provided.

## 7.	Could this method contribute to my final project? Why or why not?

Maybe! I am frustrated by the limitations of the tool when it comes to customizing how the graph looks when it comes to font, font size, legend, etc. However, considering it produces .svg files, it might be possible to edit those to correct some things I am not happy with.
