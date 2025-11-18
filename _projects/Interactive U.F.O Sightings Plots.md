---
name: Interactive U.F.O Sightings Plot
tools: [Python, HTML, vega-lite, Altair]
image: assets/pngs/cars.png
description: This is a webpage to show U.F.O sightings within the U.S and around the country!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Interactive Plot of U.F.O Sightings

A [U.F.O](https://en.wikipedia.org/wiki/Unidentified_flying_object) or also know as an Unidentified Flying Object is a flying object that cannot be immediately identified by an observer. While this can mean anything, it specifically leans towards those of extraterrestrial spacecrafts. While U.F.Os usually associate with Aliens, that is not always the case.


This first chart below, shows the top 10 states that have seen the most U.F.Os. I decided to create this visualization using a barchart to show each state on the left side versus the amount of times each U.F.O has been seen for that state.

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart_by_states.json" style="width: 100%"></vegachart>

# Interactive Line Chart (Top)

This is an interactive line chart comparing both the amount of times a U.F.O has been spotted per month over different years. As I was making the line chart, I decided to group everything on the x-axis by the dates such as months and years with the y-axis having a quantitative encoding to show the total number of sightings per month. Additionally, I decided to use a brush to demonstrate the interaction allowing users to pick between what years they want to investigate.

# Barchart (Bottom)

for this visualization, it shows a barchart of the U.F.O shapes over the years versus the amount of sightings. I decided to use a barchart because it was the easiest to compare different values based on categories. In the chart the x-axis shows a count of sightings, with the y-axis showing shapes such as oval, disk, light, cylinder, etc. Additionally, I also chose a rainbow color scheme to map out each catagory since it used light colors for each bar. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart_b_and c_interactive.json" style="width: 100%"></vegachart>

## Interactivity Discussion

When making the interactivity between graphs, I noticed that there were different columns that showed the shapes, the amount of times that shape was shown, and time (month and years). So I wanted to make a way to a way where I can demonstrate that, which I did using the brush selection. When you drag over a specific period of time on the interactive chart, you will notice that the chart underneath will adjust and chance based on those years you have selected. I believe this interactive visulization was a good way for those who want more information about U.F.O shapes over the years to learn more about it. 

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Jaylin2436chen/Jaylin2436chen.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

