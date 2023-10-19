# measures and numbers for system design

<h2>latency</h2>

|Operation|Number|
|---|---|
|L1 cache reference|0.5 ns|
|L2 cache reference|7 ns|
|Main memory reference|25 ns|
|Read 1 MB sequentially from meory|250,000 ns|
|Read 1 MG sequentially from SSD|10,000,000 ns|
|Read 1 MG sequentially from HDD|10,000,000 ns|

<h2>availability</h2>

|Availability|Downtime per day|Downtime per month|
|---|---|---|
|99%|14.40 minutes|7.31 hours|
|99.99%|8.64 seconds|4.38 minutes|
|99.999%|864.00 milliseconds|26.30 seconds|

# reference 

[back-of-the-envelope-estimation](https://bytebytego.com/courses/system-design-interview/back-of-the-envelope-estimation)
