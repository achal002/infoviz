# infoviz

https://www.cs.odu.edu/~achalke/cs725/

**Introduction:**

I was contemplating on what to do with my project. I was exploring the various ideas that would captivate a reader’s interest. One day, I was just scrolling through my news feed and I read an article about the Indian currency deprecating. Initially, Indian currency was performing badly and it reached the value 74.33 USD in the year 2018. But later in March 2019, INR dropped to 68 USD. I, then, decided to explore this further. Being an international student in the US, the rise and fall of the Indian Rupee is a topic of concern as well as interest for me.

At first I came up with questions like: What are the major factors affecting the Indian currency? Have these factors affected any other currency as well? How are normal people impacted by the change in the currency value?

On further investigation, I found out that these are the factors that affect the currency exchange rate: inflation rate, exchange rate, government debt, terms of trade , political stability, and performance. 
The rate of inflation can have major impact on the values of the country's currency. A high inflation rate is very likely to impact country's exchange rates with other nations negatively. Inflation rates, interest rates, and exchange rates are highly correlated. And then exports and imports are also major factors that affect the currecy. The exports, imports, and the exchange rates have a complicated relationship because of the feedback loop between them. The exchange rate has an effect on the trade surplus, whihc in turn affects the exchange rate.

Considering all the factors that affect the currency will make it difficult to explain. So, I decided to modify my question a bit. To continue with the project, I decided to consider imports and exports being the two major factors. What’s happening to the Indian currency? How are exports and imports affecting the currency? These factors are indeed inter-related, meaning the change in INR affects the exports and imports cost and that, in turn, affects the INR.



**Data:** 

Data was not readily available I had to collate the data from different sources. There was a problem gathering data as there was a slight change in the data on every site, so I decided to go with the data that was that was similar and looked through several articles as well to understand about the exports and imports. I then collated the data and used them for my charts.
* https://tradingeconomics.com/india/exports
* https://data.gov.in/
* https://data.worldbank.org/indicator/ne.exp.gnfs.zs
* https://atlas.media.mit.edu/en/visualize/tree_map/hs92/export
* https://atlas.media.mit.edu/en/visualize/tree_map/hs92/import
* https://www.investing.com/currencies/usd-inr-historical-data

**Visualization:** 

History of INR :

This is the first chart in my project, I have plotted the currency rates from year 2015 for every month. I have also added a feature to the graph where you can zoom in to a certain timeframe. 
From this graph we can see that the INR rate had a lot of ups and downs over the years, but in the year 2018 it reached it’s highest , it was $74.33. But later , it started falling. INR was performing bad in the year 2018 but, something happened in 2019 that improved the performance of the Indian Rupee. Additionally, it was listed as the best performing currency in Asia, at the beginning of 2019. 
 
 
The next chart lists the two major factors that I want to talk about, with the INR. I later realized that this was not the right way to represent a bar chart as the attributes have different scales (imports and Exports are represented in $USD billion, and INR as per USD).
 
For the next chart I have two graphs plotted side by side to actually see the change in currency and change in imports and exports.
 
The last chart is a line chart that shows the trend of the imports and exports. 
The red line represents exports and the blue line represents imports. From the line chart we can see that the imports were always been higher when compared to the exports. But for the year 2017 – 2018 the imports prices started increasing and reached the highest by the end of 2018.  
And like we discussed earlier more imports means more Indian money is being converted into dollars and causing trade deficit and that will bring affect the Indian currency. 
Later in the year 2019, we see that the imports started to fall and the exports prices started to increase. That means, less Indian rupee was being converted into dollars and because of the exports, more dollars were being converted into rupee, which helped in boosting the INR value. 

Well the major cause of fall in import value of because the crude oil prices dropped in the month of January 2019. And as crude oil being one of the highest imported goods(14% of total imports), drop in crude oil price affected the currency. 

That answers my question, this change in the prices of good affects the total cost of imports or exports and that, in turn, affects the currency value.


**Design Decisions:**

*Chart -1 :*

Idiom : Line chart <br>
Mark : Line <br>
Channels: The years on the y-axis are mapped using horizontal spatial position and the value of the INR is mapped using vertical spatial position. <br>

For my first chart where I wanted to see the trend of the INR rates from past few years, so I used line chart for showing the trend. For this chart we have a feature where we can zoom in to see the value for a particular month and zoom out to see as per year. 


*Chart -2 :*

Idiom : Grouped bar chart.<br>
Mark : Line <br>
Channels : The attributes exports, imports and INR is encoded using the color hue channel and vertical spatial position. <br>

The bars are grouped based on years. I wanted to see if there was any correlation between the atttributes and how they are changing over time. But it was difficult to see if there was any change at all for some attributes from the previous year. So I decided to modify this chart a bit and developed two other charts on the next page.


*Chart - 3 and 4:*

Idiom : Grouped bar chart. <br>
Mark: Line <br>
Channels : Years are encoded using color hue channel. The attributes exports, imports are INR are mapped using vertical spatial position. <br>

I have split the previous chart into two. The first one represents the exports and imports grouped according to years. and the second chart is showing the INr values. From these two charts aligned and placed side by side will allow us to see the change in exports, imports and INR. From the chart 4, we know that INr rised to it's highest value in the year 2018 and has been dropping from the begining of 2019 ( we can see this in chart 1 - line chart).

*Chart - 5:*

Idiom : Line chart. <br>
Mark : Line and point. <br>
Channels : The attributes exports and imports are mapped using horizontal spatial position and years mapped on vertical spatial position.The two attributes are color encoded, where blue is for imports and red is for exports.

In the final chart we can actually see the rise and fall in the export and import values. In the year when the INR rates were high that we saw in chart -1 , for the same year the import values were high as well. And the imports dropped in the year 2019 and exports increased. That strengthed the INR value. 


**Development Process:**

Roughly it took 5-7 days to finish the visualizations after collating all the data required for my project.
Grouped bar charts were complicated, until I found the reference code to look up. Next difficult part for me was to figure out what was wrong with my final chart, for some reason my years on x-axis has decimals. I parsed the date using d3.timeparse("%Y"), but it still didn't work, it was showing all 1969 on x-axis and that value was not even in my data. I was unable to figure it out.

Also, for the later part , I wanted to show how the prices of the exported goods and imported goods affect. But , I could only find data for the year 2017. there was no much info about the type of goods and their prices. So I couldn't plot them for my project.

**References:**

* https://blockbuilder.org/flacoman91/050cb74d729c97ae75139673222269f7
* https://www.investing.com/currencies/usd-inr-historical-data
* https://markets.businessinsider.com/commodities/oil-price
* https://markets.businessinsider.com/commodities/historical-prices/oil-price/usd/18.3.2010_16.3.2019?type=brent
* https://www.investopedia.com/articles/investing/100813/interesting-facts-about-imports-and-exports.asp
* https://www.ndtv.com/business/inr-usd-currency-exchange-march-22-2019-closing-rupee-weakens-against-us-dollar-rupee-vs-dollar-2011445
* https://blockbuilder.org/cse4qf/b4df62d5df6f47ece8f734e746d106ef


