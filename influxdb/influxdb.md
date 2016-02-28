# InfluxDB

---

![](time.jpg)

## Time Series Database

^ Time Series Data
^ Sensor Data, Logdata, Events
^ Basically everything that is time based
^ InfluxDB is made to store a large volume of time-series data and perform real-time analysis on those data, quickly.

---

![fit](TICK-Stack.png)

---

## Use Cases

^ Statistics
^ Agregate huge amounts of data
^ Monitoring & Alerting

---

## Data Model

^ Schema less
^ Key-Value on Time Event
^ Values can be strings, floats, integers, or booleans

---

```sh
brew install InfluxDB
influxd -config /usr/local/etc/influxdb.conf
```

---

![fit](webadmin.png)

---

## Query Language

---

```SQL
SELECT
  COUNT(duration) as count_duration,
  MIN(duration) as min,
  MAX(duration) as max,
  MEAN(duration) as MEAN
FROM events
WHERE time > now() - 1h
GROUP BY time(30s)
```

^ Percentile and others also available
^ You can do joins ad merges

---

```SQL
INSERT cpu_load,server_name=gilbert value=2
```

^ Values can be strings, floats, integers, or booleans
^ Tags are indexed and can be strings

---

## Retention

---

```SQL
CREATE RETENTION POLICY two_hours
  ON food_data DURATION 2h REPLICATION 1 DEFAULT
```

---

## Downsampling

^ InfluxDB can handle hundreds of thousands of data points per second.
^ A natural solution is to downsample the data; keep the high precision raw data for only a limited time, and store the lower precision, summarized data for much longer or forever.
^ do precalculations
^ organize the data in a different way

---

```SQL
CREATE CONTINUOUS QUERY cq_30m ON food_data
BEGIN
  SELECT mean(website) AS mean_website,
         mean(phone) AS mean_phone
  INTO food_data."default".downsampled_orders
  FROM orders
  GROUP BY time(30m)
END
```

---

> Bodo Tasche
> @bitboxer
-- CTO bitcrowd

---

# Credits

```
* Time Series Image CC-BY-2.0 Ian Sane https://www.flickr.com/photos/31246066@N04/5261957053
```
