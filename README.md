# Maps with labels

This is a simple map generator which allows for placement of multiple
makers (e.g. to indicate participants in scientific or other 
collaborations) with custom placement of labels and marker type and size.  
Although Google Maps (for example) allow for very easy placement of markers,
it doesn't allow for easy customization of symbols and/or labels.

The core part is a Jupyter notebook (Map-Institutions.ipynb) along
with some example data files (institutions-list.csv).

# Required Environment

Several python modules are required. See environment.yml for a list.

If you use Conda (e.g. see the Individual Edition from [Anaconda](https://www.anaconda.com/products/individual), you can create the right python environment to start the notebook with the right modules with the included environment.yml
file and this command:

conda env create -f environment. yml

followed by:

conda activate maps

# Customizing the data file


