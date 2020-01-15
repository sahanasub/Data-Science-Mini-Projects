**Visual story telling: flights at ABIA**
-----------------------------------------

### **Problem**

Consider the data in ABIA.csv, which contains information on every
commercial flight in 2008 that either departed from or landed at
Austin-Bergstrom Interational Airport.

Your task is to create a figure, or set of related figures, that tell an
interesting story about flights into and out of Austin. You can annotate
the figure and briefly describe it, but strive to make it as stand-alone
as possible. It shouldn’t need many, many paragraphs to convey its
meaning. Rather, the figure should speak for itself as far as possible.

### **Visualizations**

We have in hand, the ‘flight’ data during the year 2008 at Austin
airport. Let’s do some exploratory data analysis and try to isolate the
patterns/behaviour. We are looking at around 100k records of flight data
in 2008 here, primarily focussing on the air traffic and delays.

From the histograms of arrival and departure delays, its conclusive that
both are centred around a mean of ZERO. We are observing a similar trend
with a few outliers (values close to 500 minutes).

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-5-1.png)![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-5-2.png)

We will analyse the correlation between arrival and departure delays to
understand if any particular carrier is deviating from the normal
behaviour. For couple of carriers, there are a few outliers as expected
from the distribution plot. Almost perfect correlation between the
delays except for a few carriers who did compensate for the departure
delays(Arrival delay almost none for such observations).

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-6-1.png)

We will try to visualize the correlation for carriers individually.
Visually, the slope of the plots remain roughly constant, so NO carriers
are consistently making up for the departure delays.

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-7-1.png)

<table style="width:56%;">
<colgroup>
<col style="width: 55%" />
</colgroup>
<thead>
<tr class="header">
<th>Air carrier operation at Austin Airport</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Next we will shift our focus to the Carrier operation at Austin Airport. Southwest(WN) tops the list with almost 40k operations, followed by Alaskan Airlines(AA). Northwest Airlines(NW) has the fewest operations -121.</td>
</tr>
<tr class="even">
<td><img src="ABIA_flights_files/figure-markdown_strict/unnamed-chunk-8-1.png" /></td>
</tr>
<tr class="odd">
<td>Lets try to find out which carrier you can trust the most before planning your next flight!</td>
</tr>
<tr class="even">
<td>According to the Probability of carrier delay in excess of 30 mins: 1. Southwest(WN) and Frontier Airlines(F9) have the lowest 2. YV and 9E have more than 60% chance. We observed a big outlier for 9E earlier, so could be one of the reason.</td>
</tr>
<tr class="odd">
<td>Reliable Carriers: Southwest(WN) seems to be the most reliable. Even with 40k operations, the avg carrier delay is just 18 mins. Avg departure delay is less than avg carrier delay. We have a few airlines – F9 MQ, US, WN and XE with less that 30% probability, but the # of operations are less. We feel Alaskan Airlines(AA) with close to 20k operations outperforms a lot of carriers with way fewer number of operations.</td>
</tr>
<tr class="even">
<td>Unreliable Carriers: 1. 9E and YV seems to have an avg carrier delay in excess of 1hr. 2. With just 121 operations, NW has a high avg carrier delay of 48 minutes.</td>
</tr>
<tr class="odd">
<td><img src="ABIA_flights_files/figure-markdown_strict/unnamed-chunk-11-1.png" /><img src="ABIA_flights_files/figure-markdown_strict/unnamed-chunk-11-2.png" /></td>
</tr>
<tr class="even">
<td>Types of Delays encountered:</td>
</tr>
</tbody>
</table>

Most frequently occurring and total delay time in minutes- NAS Delay,
Late Aircraft and Carrier delay

Least- Security Delay

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-12-1.png)![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-12-2.png)

Delay of flights departing from Austin - month-wise split Sep, Oct and
Nov have the least

    ## # A tibble: 12 x 3
    ##    Month dep_delay arrdelay
    ##    <fct>     <dbl>    <dbl>
    ##  1 1         26593    20660
    ##  2 2         33638    25792
    ##  3 3         51801    47646
    ##  4 4         27112    26020
    ##  5 5         33996    26510
    ##  6 6         45401    50434
    ##  7 7         34364    28604
    ##  8 8         32277    25408
    ##  9 9          7745      -79
    ## 10 10        11606     4005
    ## 11 11        12796     2421
    ## 12 12        45685    37162

Lets try to understand how the delays vary across months. Maximum delay
times are observed during the months of March, June and December.
September, October and November are the least(Air traffic is also less
during these months).

December month seems to be interesting !! Low air traffic, but high
delays observed.

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-17-1.png)

Number of Flights by month. Arrivals and Departure numbers are similar.

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-19-1.png)

<table>
<tbody>
<tr class="odd">
<td style="text-align: left;">Air traffic hours at Austin Airport</td>
</tr>
</tbody>
</table>

Number of Departures- 49623 Number of Arrivals- 49637

Plot C suggests that there are a lot of late night arrivals. Literally
very few departures post 9 PM

High number of departures are observed between 6AM and 8AM.

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-22-1.png)

Not much insights across months except for the fact that there is a dip
during the low traffic months - Sep, Oct, Nov. 

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-23-1.png)

Traffic combining Departures and Arrivals:
------------------------------------------

11 AM to 5PM seems to be the busiest time at Autin Airport. Airtraffic
is really low during early morning hours until 5AM.

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-25-1.png)

Lets analyse a little on weather delay across months. We think weather
delay combined with tourist activity could be an issue with December.We
are considering only the delays caused in excess of 15 minutes

Both the number and minutes of weather delay peaks during March for
Departures. There is a high weather delay count in the month of December
for Arrivals ONLY, which could may imply the delays are not caused at
Austin airport !!!

![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-28-1.png)![](ABIA_flights_files/figure-markdown_strict/unnamed-chunk-28-2.png)
