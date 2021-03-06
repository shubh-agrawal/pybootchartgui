# Source for pybootchartgui

In view of pybootchartgui being deprecated and replaced with bootchart2, this repository aims to provide source code to help assist old scripts that include pybootchartgui as binary.

I suggest to replace old binary with pythonic command, as explained below.

## Where it has been tested?

This has been tested on Ubuntu-20.04 with Python 3.8. 

Application tested was to run grab-bootchart.sh script that produces android os bootchart. 

[Android Bootchart Usage](https://source.android.com/devices/tech/perf/boot-times#bootchart)


## Requirements and How-to-Use

Install cairo. For ubuntu,
``` 
sudo apt install python-cairo
```


Unzip / clone this directory in your system as per your wish. 

Replace binary call of `pybootchartgui [arguments]` with 
```
python /path/to/pybootchartgui/pybootchartgui.py [arguments]
```

## Future

I would be happy if someone can create dpkg downloadable for this source for distribution with appropriate dependencies. This also will eliminate any file modification required on user's end.


## Readme from old repository
```
PYBOOTCHARTGUI
----------------

pybootchartgui is a tool (now included as part of bootchart2) for
visualization and analysis of the GNU/Linux boot process. It renders
the output of the boot-logger tool bootchart (see
http://www.bootchart.org/) to either the screen or files of various
formats. Bootchart collects information about the processes, their
dependencies, and resource consumption during boot of a GNU/Linux
system. The pybootchartgui tools visualizes the process tree and
overall resource utilization.

pybootchartgui is a port of the visualization part of bootchart from
Java to Python and Cairo.

Adapted from the bootchart-documentation:

The CPU and disk statistics are used to render stacked area and line 
charts. The process information is used to create a Gantt chart
showing process dependency, states and CPU usage.

A typical boot sequence consists of several hundred processes. Since
it is difficult to visualize such amount of data in a comprehensible
way, tree pruning is utilized. Idle background processes and
short-lived processes are removed. Similar processes running in
parallel are also merged together.

Finally, the performance and dependency charts are rendered as a
single image to either the screen or in PNG, PDF or SVG format.


To get help for pybootchartgui, run

$ pybootchartgui --help

This code was originally hosted at:
http://code.google.com/p/pybootchartgui/
  ```
