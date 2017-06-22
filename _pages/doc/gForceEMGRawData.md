---
layout: default
---
* This will become a table of contents (this text will be scraped).
{:toc}

Some versions of gForce provides users with the ability of capturing EMG raw
data with the [EMG Raw Data Capture Utility](/assets/downloads/RawDataCapture.zip)
or [EMG Raw Data Capture SDK](/assets/downloads/RawDataCaptureSDK.zip).

EMG raw data is usually used in medical researching or for the developers
that want to build their own gesture recognition algorithm.

If you need such a special version, please query info@oymotion.com.


## Data Format
The EMG raw data, either is captured in files by the EMG Raw Data Capture
Utility or developer's own application built upon the EMG Raw Data SDK,
consists of a series of 8-channel interleaved data. Let's look at the first
32 bytes of the captured raw data:


Byte|0|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|21|22|23|24|25|26|27|28|29|30|31
----|-|-|-|-|-|-|-|-|-|-|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--
**Channel**|0|1|2|3|4|5|6|7|0|1|2|3|4|5|6|7|0|1|2|3|4|5|6|7|0|1|2|3|4|5|6|7
**Sample**|0|0|0|0|0|0|0|0|1|1|1|1|1|1|1|1|2|2|2|2|2|2|2|2|3|3|3|3|3|3|3|3

According to the above table, every 8 channels, namely channel 0 - 7 of 1 byte
per channel, make up 1 sample, so the 32 bytes are totally 4 samples.

The same for any capture file, as there is no header in the file.

## Plotting in Matlab
The following is a bunch of commands to read capture file `rawdata.hex` and
plot the channel 0 in Matlab:

```matlab
>> fp=fopen('rawdata.hex', 'r', 'l');
>> data=fread(fp,'uchar','l');
>> data_array=reshape(data, 8, []);
>> figure;
>> plot(data_array(1,:));
```
You will be able to see the plotted figure like the following:

  ![RawDataMatlabFigure01](/assets/images/RawDataMatlabFigure01.jpg)
