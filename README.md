# cmd-labour-market-statistics

Transform takes 2 input csv files, one file name contains 'levels' and one contains 'rates' -> this is how the transform distinguishes the files. The input files are provided by the business area.

Place the input files in the same directory as the script or alternatively change the location variable in transform.ipynb to match the file location.

1 output file is created
- v4-lms.csv

The transform only runs with the most recent data, it then pulls the data of the previous publication from the CMD API and adds the most recent data to it. Warning messages from the requests module is normal as "verify=False" is being used when making a request which is required when running this transform on network.

The transform only requires use of base level packages.
