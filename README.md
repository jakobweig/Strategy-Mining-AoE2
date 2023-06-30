# Seminar Strategy Mining
Jakob Weigand: 2823303

## Structure of the Code
There are 3 Notebooks. The first Notebook is ‘Data preparation’ in which the data gets examined and prepared. The second notebook ‘K-Means’ in which different strategies are analyzed and in the last notebook ‘DBSCAN’ is similar to the K-Means code and for a comparison between these two methods.

## Data preparation
The first part of the code reads in the files and creates several new columns for the later analyses. Three Boxplotes, displaying the time, elo and APM distribution give a first insight to the dataset. Next follows are Timefilter cell in which one can uncomment one of the line to filter the data respectivly for actions that happend only before the specified timestamp.

In the next part gets the dataframe divided into 4 parts which only includes the Actions of recrtuiting Units, building buildings or researching technologies and one dataframe with all the data. 
After this step is done, the actions are counted and trasnformed to numbers. Now does every dataframe contains the counts how often each player did one of the actions which are displayed in the columns.
For a better understanding of the results are the features summarized to more general terms. For example all buildings like 'farm', 'mill', 'lumber camp' get summarized do the feature 'economic building'.

After this is done the final daframes are saved.

## Machine Learning

The prepared dataframes from the first notebooks are loaded and the function 'cluster_function' is called with every dataframe which calculates the K-Means and the feature importance of every cluster of every dataframe. The feature importance gets displayed as one graph each.

The next two cells calculate the win rate of each of the clusters in order give an underatnding on how successfull the different strategies are.

The last code snippets visualize the the different dataframes with PCA, 3D PCA and the t-SNE method.

## DBSCSAN Notebook
The DBSAN notebook is only a short exploration on how good the clustering with DBSCAN works in comparison with k-Means. 

The notebook begins with reading the prepared data from the main ‘Strategy mining’ notebook. 
Directly after is the DBSCAN method applied as well as the different visualization methods PCA, 3D PCA and t-SNE like in the other notebook.

