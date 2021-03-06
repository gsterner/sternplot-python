# PyStPlot
A VERY basic plotting tool for python that creates plots to be viewed in the web broser.
Creates an html file containing the plot drawn with html canvas.

## Install with pip
```
pip install pystplot
```
## Usage
To plot a function, simply assign x and y values to two lists and call `pystplot.plot(...)`.
Call either the `pystplot.show()` to create an output file and show it in the browser or `pystplot.save(...)` to just save the html file.

## Example
```python
import pystplot as pl

x_values = range(-10,11)
y_values = [x*x for x in x_values]
pl.plot(x_values, y_values)

pl.show()
```

## Functions
#### Plot
```python
plot(x_list, y_list, property_string='-')
```
Creates the plot data.

```
Parameters:
        
x_list             list of values for x-axis
y_list             list of values for y-axis. Lists must be of same length
property_string    sets appearence of graph. Possible choices:
                   'o'   points
                   '-'   line
                   'r'   red
                   'b'   blue
                   'g'   green
                   'y'   yellow
                   'm'   magenta
                   'c'   cyan
                   'w'   white
                   'k'   black         
```

#### Show
```python
show()
```
Saves an html-file called "pystplot_output.html" that constains the plot and opens it in the default web browser.

#### Save
```python
save(file_name=PLOT_FILE)
```
Saves an html-file with file name given as parameter. If no name is given the default "pystplot_output" is used.

```
Parameter:

file_name    string that contains file name of output html-file.
```

#### Subplot
```python
subplot(rows, cols, index)
```

Creates a matrix of plots in a Matlab/Matplotlib manner. Call ```subplot(rows, cols, index)``` before ```plot(x_list, y_list, property_string='-')
``` to tag the plot.

```
Parameters:
    
rows    number of rows in plot matrix
cols    number of columns in plot matrix
index   index of this specific plot - indexed from left to right.
```