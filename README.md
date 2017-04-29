##INTERACTIVE CHART OF THE US HOUSING BOOM/BUST CYCLES

###OVERVIEW
This chart explores the trends of the US housing market from 1963 - 2016.  After exploring data from the US Census Economic Measures Time Series Dataset, the "FOR SALE" and "SOLD" metrics most clearly show the boom and bust cycles over the past 53 years. 

###NARRATIVE STATEMENTS
- The US Housing market experiences periodic boom / bust cycles.
- "FOR SALE" and "SOLD" metrics clearly show these cycles.
- Boom and Bust Cycles are balanced around their 53 year mean.
- The US is currently in a recovery phase, and an imminent bust is unlikely.

###USAGE
- View on bl.ocks.org:
 [http://bl.ocks.org/richl1/raw/9ea4f4cb5ff9a67215b3746bdaf4dbab/](http://bl.ocks.org/richl1/raw/9ea4f4cb5ff9a67215b3746bdaf4dbab/)
- The animation begins showing the boom / bust cycles over the past 53 years.
- Annotations are added at 3 second intervals emphasizing key narratives.
- Buttons are displayed allow users to show/hide the maxima and minima points.
- Hovering over the line charts animates the x and y values.


### DESIGN DECISIONS
- I selected the data set due to my familiarity with it from the EDA project.
- I selected the "For Sale" and "Sold" metrics because they are the clearest Boom/Bust indicators.
- I selected a line chart to highlight the changes over time.
- I animated the drawing of the line chart to emphasize the cycles.
- I normalized the "For Sale" and "Sold" metrics around their means to show how the cycles are balanced around their means.
- I animated annotations at 3 second intervals to emphasize their narrative impact.
- I initially hid the maxima and minima lines to keep the chart from becoming too busy.
- I added user clicked buttons to allow the user to display these lines interactively.
- I added in introduction to the top of the chart based on user feedback.
- Initially, I expected to allow users to view region trends as this data is available.  However, the regional data does not show significant differences and it would have distracted from the overall narrative.

### FUTURE DEVELOPMENT
I believe the visualization could be improved by allowing the user to scroll / zoom on trends at specific times.  At greater zoom levels, I could remove the smoothing of the "SOLD" data to allows users to see the seasonal variations.  Both these addition would require abandoning the DIMPLE.JS chart and the associates x, y coordinate animations.

### FEEDBACK/CHANGES

__Initial Udacity member feedback:__

1. I would suggest making the chart a bit smaller. It takes up the full width of the page which forces the user to scroll back and forth to see the whole image.

1. It might be a good idea to include an introductory paragraph about your visualization (for example, by describing the axis measurements). I find that the length of the y Axis a bit too long to read vertically.

1. I also recommend removing the grey gridlines. This will make your chart look less messy, especially when the maxima and minima lines are showing.

I incorporated all these changes and re-posted a revised request for feedback.  I requested feedback a total of (4) times starting with my initial sketch and at each major revision / git commit.

__First Udacity Review__ Sumbission feedback / updates __(A version is included in the "1st_submission" subdirectory in the GIT repo.)__: 

- Suggestion 1: ... the length of the text is potentially overwhelming

	- I simplified the title and text as suggested.

- Suggestion 2:  ... Minima and Maxima are mathematical terms, ... Between 1995 and 2005 there seems to be two red lines in a row.... , ... What would definitely help is an 'average' line running parallel to the x-axis at 100%...

	- I renamed the terms to "peaks" amd "valleys".  I added the missing "valley" line.  I added a dashed mean line at 100%.

- Suggestion 3: Do you need two Y-axis if they are both based on %. The label could be "HOUSES FOR SALE/SOLD AS A % OF MEAN" You could then outline the mean values for both somewhere else on the graphic?

	- I removed the Text and ticks from the second Y axis; however, dimple.js requires this axis to be present.

__Second Udacity member feadback__  

- Suggestion: I have one suggestion regarding the MINIMA LINE and the MAXIMA LINE buttons. I notice when I click the button, it changes to blue color, however, the MINIMA LINE is green, the MAXIMA LINE is red. I think it might be more consistent if you change the two button colors when clicked to green and red respectively.

	- Changing ther background colors became distracting.  Instead, I used red/green font colors for each button to correspond to each set of lines.


Viewers can review the development steps of the visualization by checking out each git commit and viewing ```index.html``` in a local browser.

###GIT HUB REPOSITORY
- Go to: [http://github.com/richl1/DAND_P6](http://github.com/richl1/DAND_P6)
- Clone the repository with:

$ ```git clone https://github.com/richl1/DAND_P6.git```

$ ```cd DAND_P6```

$ ```python -m SimpleHTTPServer 8000```

Navigate browser to: ```http://localhost:8000/```

GIT HUB currently has (6) commits to track and view the changes to this project.

- The chart includes a single ```index.html``` file
- The dataset is stored in ```rs.tsv``` and is loaded via script.
- CSS styles and javascript sections are included in index.html
- D3.js and Dimple.js are loaded via script
- local viewing is available using python's Simple HTTP Server.
- Files ```DAND_P6.RMD```, ```DAND_P6.html```, ```sketch_v1.html```, and ```rs.txt``` are available to view the original sketch and they are not required or used in the final visualization.

 
###DATASET INFORMATION

- url: [http://wwww.census.gov/econ/currendata/datasets](http://wwww.census.gov/econ/currendata/datasets)

- “Economic Measures Time Series Dataset”

- The original "SOLD" data is very noisy due to large seasonal variations of home sales.  The displayed data is smoothed with a 12 month moving average (6 months before and after).  

###EXPLORATORY DATA ANALYSIS
A thorough exploratory data analysis is available at: 
[http://github.com/richl1/DAND_P4](http://github.com/richl1/DAND_P4)





