Flight Cancellation Visual

Summary

It would have been the most disappointing thing if your flight were cancelled when you were just ready and looking forward to boarding. Here is the visual cancellation data for the year 2008 including 19 airlines in US. It tells us Envoy Air (MQ) has the most cancellation rate while Frontier Airlines (F9) has the least cancellation amount. By clicking for the airline details, we can see the months December, January and February have the higher cancellation rate than months in fall. Thus, this might be a better choice if you plan to travel in fall. Note that the trend of cancellation rate due to weather is similar to the trend of all cancellation rate for most of the carriers, weather is likely to be the major reason for the cancellation rate fluctuation.

Here is the data visualization on line:
http://bl.ocks.org/Moshangtang/raw/75bf8fbdab9ae7afbfb66eaafad15bd4

Design

The dataset I chose is the flight data in year 2008 from the website:  http://stat-computing.org/dataexpo/2009/the-data.html. I would like to explore the cancellation rate as well as its relationship with months for each airline in US.

In order to do the visualization, I firstly looked through the data and chose the fields of interests: UniqueCarrier, Months, CancellationCode(cancellation reasons) and the Cancel. I grouped the data by UniqueCarrier, Months and CancellationCode and calculated the cancellation amount for each group. The final dataset I used for visualization is in 2008cancel.csv file.

I think the best way to visualize it is to use stacked bar chart since I would like to show both of the total cancellation amount and the individual cancellation amount due to different reason. So I used the stacked bar charts for all the figures. Together with the cancellation amount charts for each airlines, I created buttons for the cancellation amount vs. months for each airlines. Because I also want to convey the information of cancellation type, I decided to use different colors for different types. The weather type was put in the bottom because I want to have a scatter line to show the trend of its change during months. In this way, I can compare it with the trend of the total cancellation rate. If I put it on the top, I cannot show this trend. The first version is kept in index1.html.

Based on feedback to version 1, I fixed the “All” button, which was not working fine on multiple clicks. I also added the title for each charts for clearer depiction. The sub-header were also modified to clarify my story. Index2.html was created with these modification.

After hearing from my second reviewer, I added the guide information to clarify the reasons for cancellation in detail to avoid the situation that the reader does not know the meaning of cancellation term. This was in my index3.html.

Based on the feedback from Andrew, the mentor in Udacity, I realized that the cancellation amount is not a good parameter for depicting my story while the cancellation rate is. Cancellation rate is the cancellation amount divided by the total amount of flights for one airline. I modified the dataset and redraw the chart. Also, per his suggestion, I added scatter-lines for the charts of each airline to depict the trend by month of the total cancellation rate and the cancellation due to weather for each of the airline. This can lead to a finding that the major reason for cancellation is weather. All these updates are included in my index4.html

Finally, I added the necessary comments for better understand the code. Also, I updated the title to avoiding the confusion of the depiction of all my data according to the reviewer’s suggestion. The final version of my code is in index_final.html.

Feedback

1. 1st Feedback:
•   On first look, it seems chart is missing header. Though you have provided page header and summary, but first chart that appears should have header as it is not immediately clear what this chart is depicting.
•   Instead of stacked bar chart, you could also try grouped bar chart.
•   You should improve header to show relationship is between months and number of cancellation as on first page there is different relationship.
•   "ALL" button is not working fine on multiple clicks.

   Reply to 1st Feedback:

•   As the reviewer’s feedback, I added headers for every chart in order to let the reader immediately clear what the chart is showing.
•   In this case, I think stacked bar chart is more suitable for my topic since I want to show both the total cancellation rate and the individual cancellation rate by different reason.
•   The sub-header was modified to clarify the features of interest for the charts and the relationships I would like to explore.
•   "ALL" button was fixed.

2. 2nd Feedback:
•   Is there any green bar in the graph?
•   Does “carrier” for blue color mean cancellation due to carrier reasons?

   Reply to 2nd Feedback:
•   The cancellation rate due to the security is too small to view. However, the legend shows the existence of the green bar.
•   To clarify this question, I added the guide text which is “Reasons for Cancellation” to explain each term in detail.

3. 3rd Feedback:
This is a very cool visualization. I really like the stacked bar plots showing the number of flights cancelled by cause. The feature allowing the viewer to see flight cancellations by month and per airline is well conceived and executed. Here are some recommendations to consider:
•   The visualization could be more explanatory consider showing some trends in the data, the first thing that comes to mind is trend by month and within that, by cause (is weather the main reason for the month trend?).
•   The other thing to consider is to use proportion or rate instead of raw counts. That is, one airline may have more cancellations than another or one month may have more than another, but is this a function of how many flights occurred, that is one airline or month may have significantly more flights but the same cancellation rate.

   Reply to 3rd Feedback:
•   The scatter-lines are added to depict the trend by month of the total cancellation rate and the cancellation due to weather for each of the airline. Since the trend of these two rate looks similar, I would say, the main reason for cancellation is weather.
•   I think the reviewer was absolutely right in this point, so I replace the amount with the cancellation rate as the data.

References:

http://www.w3schools.com/tags/
https://github.com/d3/d3-3.x-api-reference/blob/master/API-Reference.md
https://discussions.udacity.com/c/nd002-p6-data-visualization-with-d3-js?_ga=1.225523672.311546568.1472610737
https://github.com/PMSI-AlignAlytics/dimple/wiki/dimple.axis#properties-1
http://stackoverflow.com/
http://stackoverflow.com/questions/19384532/how-to-count-number-of-rows-in-a-group-in-pandas-group-by-object


