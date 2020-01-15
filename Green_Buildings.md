**Visual story telling: Green buildings**
-----------------------------------------

### **Problem**

An Austin real-estate developer is interested in the possible economic
impact of “going green” in her latest project: a new 15-story mixed-use
building on East Cesar Chavez, just across I-35 from downtown. Will
investing in a green building be worth it, from an economic perspective?
The baseline construction costs are $100 million, with a 5% expected
premium for green certification.

The developer has had someone on her staff, who’s been described to her
as a “total Excel guru from his undergrad statistics course,” run some
numbers on this data set and make a preliminary recommendation. Here’s
how this person described his process:

> I began by cleaning the data a little bit. In particular, I noticed
> that a handful of the buildings in the data set had very low occupancy
> rates (less than 10% of available space occupied). I decided to remove
> these buildings from consideration, on the theory that these buildings
> might have something weird going on with them, and could potentially
> distort the analysis. Once I scrubbed these low-occupancy buildings
> from the data set, I looked at the green buildings and non-green
> buildings separately. The median market rent in the non-green
> buildings was $25 per square foot per year, while the median market
> rent in the green buildings was $27.60 per square foot per year: about
> $2.60 more per square foot. (I used the median rather than the mean,
> because there were still some outliers in the data, and the median is
> a lot more robust to outliers.) Because our building would be 250,000
> square feet, this would translate into an additional $250000 x 2.6 =
> $650000 of extra revenue per year if we build the green building.

> Our expected baseline construction costs are $100 million, with a 5%
> expected premium for green certification. Thus we should expect to
> spend an extra $5 million on the green building. Based on the extra
> revenue we would make, we would recuperate these costs in
> $5000000/650000 = 7.7 years. Even if our occupancy rate were only 90%,
> we would still recuperate the costs in a little over 8 years. Thus
> from year 9 onwards, we would be making an extra $650,000 per year in
> profit. Since the building will be earning rents for 30 years or more,
> it seems like a good financial move to build the green building.

> Goal: The developer listened to this recommendation, understood the
> analysis, and still felt unconvinced. She has therefore asked you to
> revisit the report, so that she can get a second opinion.

### **Visualizations**

<img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-5-1.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-5-2.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-5-3.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-5-4.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-5-5.png" width="50%" />

**Observations**

-   Rent is correlated with the cluster rent
-   Rent is correlated with the size, as expected
-   Most of the class A buildings are also younger
-   Age does not have a high correlation with rent
-   Class a buildings get higher rent as they are premium buildings

<img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-6-1.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-6-2.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-6-3.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-6-4.png" width="50%" />

**Observations**

-   Most of the green buildings are younger than non-green buildings
-   The proportion of class a buildings is higher in green buildings
-   The proportion of green and non-green building increases as the size
    of buildings increases
-   The is a significant difference in the of rent of class a and
    non-class a buildings

<img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-7-1.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-7-2.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-7-3.png" width="50%" /><img src="Green_Buildings_files/figure-markdown_strict/unnamed-chunk-7-4.png" width="50%" />

**Observations**

-   For a size of 250,000 sqft, the green buildings have a higher rent
    when it is a class a building
-   The rent of green buildings is lower than non-green ones when they
    are not class a buildings
-   The rent difference is not uniform across different sizes and ages

### **Insights and Recommendations**

We have seen that the analysis by stats guru is flawed since he fails to
account for all the factors that affect the rent. First, he used the
median rent of all buildings to calculate the returns. Hence he fails to
accout for other factors such as size and class of the buildings into
his analysis. For instance, we have seen that class a buildings will
yield a higher rent than non green buildings that are class a.

**Calculations**

-   The rent difference is not uniform across different sizes and age,
    so we cannot use a fixed difference in rent to calculate the returns
-   For the same reason, we should consider only the buildings that have
    sizes between 200k and 300k sq.ft
-   We should also use the median leasing rate of such buildings instead
    of 90% rate
-   The data provided does not have information about class a buildings
    with sizes ranging from 200k sq.ft to 300k sq.ft. So let’s use
    average 5 year return to arrive at final recommendations

**Final recommendation**

-   If the building is not a Class-A building, it is not wise to invest
    in a green building since the average returns for 5 years are
    negative
-   The builder should invest in a Class-A green building to yield
    positive returns
-   We can expect a occupancy rate of 91.6% on such buildings
-   The average difference in rent for green and non-green buildings
    that are class a and whose sizes ranging from 200k to 300k is 3.097
-   Hence, for a 250k sq.ft building at 91.6% occupancy, we expect to
    recuperate the costs in 7.05 years
