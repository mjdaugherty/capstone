## Project Proposal: Grouping Galaxies by Spatial Coordinates

### Objective
Use publicly available data on several thousand galaxies to create a map of our cosmic neighborhood

### Methods and Models
- Collect data from the [NASA/IPAC Extragalactic Database (NED)](https://ned.ipac.caltech.edu/): for each galaxy in the New General Catalogue, collect declination and right ascension (angular coordinates, analogous to latitude and longitude) and redshift (can be used to estimate distance from Earth)
- Use DBSCAN to group the data points (galaxies) into clusters
- Easy problem: compare these clusters to real maps of galaxy distributions and evaluate the usefulness of unsupervised learning methods for learning about these and similar data
- Hard problem: make predictions on the future evolution of these clusters (will they collapse? disband?); this is probably impossible given computational constraints, but maybe predictions could be made using momentum or similar calculations

### Risks/Assumptions Associated with the Data
The New General Catalogue consists of 7841 astronomical objects, but not all of them are galaxies. In addition, the catalogue is more comprehensive for the northern sky than the southern sky, meaning that most of the galaxies in the catalogue are above 0<sup>°</sup>. Finally, some of the entries in the NED are missing redshift values. I believe that there will still be enough galaxies to create a useful model.

### Goals/Success Criteria
- Goal: use machine learning to create a representation of the distribution of galaxies that is both accurate and visually/intellectually appealing (interactive map?)
- Success metrics: silhouette score, comparison to real galactic clusters that are known to be gravitationally interacting