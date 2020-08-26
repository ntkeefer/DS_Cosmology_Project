# Data Science & Cosmology Project
By Kian Malone, Nicky Keefer, and Joey DiConza

### Table of Contents

show/hide:
<details>
  <summary>Click to expand!</summary>

* [Intro and Problem](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/README.md#introduction-and-problem)

* [Jupyter Notebooks](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/README.md#jupyter-notebooks)

* [Project Overview](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/README.md#project-overview)

* [Summary of Algorithm Performance](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/README.md#summary-table-of-algorithm-performance)

* [Data Overview](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/README.md#data-overview)

* [EDA & Regression](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/README.md#exploratory-data-analysis--ols-regression)

* [Regression Analysis](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/README.md#regression-analysis-part-i)

* [Clustering & Classification](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/README.md#predictive-modeling-and-analysis-part-ii--iii)

* [Conclusion](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/README.md#conclusion)

</details>

## Introduction and Problem

We are lovers of outer space. We follow SpaceX launches, we get excited about real pictures of black holes, and we love to argue over the time scale of the eventual heat death of the Universe. We had some questions. Are the distances between all large scale objects growing? Is the expansion between these objects accelerating? Normally, explosions start really fast and then slow down as they evolve through time. Could it really be possible that our Universe really contains evidence that big bang explosion started fast and is speeding up over time?? How could one make such an observation? We have an answer: Data Science and Machine Learning.


**[Hubble's Law:](https://en.wikipedia.org/wiki/Hubble%27s_law)**

<p align="center"> 
<img src="https://render.githubusercontent.com/render/math?math=v = H_{o}D"height="50" width="500">
</p>

Where <img src="https://render.githubusercontent.com/render/math?math=v"> is the [recessional velocity](https://en.wikipedia.org/wiki/Recessional_velocity) and <img src="https://render.githubusercontent.com/render/math?math=H_{o}"> is the Hubble constant and corresponds to H (the Hubble parameter and can be expressed as a [scale factor](https://en.wikipedia.org/wiki/Scale_factor_(cosmology))) in the Friedmann equations taken at the time of observation denoted by the subscript o.  <img src="https://render.githubusercontent.com/render/math?math=D"> is the proper distance from the galaxy to the observer in the typical 3-space coordinate system. As you can see, Hubble's Law is a simple linear equation where <img src="https://render.githubusercontent.com/render/math?math=D"> is the independent variable and <img src="https://render.githubusercontent.com/render/math?math=v"> is the dependent variable, yielding a slope of the line <img src="https://render.githubusercontent.com/render/math?math=H_{o}">.

**Ultimate Fate and Age of the Universe:** 

<p align="center"> 
<img src="https://render.githubusercontent.com/render/math?math=q = -(1 %2B \frac{\dot{H}}{H^{2}})"height="50" width="500">
</p>

Where <img src="https://render.githubusercontent.com/render/math?math=q"> is the [deceleration parameter](https://en.wikipedia.org/wiki/Deceleration_parameter) and its value, whether positive or negative, will yield a Big Crunch or Big Freeze (Heat Death) respectively. Current estimates lean toward the "Big Freeze" as <img src="https://render.githubusercontent.com/render/math?math=q"> is negative. <img src="https://render.githubusercontent.com/render/math?math=\dot{H}"> is the first time derivative of the Hubble Parameter.

Images of SpaceX, Black Hole, and Big Bang Timeline:
<details>
  <summary>Click to show!</summary>
  
SpaceX Starship [(Link)](https://cdn.mos.cms.futurecdn.net/J2NTP9Er4Ad3kRsms7XRoD.jpeg) | Real Image of Black Hole [(Link)](https://www.jpl.nasa.gov/images/universe/20190410/blackhole20190410.jpg)
----------------------------------------------------------------------------------------|--------------------------
![J2NTP9Er4Ad3kRsms7XRoD-1024-80](https://user-images.githubusercontent.com/42389358/89854478-38343180-db51-11ea-9b5a-ec811eeaae15.jpeg) | ![blackhole20190410](https://user-images.githubusercontent.com/42389358/89842671-9b16d000-db33-11ea-98a7-9928f9164e0b.jpg) 

Expansion of the Universe [(Link)](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6f/CMB_Timeline300_no_WMAP.jpg/2560px-CMB_Timeline300_no_WMAP.jpg) |
-----------------------------------------------------------------------------------------------------------------------------------------------------------|
![2560px-CMB_Timeline300_no_WMAP](https://user-images.githubusercontent.com/42389358/89842665-96eab280-db33-11ea-9aff-1c8bb8f75746.jpg) 

</details>


## Jupyter Notebooks

* [Data_Cleaning.ipynb](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/Data_Cleaning.ipynb) (Initial data preparation)

* [EDA_Regression.ipynb](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/EDA_Regression.ipynb) (EDA and Part I: Regression)

* [Models.ipynb](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/Models.ipynb) (Part II & III: Clustering and Classification)



## Project Overview

1. Regression: 
  In our project, we first set out to answer just how fast the universe is expanding. We called this *Part I* of our project in our meetings with each other. We plotted velocity     against distance, and created a regression line for each of our data sets. The slope of this line is what is called the "Hubble Constant", <img              src="https://latex.codecogs.com/svg.latex?\Large&space;H_{o}" title="H_{o}" /> which describes the increase in the rate of expansion of the universe as you get farther and         farther away.
  Will our calculation of the Hubble Constant get us close to the the gravitational wave calculation performed by modern physicists? We hope so. We decided we would be happy if     our caluclation was within an order of magnitude of the modern calculation of 68-72 km/s*\mpc and Edwin Hubble's first estimates were around 55 km/s*\mpc.


2. Clustering:
For *Part II*, we reasoned that we had enough data to create a clustering model to allow a computer to distinguish "red" galaxies from "green"/ "blue" galaxies. You can read more about this on [Wikipedia](https://en.wikipedia.org/wiki/Galaxy_color%E2%80%93magnitude_diagram)

3. Classifier:
For *Part III*, we created a classifier to determine whether an astronomical object is a Quasar, or just a normal galaxy. For a fascinating description of what a Quasar is, check out [PBS Space Time's video](https://www.youtube.com/watch?v=3TZEp_n3eIc)

## Algorithms for Part II and III:
We tested two different models for each task. For clustering, we chose to use a K-Means model and a DBSCAN model. For classifying, we used a Support Vector Machine and a K-Nearest Neighbors classifier. We wanted two different methods for each task in order to gauge the relative strength of each method.

## Summary table of model performance

|Regression: log(distance) vs. velocity | Classification |
|:-------------------------------------:|:--------------:|
|<img src="https://latex.codecogs.com/svg.latex?\Large&space;R^{2} = 0.856" title="R^{2} = 0.856" />|<img src="https://latex.codecogs.com/svg.latex?\Large&space;R^{2} = 0.856" title="R^{2} = 0.856" />|



## Data Overview
show/hide:
<details>
  <summary>Click to expand!</summary>
  
We acquired our raw data from the SLOAN DIGITAL SKY SURVEY (SDSS). At the SDSS website, they have a built-in SQL Query Request Tool. While this did make our life much easier, there were basic query limits of 500,000 rows and 10 minute time-out, thus we had to optimize our SQL queries in order to sumbit the following request to the SDSS database:

**SQL Query:**
```
SELECT s.class
,s.z
,s.zErr
,p.modelMag_g
,p.modelMagErr_g
,p.extinction_g
,p.modelMag_r
,p.modelMagErr_r
,p.extinction_r
FROM PhotoTag AS p 
JOIN SpecObj AS s ON s.bestobjid = p.objID
WHERE s.zWarning=0 AND (s.class = 'QSO' OR s.class = 'GALAXY') AND (p.htmID*37 & 0x000000000000FFFF) < (650 * 0.5)
```

What this did was select a random sample of .005% of the SDSS data's on galaxies and quasars. By changing the "37" after p.htmID to another prime number, the query reselects a new random sampling of the same size. By changing the "0.5" after the 650, the query selects a different proportion of the complete database (i.e. 0.75 will yield .0075 rather than .005% of the data).

We grabbed the columns representing the apparent magnitude in the green and red band, as well as the redshift (to find redshift velocity <img src="https://render.githubusercontent.com/render/math?math=v_{rs}">) for these objects, and all of their associated errors. Along with these we also pulled the extinction in the red band just in case we have a large deviation from the expected result, we can add extra correction factors to see if anything changes. Due to the sampling being random, and since our sample size is large, we can infer better estimates about the Universe as a whole from this data set. In turn, satisfy our intitial goal for the project.

**Redshift Velocity:**

<p align="center">  
<img src="https://render.githubusercontent.com/render/math?math=v_{rs} = cz"height="20" width="200">  
</p>

While variables from two seperate SDSS tables were needed, we were able to join everything into a single table using the JOIN function and a common object id to match up the data before we ran our query. We also made certain that no entries have "NA" values in any column using zwarning=0, a binary column in the SpecObj table that makes sure we are pulling data that has no issues or missing values throughout, this matches up with objects that are also clean in the other table, helping us cut down on our data clean up even before we pulled it!

Note that this process was largely trial-and-error, since the SDSS database is hundreds of terrabytes in depth, we needed our query to be precisely targeted and maximize efficiency so that it wouldn't take hours to return one dataset (we needed 40 sets, and the query times out after 10 minutes).

In fact, the original data that we pulled ended up being identical within each size bracket, but with the indexes rearranged (i.e. all datasets of size 7k were identical to each other, all of size 14k were identical to each other, etc...). We had to go back to the drawing board to fix it mid-analysis.

After we obtained the raw data, we had to clean the numbers. We converted almost all columns to a float, since they mostly came in as strings. We also renamed each column to make it easier to work with. Much of what you might consider "data cleaning" also occured after exploring the data, and will be discussed in our "Exploratory Data Analysis" section.

Once we were happy with this, we were ready to create some data frames for our initial analysis. We included the inital pulled data in the file [roughdata](https://github.com/ntkeefer/DS_Cosmology_Project/tree/master/roughdata) and the final cleaned data in the file [cleandata](https://github.com/ntkeefer/DS_Cosmology_Project/tree/master/cleandata). We also included the data cleaning process in the note book file [Data_Cleaning.ipynb](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/Data_Cleaning.ipynb)
</details>

## Exploratory Data Analysis & OLS Regression
show/hide:
<details>
  <summary>Click to expand!</summary>


The goals of the EDA that we ran were as follows:

- Describe the distribution of each variable in our datasets, including searching for the presence of outliers.
- Calculate the velocity, flux, and distance for each astronomical object. Please see [Sketch_Analysis_Equations](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/Sketch_Analysis_Equations.ipynb) for more details.
- Obtain an estimate for the Hubble Constant <img src="https://render.githubusercontent.com/render/math?math=H_{o}">, the rate of expansion of the universe.
- Determine whether increased amounts of data leads to more accurate results in order to decide if error comes from lack of complete data or problems in methodology.

By looking at the output of sns.pairplot on our data, we were able to discover that each variable behaves reasonably close to the way we expected them to (from our prior knowledge of physics). There are more objects in our data that are close to us than far away. Magnitudes for each band of light usually fall into two bunches: one for galaxies and one for quasars, as expected.

<p align="center"> 
  
![SnsPairPlot](https://user-images.githubusercontent.com/42389358/90968306-00f64680-e4a8-11ea-909b-d98d71e7c168.png)

</p>

We also were able to identify the presence of several outliers in our data, which we later dealt with by cutting off values that fell outside of specific ranges for each variable.

The most important discovery was that Quasars are extremely erratic. The values for their magnitudes and redshifts are often point clouds or fan out to extreme values. We decided that for the purposes of caluclating the Hubble Constant, we would leave quasars out. Indeed, when we ran regressions on "velocity~distance" for quasars, the average R Squared value was .08, which means only 8% of the variance between velocity and distance is explained by that linear model. That result is not nearly satisfactory when we expected to see a near-perfect line there.


Another important discovery was that the magnitude of the green band had a closer relationship with velocity than the magnitude of the red band. We changed our original plans to use the green band in our distance calculations for this reason.
</details>

## Regression Analysis (Part I):

show/hide:
<details>
  <summary>Click to expand!</summary>

We completed the calculations for velocity, flux, and distance after observing that the trends in our data are reasonably close to our expectations. You can see how these columns are calculated by referencing [Sketch_Analysis_Equations](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/Sketch_Analysis_Equations.ipynb).

Upon inspection, we discovered that the relationship between distance and velocity was not linear, as we had expected, but logarithmic. After putting our heads together, we reasoned that this comes from our "standard candle" assumption for luminosity! Since these luminosity values typically vary in a logarithmic fashion, we introduce a logarithmic error when we assume them to "average out" to a flat value.

<p align="center"> 

![DistVeloGalaxy2](https://user-images.githubusercontent.com/42389358/90968301-fe93ec80-e4a7-11ea-948f-7aff4f8727f5.jpg)

</p>

In order to combat this, we decided to regress on the log of distance, rather than just distance, in order to calculate the Hubble Parameter. This indeed achieved a more precise result, with R-Squared values trending from about .7 to .85 after making this correction.

<p align="center"> 

<img width="542" alt="OLS Log of distance" src="https://user-images.githubusercontent.com/42389358/90968304-005db000-e4a8-11ea-855a-4d7b4a5d6a78.png">

</p>

Finally, after running all of our data through linear regressions for "velocity ~ distance", and after weighting each result appropriately for the size of each dataset, we obtained an expetimental value for the Hubble Parameter of 43.57285 km/sMpc. We are pleased with this result, as it is well within an order of magnitude of the "actual" value of roughly 68-72 determined by modern physicists.

It is important to note that increasing the size of the dataset from 7k, to 14k, then 21k and 28k neither increased R-Squared nor improved the accuracy of our Hubble Parameter. We conclude that the reason we aren't getting 72 as our value isn't because of incomplete data, but rather problems with methodology.

You can reference [EDA_Regression.ipynb](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/EDA_Regression.ipynb) to see this in action. We simplified many of the original "for" loops that processed all of our data down to single examples for ease of readability and processing speed.

</details>

## Predictive Modeling and Analysis (Part II & III):
show/hide:
<details>
  <summary>Click to expand!</summary>


Check out our models in [Models.ipynb](https://github.com/ntkeefer/DS_Cosmology_Project/blob/master/Models.ipynb)

In this notebook, we included only our final models, with the highest scores for their relevant metrics. To choose parameters for these models, we underwent an intensive looping process that usually had to run overnight in order to run models for hundreds of possible parameter combinations. We plotted these results and selected appropriate parameters this way.

On the first night of looping, the desktop we were running calculations on shut itself down before completing the loop and achieving the desired result. After modifying some settings and pulling the computer itself to a more open area to prevent overheating, the next day the loop ran as expected. You might need to take similar measures if you plan on running some of these models yourself!

For Part II, the star performer of our models was the k-Means clustering model. If you compare its plot to the graph on the wikipedia page for the galaxy color-magnitude diagram, you will see a close resemblence. We had the advantage of knowing that our data should contain 3 clusters: one red, one green, and one blue. Because of this, the choice for k=3 was obvious and lead to seemingly perfect results. Check out the notebook to see this!

<p align="center"> 
  
![KmeansGalaxyColorMagDiagram](https://user-images.githubusercontent.com/42389358/90968302-ff2c8300-e4a7-11ea-9c7d-7decbd03618c.png)

</p>



The DBSCAN model performed poorly on our dataset. When cross-validated between the datasets, the model was rarely able to pick out three distinct color clumps. Often the whole dataset would be one cluster, or the model would distinguish only the main group of galaxies from those with extreme values. We believe that this is due to our data being somewhat "smudged together," with no cluster being completely seperate from another. We suspect that the epsilon value required to detect the appropriate clusters with a DBSCAN model is probably so precise that our discrete "for" loops can't locate it.

<p align="center"> 
  
![DBSCANGalaxyColorMagDiagram](https://user-images.githubusercontent.com/42389358/90968300-fb98fc00-e4a7-11ea-97a3-f5538c133821.png)

</p>


For Part III, we referenced the results of our EDA to include redshift, green apparent magnitude, red apparent magnitude, and absolute magnitude in our models.

Our final support vector machine (SVM) model was able to correctly classify an object as a galaxy or quasar 98.3% of the time on test sets! Despite the data being sort of "mixed together" within the green valley of the color-magnitude diagram, the SVM classifier was still able to correctly determine whether the object was a quasar or a galaxy 98% of the time. Our k-Nearest Neighbors model performed almost as well, with an average 98.2% success rate among the test sets.

<p align="center">
  
![SVMGalaxyColorMagDiagram](https://user-images.githubusercontent.com/42389358/90968307-02277380-e4a8-11ea-8940-a38c5bfd5749.png)

</p>

<p align="center"> 
  
![KNNGalaxyColorMagDiagram](https://user-images.githubusercontent.com/42389358/90968303-ffc51980-e4a7-11ea-84a5-7e6fc4bd90a7.png)

</p>

</details>

## Conclusion
show/hide:
<details>
  <summary>Click to expand!</summary>


Our project had great results.

In Part I, our Hubble Parameter met our goal for accuracy, being well within an order of magnitude of the modern calculation. In fact, the original prediction made by Edwin Hubble for this parameter was about 55, which we are quite close to at 43.6.

In Part II, we were able to obtain a great model to cluster objects around their appropriate color, with results closely following what a human would decide.

In Part III, our models were able to achieve an accuracy rate of 98.3% for correctly classifying an obect as a galaxy or a quasar.

If we redesigned this project, we would include a method to more accurately determine the luminosity and flux using outside data in order to avoid introducing error into our data!

We might also attempt find labels for "red" vs "green" vs "blue" galaxies. Since DBSCAN clustering didn't perform well, it would have been great to be able to build a classifier to perform this task and compare the results of classifiers vs. clustering!

Key Takeaways

Machine learning and other data science techniques can closely mirror results obtained through classical methods in physics, though not to the same degree of accuracy.

There is a limit where acquiring more data contributes less to obtaining accurate results than an appropriate change in methodology would, as seen by our error being consistent among our values for the Hubble Parameter among datasets of varying size.

It is important to choose the right model for the right data. Our K-means model was excellent for our data, but DBSCAN was horrible!

computed foundational astrophysical findings using modern data science techniques. The first steps of our project utilized a linear regression on large data sets to estimate the Hubble parameter, a measure of the expansion of the universe. After this value was established, we implemented machine learning algorithms to classify populations of blue and red galaxies and separate active quasars from galaxies. For a summary of our findings and analysis, review Final_Notebook.ipnyb. 
</details>

Notes:

show/hide:
<details>
  <summary>Click to expand!</summary>
</details>
