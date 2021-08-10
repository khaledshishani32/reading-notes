# Data Visualization
---
# Matplotlib

#### Matplotlib is probably the most used Python package for 2D-graphics. It provides both a quick way to visualize data from Python and publication-quality figures in many formats. We are going to explore matplotlib in interactive mode covering most common cases.

---
# pyplot

#### pyplot is a collection of functions that make matplotlib work like MATLAB. Each pyplot function makes some change to a figure: e.g., creates a figure, creates a plotting area in a figure, plots some lines in a plotting area, decorates the plot with labels
---
# How to Set X-Limit (xlim) in Matplotlib

#### using both the PyPlot and Axes instances. Both of these methods accept a tuple - the left and right limits. So, for example, if we wanted to truncate the view to only show the data in the range of 25-50 on the X-axis, we'd use xlim([25, 50]):

#### fig, ax = plt.subplots(figsize=(12, 6))

#### x = np.arange(0, 10, 0.1)
#### y = np.sin(x)
#### z = np.cos(x)

#### ax.plot(y, color='blue', label='Sine wave')
#### ax.plot(z, color='black', label='Cosine wave')

#### plt.xlim([25, 50])
#### plt.show()

![](https://stackabuse.s3.amazonaws.com/media/how-to-set-axis-range-xlim-ylim-in-matplotlib-2.png)

---

# Animation
#### For quite a long time, animation in matplotlib was not an easy task and was done mainly through clever hacks. However, things have started to change since version 1.1 and the introduction of tools for creating animation very intuitively, with the possibility to save them in all kind of formats (but don't expect to be able to run very complex animations at 60 fps though).

---

# Axes
#### Axes are very similar to subplots but allow placement of plots at any location in the figure. So if we want to put a smaller plot inside a bigger one we do so with axes.

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/axes.png)

---
# Ticks
#### Well formatted ticks are an important part of publishing-ready figures. Matplotlib provides a totally configurable system for ticks. There are tick locators to specify where ticks should appear and tick formatters to give ticks the appearance you want. Major and minor ticks can be located and formatted independently from each other. By default minor ticks are not shown, i.e. there is only an empty list for them because it is as NullLocator 

---
# Other Types of Plots
![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/plot.png)
![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/bar.png)
![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/plot3d.png)

#### you need to use contourf.

#### Starting from the code below, try to reproduce the graphic on the right.

#### import numpy as np
#### import matplotlib.pyplot as plt
#### from mpl_toolkits.mplot3d import Axes3D

#### fig = plt.figure()
#### ax = Axes3D(fig) 
#### X = np.arange(-4, 4, 0.25)
#### Y = np.arange(-4, 4, 0.25)
#### X, Y = np.meshgrid(X, Y)
#### R = np.sqrt(X**2 + Y**2)
#### Z = np.sin(R)

#### ax.plot_surface(X, Y, Z, rstride=1, cstride=1, cmap='hot')

#### plt.show()
---



