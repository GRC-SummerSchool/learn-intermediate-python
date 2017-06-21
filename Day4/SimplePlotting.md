|[< Previous (File I/O) >](CSVFiles.md) | [Day4](../README.md)|  [Next (Extra - Data Analysis)](../Extra/DataAnalysis.md) |
|----|----|----|


# Simple Plotting

Now that we have loaded the weather data, let's create a few plots. There are many plotting packages available.
Here we are going to use the [matplotlib](https://matplotlib.org/) package to create some plots.


## Using matplotlib

Before we can use the matplotlib library, we must import it
```python
import matplotlib.pyplot as plt
```

## Simple X, Y Plot

To create an X, Y plot, the arrays of the X and Y values are simply passed to the ```plot()``` function.
Below we define a function called ```plot_tavg``` which takes the 2 arguments which are the X and Y arrays passed to the ```plot``` function

```python
def plot_tavg(array_YEARMONTH, array_TAVG):
    plt.plot(array_YEARMONTH, array_TAVG)
    plt.title('Average Temperature')
    plt.show()
```

The ```matplotlib.pyplot``` library contains many [functions](https://matplotlib.org/2.0.2/api/pyplot_summary.html) for plotting different kinds of
plots (line, bar, contours) and for styling the plots with a title or different colors. In the example, we create a simple line plot and provide a title. If desired, you can pass addtional options to the ```plot``
function to specify maerks rather than lines, as well as the styke and color of the lines or markers.

Finally, the ```show()``` function is called to display the resulting plot (shown below).

![](.SimplePlotting_images/ec4101b5.png)

Before calling the ```plot_tavg``` function, the data from the map must be placed into arrays. This little function will loop through our dictionary and pull out data from a particular attribute.

```python
# Extract attribute from dictionary as an array
def create_attribute_array (data, attribute):
    a = []
    for x in data:
        a.append( x[attribute] )
    return a
```

### Exercise

Add the import statement to the top of your readweather.py file.
Add the plot_tavg function to the file.
Add the create_attribute_array function to the file.
Update your main section to
1) Select one of the divisions from the data map.
2) Create attribute array objects for the YearMonth attribute and the TAVG attribute.
3) Call the plot_tavg function with the YearMonth as first input and TAVG as second.

The plot shown above is for division 10.

## Multiple sub-plots

Often it is useful to plot several plots together. Below two subplots are created, one for Average Temperture and another for Precipitation.

```python
def plot_division (division_data):

    array__DIVISION = create_attribute_array(division_data, 'Division')
    array_YEARMONTH = create_attribute_array(division_data, 'YearMonth')
    array_TAVG = create_attribute_array(division_data, 'TAVG')
    array_PCP = create_attribute_array(division_data, 'PCP')

    plt.subplot(2, 1, 1)
    plt.plot(array_YEARMONTH, array_TAVG, 'ko-')
    plt.title('Division ' + str(array__DIVISION[0]))
    plt.ylabel('TAVG (F)')

    plt.subplot(2, 1, 2)
    plt.plot(array_YEARMONTH, array_PCP, 'r.-')
    plt.xlabel('array_YEARMONTH')
    plt.ylabel('PCP')

    plt.show()
```

![](.SimplePlotting_images/52bf7c6c.png)

### Exercise

Add the plot_division function to the file.
Update your main section to call the plot_division function instead of create_attribute_array and plot_tavg.


### Exercise

Modify your program to plot your data in Celsius units instead of Fahrenheit.

|[< Previous (File I/O) >](CSVFiles.md) | [Day4](../README.md)|  [Next (Extra - Data Analysis)](../Extra/DataAnalysis.md) |
|----|----|----|