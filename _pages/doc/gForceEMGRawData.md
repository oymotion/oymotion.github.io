---
layout: default
---
* This will become a table of contents (this text will be scraped).
{:toc}

Some versions of gForce provides users with the ability of capturing sEMG raw
data with the [sEMG Raw Data Capture Utility](/assets/downloads/RawDataCapture.zip)
or [sEMG Raw Data Capture SDK](/assets/downloads/RawDataCaptureSDK.zip).

sEMG raw data is usually used in medical researching or for the developers
that want to build their own gesture recognition algorithm.

If you need such a special version of gForce, please query info@oymotion.com.


## Data Format
The sEMG raw data, either is captured in files by the sEMG Raw Data Capture
Utility or developer's own application built upon the sEMG Raw Data SDK,
consists of a series of samples of 8-channel interleaved data. Let's look 
at the first 18 bytes of the captured raw data for instance:

Byte|0|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|...
----|-|-|-|-|-|-|-|-|-|-|--|--|--|--|--|--|--|--|...
**Channel**|0|1|2|3|4|5|6|7|0|1|2|3|4|5|6|7|0|1|...
**Sample**|0|0|0|0|0|0|0|0|1|1|1|1|1|1|1|1|2|2|...

According to the above table, data of every 8 channels, consequently channel 
0 - 7, makes up 1 sample, and each channel occupies 1 byte, so the data of 
channel 0 is byte 0, 8, 16, 24, 32...; and channel 7 byte 7, 15, 23, 31, 39...

The same for any captured raw data file, as there is no header in the file.

## More about Channel Sample Data
Since it is 1 byte per channel per sample, and the output votage is 0-2.5v, and
amplifier is 800x, the input vatage of the orignal sEMG is:

{% raw %}
  $$in &= \frac{1.25 \times \(out-128\)}{128 \times 800}}$$                           
{% endraw %}

## Plotting in Matlab
The following are a bunch of commands to read captured raw data file 
`rawdata.hex` and plot the channel 0 in Matlab:

```matlab
>> fp=fopen('rawdata.hex', 'r', 'l');
>> data=fread(fp,'uchar','l');
>> data_2d=reshape(data, 8, []);
>> figure;
>> plot(data_2d(1,:));
```

It must be noted that Matlab uses 1-based array index!
 
You will be able to see the plotted figure like the following:

  ![RawDataMatlabFigure01](/assets/images/RawDataMatlabFigure01.jpg)

If you want to plot channel 7 instead, just replace the last command with:

```matlab
>> plot(data_2d(8,:));
```
