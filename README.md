# ekmeans
K-means algorithm with optional equal cardinality constraint (Pierre David Belanger: https://github.com/pierredavidbelanger/ekmeans) modified and ported to MATLAB.

Input is a matrix where columns are dimensions and rows are data-points.

Outputs are cluster assignments for each data-point and the centroid co-ordinate of each cluster.

Random centroids are seeded in the data and data points are assigned to these centroids on the basis of their euclidian distance. Assignments and centroid positions are iteratively updated. If equal cardinality is specified, whenever a cluster becomes too large points in that cluster that are closest to any other centroid are removed and reassigned to their next closest centroid and all clusters/centroids updated.

# ekmeans GUI
GUI to view, evaluate and optimise cluster assignments. Can plot in up to 3 dimensions. GUI stores up to 10 cluster splits in memory and user can cycle through/replace clusters with GUI buttons.

Inputs:
- .csv/.txt: matrix where columns are dimensions and rows are data-points.
- .mat: where first variable is matrix where columns are dimensions and rows are data-points.
- .tiff: all pixels are 0 except data-point pixels which are > 0
- matrix: all values are 0 except data-points which are > 0

Input can be provided as workspace variables or selected in file-selection GUI.

Input can be provided as a workspace variable or not provided (select in file-section GUI).

# Plot clusters
Scatterplots 2D/3D clusters, connected by lines to their respective centroids and applies an arbitrary colourcode to aid visualisation.
