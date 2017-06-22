---
layout: page
title: Data Model
permalink: /data-model/
---

[Time Series Databases][tsdb] are about storing [Time Series data][ts]. Each 
[Time Series][ts] consist of a sequence of time ordered data items. Each item 
consist of its time stamp and its actual value.

Time stamps are unsigned numbers that indicate the offset in time with respect
to a given [Epoch][epoch]. The [Media Type][mt] of item values is application 
specific and normally is Numerical or Textual.

As you can see Time Series data left out a lot of information that is needed
to get some meaning about it. Specifically the [Epoch][epoch] (normally the 
UNIX Epoch), [Temporal Resolution][tr] of each timestamp and the 
[Media Type][mt] of the data values. Without this information usage of Time 
Series is restricted to a single Program that knows it in advance.

In order to allow multiple tools to be used with the same Time Series, the model
is extended to add support for Time Series metadata. Thus removing the need
to exchange out of band the information required to get meaning about the
Time Series.

[epoch]: https://en.wikipedia.org/wiki/Epoch_(reference_date)
[mt]: https://en.wikipedia.org/wiki/Media_type
[tr]: https://en.wikipedia.org/wiki/Temporal_resolution
[ts]: https://en.wikipedia.org/wiki/Time_series
[tsdb]: https://en.wikipedia.org/wiki/Time_series_database
