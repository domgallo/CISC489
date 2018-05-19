# How our results can be reproduced

## Importing Data

The data that we used is in a file called 'All UV Data.csv'. When you run this line of code:
```
from google.colab import files
uploaded = files.upload()
```
a box with "Choose Files..." will pop up underneath and you click on that to select whichever data file you would like to use. 
If you use your own file, then in this line of code:
```
df = pd.read_csv(StringIO(uploaded['All UV Data.csv']))
```
you would need to replace 'All UV Data.csv' with the name of your data file.

```
x = df['Date']
y = df['ClearSkyUVI']
```
In the above two lines of code, we set the array x to the values in the column labeled Date in the csv file, and we set the
array y to the values in the column labeled ClearSkyUVI. These can be changed to fit your individual data if necessary.
