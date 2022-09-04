---
layout: post
title: "PySerial Plotter"
author: vaibhav
categories: [Electronics, Tech, Microcontrollers, Python, Project]
tags: [featured]
image: assets/images/pyserial.jpg
---
PySerial Plotter is a python app made using tkinter, matplotlib and pyserial library. It lets you plot the serial data you receive over a COM port from a microcontroller. Unlike the one in the Arduino IDE, this one allows you to plot multiple values and also shows them in a modern gui console, where you can see a multiplot and individual plots for every datapoint.

Along with plotting, all the data is logged in a CSV file with timestamps.

### Usage 
On your microcontroller just print the data formatted in a dictionary form like "{'Temperature':32, 'Humidity':45}"

And on your PC, use 
{% highlight ruby %}
python pyserial.py COM5 
{% endhighlight %}
where COM5 is the name of the COM port your mcu is connected to.

You can access the code here on [GitHub][github].

[github]: https://github.com/vaibhavdevnani7/python_tkinter_serial-plotter
