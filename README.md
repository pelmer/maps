# Maps with labels

This is a simple map generator which allows for placement of multiple
markers (e.g. to indicate participants in scientific or other 
collaborations) with custom placement (size, font) of the corresponding
labels. Although Google Maps (for example) allow for very easy placement of 
markers, it doesn't allow for easy customization of symbols and/or labels.
This map generator provides a bit more flexibility.

The core is a Jupyter notebook (Map-Institutions.ipynb) along with some 
example data files in csv format (master-list.csv, etc.).

# Required Environment

Several python modules are required. See environment.yml for a list.

If you use Conda (e.g. see the Individual Edition from [Anaconda](https://www.anaconda.com/products/individual), you can create the right python environment to start the notebook with the right modules with the included environment.yml
file and this command:

conda env create -f environment. yml

followed by:

conda activate maps

# Customizing the data file

A number of data files are included:

  * master-list.csv - a full list of a bunch of places
  * example-collaboration.csv - an example large collaboration
  * iris-hep.csv - funded institutions for IRIS-HEP (https://iris-hep.org)
  * clariphy.csv - collaboratin institutions for CLARIPHY (https://clariphy.org)

Note that there are also examples in the notebook (and corresponding data
files) for plotting two or three types of lists of institutions. Additional
(commented) options show how to change the extent of the map (e.g. regions in
the US or including Puerto Rico)

The data files contain lines of the form:

NameLine1,NameLine2,LatVal,NorS,LongVal,LabelLatOffset,LabelLongOffset

For example:

Princeton,,40.3431,N,74.6551,W,-0.65,1.4

The NameLine1 and NameLine2 allow for more than one line in the label.
Typically for short institution names only NameLine1 is needed.

The offsets for the label are in units of latitude and longitude,
e.g. "-0.7,0.0" will usually put the label just below the point and
"0.3,0.0" will usually put the label just above the point.
Note that a "West" longitude is treated as negative (-74.6551) and the
chosen offset should reflect that. Similarly "North" is positive. You
can get the latitude and longitude from any source you like (googling
'latitude longitude Princeton University' will return the values above,
for example).

# Questions or contributions

If you have questions, please file a github issue. Contributions (e.g.
additions to the master list) are welcome via pull requests.
