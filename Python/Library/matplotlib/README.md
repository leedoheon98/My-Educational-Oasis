# Matplotlib

Matplotlib is a powerful Python library for creating static, animated, and interactive visualizations. It is widely used for plotting various types of graphs such as line plots, bar plots, histograms, and scatter plots.

### Frequently Used Methods

- `plt.plot(*x*, *y*, *format*)`: Plots *x* versus *y* with specified format.
- `plt.bar(*x*, *height*, *width*, *color*)`: Creates a bar chart with specified bars' heights and widths.
- `plt.hist(*data*, *bins*, *color*)`: Generates a histogram from given data with specified number of bins.
- `plt.scatter(*x*, *y*, *s=*, *c=*, *marker=*)`: Creates a scatter plot with specified marker size and color.
- `plt.xlabel(*label*)`, `plt.ylabel(*label*)`: Sets labels for x-axis and y-axis, respectively.
- `plt.title(*title*)`: Sets the title for the plot.
- `plt.legend(*loc=*)`: Places a legend on the plot.
- `plt.savefig(*filename*)`: Saves the current figure to a file.
- `plt.subplot(*nrows*, *ncols*, *index*)`: Adds a subplot to the current figure.
- `plt.colorbar(*mappable*)`: Adds a colorbar to a plot.

### Frequently Used Commands

- `import matplotlib.pyplot as plt`: Importing Matplotlib's pyplot module.
- `plt.show()`: Displays the plot.
- `plt.style.use(*style*)`: Sets the plotting style.
- `plt.grid(*bool*, *which='major'*)`: Turns grid on or off for major or minor ticks.
- `plt.figure(*figsize=*)`: Creates a new figure with specified size.
- `plt.tight_layout()`: Adjusts subplot parameters to fit the figure area.
- `plt.annotate(*text*, *xy=*, *xytext=*, *arrowprops=*)`: Annotates a point on the plot with text and optional arrow.
- `plt.contour(*X*, *Y*, *Z*, *levels=*)`: Plots contour lines.
