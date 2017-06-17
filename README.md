# EMG Filters

## Overview
This library provides the following filters for processing OYMotion's sEMG
signals:

1. an anti-hum notch filter to filter out 50HZ or 60HZ power line noise.
2. a lowpass filter to filter out noises above 150HZ.
3. a highpass filter to filter out noises below 20HZ.

You can turn on or off these filters by the init function.

**Note**:
Input frequencies of 500HZ and 1000HZ are supported only!

As you might have known, there has been some existing DSP libraries which provide
rich set of functions you may need (e.g. https://github.com/vinniefalco/DSPFilters).
We are NOT going to re-invent the wheel! Instead, what we're going to provide is
a set of simplified functions that allows developers to focus on sEMG signal
processing with common configurations.

## How to Use It
The library is written in standard C++ without dependency of external
libraries, so it should be easy to embed it into any C++ project.

[A simple sample code for using on Arduino][ArduinoSampleCode] in the `example`
folder is provided for your reference.

[ArduinoSampleCode]: https://github.com/oymotion/EMGFilters/blob/master/examples/SimpleEMGFilters/SimpleEMGFilters.ino 
