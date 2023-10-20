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

<h2>redis</h2>

(numbers on 64-bit instances) 

|Actor|Condition|Memory usage|
|---|---|---|
|empty instance|| ~3MB|
|1 Million small keys|string value pairs| ~85MB|
|1 Million keys|Hash value, representing an object with 5 fields| ~160MB|
|number of key limit|| 2^32|
|number of elements for hash, list, set, sorted set|| 2^32|
|keys per instance|| over 250 million|
|conversion threshold from ziplist to skiplist|entry count| 512| 



# reference 

[back-of-the-envelope-estimation](https://bytebytego.com/courses/system-design-interview/back-of-the-envelope-estimation)
[redis](https://redis.io/docs/getting-started/faq/)
