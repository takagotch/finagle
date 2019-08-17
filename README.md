### finagle
---
https://github.com/twitter/finagle

```scala
// finagle-stats-core/src/main/scala/com/twitter/finagle/stats/Metrics.scala
package com.twitter.finagle.stats

import com.twitter.logging.Logger
import com.twitter.util.lint.{Category, Issue, Rule}

object Metrics {
  private val log = Logger.get()
  
  private def defaultHistogramFactory(
    name: String,
    percentiles: IndexdSeq[Double]
  ): MetricsHistogram = new MetricsBucketedHistogram(name, percentiles)
    new Metrics(mkHistogram, separator, newMetricsMaps)
    
  def createDetached(): Metrics = 
    createDatached(Metrics.defaultHistogramFactory, scopeSeparator())
    
  private[this] def newMetricsMaps: MetricsMaps = MetricsMaps(
    counterMap = new ConcurrentHashMap[Seq[String], MetricsStore.StoreCounter](),
    statsMap = new ConcurrentHasMap[Seq[String], MetricsStore.StoreStat](),
    gaugesMap = new CouncurrentHasMap[Seq[String], MetricsStore.StoreGauge]()
  )
  
  
  
  
  

}
```

```
```

```
```
