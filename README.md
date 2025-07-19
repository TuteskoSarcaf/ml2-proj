# ml2-proj

Unsupervised learning applied to astronomy

The purpose of this project is to demonstrate classification of stars by their stellar type using the https://www.kaggle.com/competitions/PLAsTiCC-2018/ dataset.
This data represents many stars and their measured brightness across multiple passbands (wavelengths). We'd like to classify a star based on its brigthness measurements.

Data is as described on the Kaggle page. We have measurements of brightness and passband information for objects (stars) based on their object IDs. We also have dates these measurements were made. Since stars generally have periodic brigthness curves, it is possible to compare these curves and do classification based on that.
However, since we do not know what the periods are for them, a simplification will be introduced - we will look at average, median, max, and min values for brightness across the several passbands we do have data for.

We therefore need to CLEAN this data first, and then TRANSFORM by calculating these values.
Another transformation is also to go from relative brightness (in Astronomy known as apparent magnitude) to absolute - we need to factor in the distances to stellar objects. This will make them comparable to each other.

Afterwards, we do unsupervised classification using KMeans clustering and compare to a supervised classif model.
We also explore Gaussian mixture and linear classification.
