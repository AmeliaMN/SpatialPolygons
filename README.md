# How Spatial Polygons Shape Our World
## Amelia McNamara, OpenVisConf 2017

This repo contains a PDF version of the slides for my 2017 OpenVisConf talk, How Spatial Polygons Shape Our World. The video of me giving the talk is [available on youtube](https://www.youtube.com/watch?v=wn5larsRHro), and the full transcript is available [on the conference website](https://openvisconf.com/files/transcripts/OpenVis_Amelia_McNamara.txt).

### References and links:

#### All maps are wrong:
- Choropleth map example, [Prop 1 election results](https://www.flickr.com/photos/viriyincy/13988403042/in/photolist-nj7dSN-7m2b-5zw5MQ-8UCreo-axnnhd-an24ax-9EfLhX-fAaYES-7rnv-iGuuTo-iGtTGR-iGvtUs-edPtj8-482zRm-hXL359-Ew8CM3-9F6L4C-drZNsk-9kzFYA-nEhkKH-7Wp2Rk-drdZCY-93V7Tf-nNtgXA-yB85qM-dtahrN-zguDMT-zwVDzb-5VZdKf-zvGoTy-5wKw7m-5BfZdA-y621-rRsi4-2DvmA-5zrNhR-jgpED-9FEhvg-8waRV-5zw5L7-oRDEcs-dhgAuh-7Yeuhj-7YewZ3-9EWQ3h-7FMbCj-5zkEBN-5zksaj-5EfFs9-4qyp68).
- [All maps of parameter estimates are misleading](http://bit.ly/AllMaps), paper by Andrew Gelman and Phillip Price.
- An illustration of the issue of mapping parameter estimates: [Avoiding Data Pitfalls, Part 2: Fooled by Small Samples](http://dataremixed.com/2015/01/avoiding-data-pitfalls-part-2/) (Kidney cancer rates by county).
- A solution to the issue of mapping parameter estimates: [Surprise! Bayesian Weighting for De-Biasing Thematic Maps](http://bit.ly/SurpriseMaps), Michael Correll and Jeff Heer.
- The standard presidential election map: [2008 Presidential election map](http://www.nytimes.com/elections/2008/results/president/map.html).
- One way to avoid being fooled by large areas with few people is to make a cartogram. [2004 Presidential election cartogram](https://commons.wikimedia.org/w/index.php?curid=10523106).
- [Square and hexagon cartograms](http://blog.apps.npr.org/2015/05/11/hex-tile-maps.html) are another way to avoid being fooled by area.
- If you're making cartograms, you might care [Whose map is better? Quality metrics for grid map layouts](https://medium.com/@kristw/whose-grid-map-is-better-quality-metrics-for-grid-map-layouts-e3d6075d9e80).
- [Evaluating cartogram effectiveness](https://arxiv.org/pdf/1504.02218.pdf) is another resource.

#### Combining incompatible data
- With rectangular data, you could use the [RStudio data wrangling cheatsheet](https://www.rstudio.com/resources/cheatsheets/) to join two types of data. With "incompatible spatial units" this doesn't work.
- The [Modifiable Areal Unit Problem](http://gispopsci.org/maup/) is the problem that aggregating point data to different polygons can have huge effects on the visual distribution. 
- It shouldn't surprise us that this happens. Check out the [histogram essay](http://tinlizzie.org/histograms/) I've been working on with a collaborator to see this in a one-dimensional case.

#### Gerrymandering
- In the context of elections, we call the MAUP [Gerrymandering](https://commons.wikimedia.org/w/index.php?curid=6030613).
- John Oliver on Last Week Tonight [explains gerrymandering](http://bit.ly/LWT_gerrymandering) in a much funnier way than I could.
- A commonly-cited Washington Post article, ["The best explanation of gerrymandering you will ever see"](https://www.washingtonpost.com/news/wonk/wp/2015/03/01/this-is-the-best-explanation-of-gerrymandering-you-will-ever-see).
- For a more realistic experience, try the [Redistricting Game](http://redistrictinggame.org/).

#### Downscaling, upscaling, sidescaling
- [Disser](http://conveyal.com/blog/2014/04/08/aggregate-disser) could help you move from aggregated data to point data.
- Jon Kimerling has thoughts on [Dotting the dot map, revisited](http://downloads2.esri.com/MappingCenter2007/resources/presentations/Kimerling_2008_UR_Colloquium.pdf) .
- Another project with my collaborator: [Spatial aggregation explorer](http://www.bit.ly/spatial_agg).
- In the electoral context, you might want to [Redraw the States](http://kevinhayeswilson.com/redraw/) by moving counties from one state to another.
- [How zip codes almost masked the lead problem in Flint](http://theconversation.com/how-zip-codes-nearly-masked-the-lead-problem-in-flint-65626).
- The [pycno package](https://cran.r-project.org/web/packages/pycno/index.html) in R to perform pycnophylactic interpolation. 
- In javascript, [cogran.js](https://github.com/berlinermorgenpost/cogran) will let you combine data of different spatial granularities. 



### Thanks to:
- [Pierre Goovaerts](https://sites.google.com/site/goovaertspierre/), whose talk on geostatistics in practice at UCLA in 2014 started me thinking about the change of support problem.
- [Friedrich Hartmann](https://twitter.com/mxfh), who introduced me to dasymetric mapping and the MAUP at IEEEVis in 2014 and pointed me toward cogran.js right before my talk.
- [Moon Duchin](http://www.chronicle.com/article/Meet-the-Math-Professor/239260), one of the mathematicians solving gerrymandering.
- [Richard Casey Sadler](https://chmfamilymedicine.msu.edu/directory/rick-sadler-phd), who works on public health problems in Michigan.
- [Matt Brehmer](https://twitter.com/mattbrehmer) who sent me references to cartogram effectiveness measures.
