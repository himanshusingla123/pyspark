<main class="col-12 col-md-9 col-xl-7 py-md-5 pl-md-5 pr-md-4 bd-content" role="main">
<div>          
  <section id="spark-streaming-legacy">
<h1>Spark Streaming (Legacy)<a class="headerlink" href="#spark-streaming-legacy" title="Permalink to this headline">¶</a></h1>
<section id="core-classes">
<h2>Core Classes<a class="headerlink" href="#core-classes" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.html#pyspark.streaming.StreamingContext" title="pyspark.streaming.StreamingContext"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext</span></code></a>(sparkContext[,&nbsp;…])</p></td>
<td><p>Main entry point for Spark Streaming functionality.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.html#pyspark.streaming.DStream" title="pyspark.streaming.DStream"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream</span></code></a>(jdstream,&nbsp;ssc,&nbsp;jrdd_deserializer)</p></td>
<td><p>A Discretized Stream (DStream), the basic abstraction in Spark Streaming, is a continuous sequence of RDDs (of the same type) representing a continuous stream of data (see <code class="xref py py-class docutils literal notranslate"><span class="pre">RDD</span></code> in the Spark core documentation for more details on RDDs).</p></td>
</tr>
</tbody>
</table>
</section>
<section id="streaming-management">
<h2>Streaming Management<a class="headerlink" href="#streaming-management" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.addStreamingListener.html#pyspark.streaming.StreamingContext.addStreamingListener" title="pyspark.streaming.StreamingContext.addStreamingListener"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.addStreamingListener</span></code></a>(…)</p></td>
<td><p>Add a [[org.apache.spark.streaming.scheduler.StreamingListener]] object for receiving system events related to streaming.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.awaitTermination.html#pyspark.streaming.StreamingContext.awaitTermination" title="pyspark.streaming.StreamingContext.awaitTermination"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.awaitTermination</span></code></a>([timeout])</p></td>
<td><p>Wait for the execution to stop.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.awaitTerminationOrTimeout.html#pyspark.streaming.StreamingContext.awaitTerminationOrTimeout" title="pyspark.streaming.StreamingContext.awaitTerminationOrTimeout"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.awaitTerminationOrTimeout</span></code></a>(timeout)</p></td>
<td><p>Wait for the execution to stop.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.checkpoint.html#pyspark.streaming.StreamingContext.checkpoint" title="pyspark.streaming.StreamingContext.checkpoint"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.checkpoint</span></code></a>(directory)</p></td>
<td><p>Sets the context to periodically checkpoint the DStream operations for master fault-tolerance.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.getActive.html#pyspark.streaming.StreamingContext.getActive" title="pyspark.streaming.StreamingContext.getActive"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.getActive</span></code></a>()</p></td>
<td><p>Return either the currently active StreamingContext (i.e., if there is a context started but not stopped) or None.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.getActiveOrCreate.html#pyspark.streaming.StreamingContext.getActiveOrCreate" title="pyspark.streaming.StreamingContext.getActiveOrCreate"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.getActiveOrCreate</span></code></a>(…)</p></td>
<td><p>Either return the active StreamingContext (i.e.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.getOrCreate.html#pyspark.streaming.StreamingContext.getOrCreate" title="pyspark.streaming.StreamingContext.getOrCreate"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.getOrCreate</span></code></a>(checkpointPath,&nbsp;…)</p></td>
<td><p>Either recreate a StreamingContext from checkpoint data or create a new StreamingContext.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.remember.html#pyspark.streaming.StreamingContext.remember" title="pyspark.streaming.StreamingContext.remember"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.remember</span></code></a>(duration)</p></td>
<td><p>Set each DStreams in this context to remember RDDs it generated in the last given duration.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.sparkContext.html#pyspark.streaming.StreamingContext.sparkContext" title="pyspark.streaming.StreamingContext.sparkContext"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.sparkContext</span></code></a></p></td>
<td><p>Return SparkContext which is associated with this StreamingContext.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.start.html#pyspark.streaming.StreamingContext.start" title="pyspark.streaming.StreamingContext.start"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.start</span></code></a>()</p></td>
<td><p>Start the execution of the streams.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.stop.html#pyspark.streaming.StreamingContext.stop" title="pyspark.streaming.StreamingContext.stop"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.stop</span></code></a>([stopSparkContext,&nbsp;…])</p></td>
<td><p>Stop the execution of the streams, with option of ensuring all received data has been processed.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.transform.html#pyspark.streaming.StreamingContext.transform" title="pyspark.streaming.StreamingContext.transform"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.transform</span></code></a>(dstreams,&nbsp;…)</p></td>
<td><p>Create a new DStream in which each RDD is generated by applying a function on RDDs of the DStreams.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.union.html#pyspark.streaming.StreamingContext.union" title="pyspark.streaming.StreamingContext.union"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.union</span></code></a>(*dstreams)</p></td>
<td><p>Create a unified DStream from multiple DStreams of the same type and same slide duration.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="input-and-output">
<h2>Input and Output<a class="headerlink" href="#input-and-output" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.binaryRecordsStream.html#pyspark.streaming.StreamingContext.binaryRecordsStream" title="pyspark.streaming.StreamingContext.binaryRecordsStream"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.binaryRecordsStream</span></code></a>(…)</p></td>
<td><p>Create an input stream that monitors a Hadoop-compatible file system for new files and reads them as flat binary files with records of fixed length.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.queueStream.html#pyspark.streaming.StreamingContext.queueStream" title="pyspark.streaming.StreamingContext.queueStream"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.queueStream</span></code></a>(rdds[,&nbsp;…])</p></td>
<td><p>Create an input stream from a queue of RDDs or list.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.socketTextStream.html#pyspark.streaming.StreamingContext.socketTextStream" title="pyspark.streaming.StreamingContext.socketTextStream"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.socketTextStream</span></code></a>(hostname,&nbsp;port)</p></td>
<td><p>Create an input from TCP source hostname:port.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.StreamingContext.textFileStream.html#pyspark.streaming.StreamingContext.textFileStream" title="pyspark.streaming.StreamingContext.textFileStream"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingContext.textFileStream</span></code></a>(directory)</p></td>
<td><p>Create an input stream that monitors a Hadoop-compatible file system for new files and reads them as text files.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.pprint.html#pyspark.streaming.DStream.pprint" title="pyspark.streaming.DStream.pprint"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.pprint</span></code></a>([num])</p></td>
<td><p>Print the first num elements of each RDD generated in this DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.saveAsTextFiles.html#pyspark.streaming.DStream.saveAsTextFiles" title="pyspark.streaming.DStream.saveAsTextFiles"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.saveAsTextFiles</span></code></a>(prefix[,&nbsp;suffix])</p></td>
<td><p>Save each RDD in this DStream as at text file, using string representation of elements.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="transformations-and-actions">
<h2>Transformations and Actions<a class="headerlink" href="#transformations-and-actions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.cache.html#pyspark.streaming.DStream.cache" title="pyspark.streaming.DStream.cache"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.cache</span></code></a>()</p></td>
<td><p>Persist the RDDs of this DStream with the default storage level (<cite>MEMORY_ONLY</cite>).</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.checkpoint.html#pyspark.streaming.DStream.checkpoint" title="pyspark.streaming.DStream.checkpoint"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.checkpoint</span></code></a>(interval)</p></td>
<td><p>Enable periodic checkpointing of RDDs of this DStream</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.cogroup.html#pyspark.streaming.DStream.cogroup" title="pyspark.streaming.DStream.cogroup"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.cogroup</span></code></a>(other[,&nbsp;numPartitions])</p></td>
<td><p>Return a new DStream by applying ‘cogroup’ between RDDs of this DStream and <cite>other</cite> DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.combineByKey.html#pyspark.streaming.DStream.combineByKey" title="pyspark.streaming.DStream.combineByKey"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.combineByKey</span></code></a>(createCombiner,&nbsp;…[,&nbsp;…])</p></td>
<td><p>Return a new DStream by applying combineByKey to each RDD.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.context.html#pyspark.streaming.DStream.context" title="pyspark.streaming.DStream.context"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.context</span></code></a>()</p></td>
<td><p>Return the StreamingContext associated with this DStream</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.count.html#pyspark.streaming.DStream.count" title="pyspark.streaming.DStream.count"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.count</span></code></a>()</p></td>
<td><p>Return a new DStream in which each RDD has a single element generated by counting each RDD of this DStream.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.countByValue.html#pyspark.streaming.DStream.countByValue" title="pyspark.streaming.DStream.countByValue"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.countByValue</span></code></a>()</p></td>
<td><p>Return a new DStream in which each RDD contains the counts of each distinct value in each RDD of this DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.countByValueAndWindow.html#pyspark.streaming.DStream.countByValueAndWindow" title="pyspark.streaming.DStream.countByValueAndWindow"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.countByValueAndWindow</span></code></a>(…[,&nbsp;…])</p></td>
<td><p>Return a new DStream in which each RDD contains the count of distinct elements in RDDs in a sliding window over this DStream.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.countByWindow.html#pyspark.streaming.DStream.countByWindow" title="pyspark.streaming.DStream.countByWindow"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.countByWindow</span></code></a>(windowDuration,&nbsp;…)</p></td>
<td><p>Return a new DStream in which each RDD has a single element generated by counting the number of elements in a window over this DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.filter.html#pyspark.streaming.DStream.filter" title="pyspark.streaming.DStream.filter"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.filter</span></code></a>(f)</p></td>
<td><p>Return a new DStream containing only the elements that satisfy predicate.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.flatMap.html#pyspark.streaming.DStream.flatMap" title="pyspark.streaming.DStream.flatMap"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.flatMap</span></code></a>(f[,&nbsp;preservesPartitioning])</p></td>
<td><p>Return a new DStream by applying a function to all elements of this DStream, and then flattening the results</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.flatMapValues.html#pyspark.streaming.DStream.flatMapValues" title="pyspark.streaming.DStream.flatMapValues"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.flatMapValues</span></code></a>(f)</p></td>
<td><p>Return a new DStream by applying a flatmap function to the value of each key-value pairs in this DStream without changing the key.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.foreachRDD.html#pyspark.streaming.DStream.foreachRDD" title="pyspark.streaming.DStream.foreachRDD"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.foreachRDD</span></code></a>(func)</p></td>
<td><p>Apply a function to each RDD in this DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.fullOuterJoin.html#pyspark.streaming.DStream.fullOuterJoin" title="pyspark.streaming.DStream.fullOuterJoin"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.fullOuterJoin</span></code></a>(other[,&nbsp;numPartitions])</p></td>
<td><p>Return a new DStream by applying ‘full outer join’ between RDDs of this DStream and <cite>other</cite> DStream.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.glom.html#pyspark.streaming.DStream.glom" title="pyspark.streaming.DStream.glom"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.glom</span></code></a>()</p></td>
<td><p>Return a new DStream in which RDD is generated by applying glom() to RDD of this DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.groupByKey.html#pyspark.streaming.DStream.groupByKey" title="pyspark.streaming.DStream.groupByKey"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.groupByKey</span></code></a>([numPartitions])</p></td>
<td><p>Return a new DStream by applying groupByKey on each RDD.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.groupByKeyAndWindow.html#pyspark.streaming.DStream.groupByKeyAndWindow" title="pyspark.streaming.DStream.groupByKeyAndWindow"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.groupByKeyAndWindow</span></code></a>(windowDuration,&nbsp;…)</p></td>
<td><p>Return a new DStream by applying <cite>groupByKey</cite> over a sliding window.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.join.html#pyspark.streaming.DStream.join" title="pyspark.streaming.DStream.join"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.join</span></code></a>(other[,&nbsp;numPartitions])</p></td>
<td><p>Return a new DStream by applying ‘join’ between RDDs of this DStream and <cite>other</cite> DStream.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.leftOuterJoin.html#pyspark.streaming.DStream.leftOuterJoin" title="pyspark.streaming.DStream.leftOuterJoin"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.leftOuterJoin</span></code></a>(other[,&nbsp;numPartitions])</p></td>
<td><p>Return a new DStream by applying ‘left outer join’ between RDDs of this DStream and <cite>other</cite> DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.map.html#pyspark.streaming.DStream.map" title="pyspark.streaming.DStream.map"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.map</span></code></a>(f[,&nbsp;preservesPartitioning])</p></td>
<td><p>Return a new DStream by applying a function to each element of DStream.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.mapPartitions.html#pyspark.streaming.DStream.mapPartitions" title="pyspark.streaming.DStream.mapPartitions"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.mapPartitions</span></code></a>(f[,&nbsp;preservesPartitioning])</p></td>
<td><p>Return a new DStream in which each RDD is generated by applying mapPartitions() to each RDDs of this DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.mapPartitionsWithIndex.html#pyspark.streaming.DStream.mapPartitionsWithIndex" title="pyspark.streaming.DStream.mapPartitionsWithIndex"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.mapPartitionsWithIndex</span></code></a>(f[,&nbsp;…])</p></td>
<td><p>Return a new DStream in which each RDD is generated by applying mapPartitionsWithIndex() to each RDDs of this DStream.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.mapValues.html#pyspark.streaming.DStream.mapValues" title="pyspark.streaming.DStream.mapValues"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.mapValues</span></code></a>(f)</p></td>
<td><p>Return a new DStream by applying a map function to the value of each key-value pairs in this DStream without changing the key.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.partitionBy.html#pyspark.streaming.DStream.partitionBy" title="pyspark.streaming.DStream.partitionBy"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.partitionBy</span></code></a>(numPartitions[,&nbsp;…])</p></td>
<td><p>Return a copy of the DStream in which each RDD are partitioned using the specified partitioner.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.persist.html#pyspark.streaming.DStream.persist" title="pyspark.streaming.DStream.persist"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.persist</span></code></a>(storageLevel)</p></td>
<td><p>Persist the RDDs of this DStream with the given storage level</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.reduce.html#pyspark.streaming.DStream.reduce" title="pyspark.streaming.DStream.reduce"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.reduce</span></code></a>(func)</p></td>
<td><p>Return a new DStream in which each RDD has a single element generated by reducing each RDD of this DStream.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.reduceByKey.html#pyspark.streaming.DStream.reduceByKey" title="pyspark.streaming.DStream.reduceByKey"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.reduceByKey</span></code></a>(func[,&nbsp;numPartitions])</p></td>
<td><p>Return a new DStream by applying reduceByKey to each RDD.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.reduceByKeyAndWindow.html#pyspark.streaming.DStream.reduceByKeyAndWindow" title="pyspark.streaming.DStream.reduceByKeyAndWindow"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.reduceByKeyAndWindow</span></code></a>(func,&nbsp;invFunc,&nbsp;…)</p></td>
<td><p>Return a new DStream by applying incremental <cite>reduceByKey</cite> over a sliding window.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.reduceByWindow.html#pyspark.streaming.DStream.reduceByWindow" title="pyspark.streaming.DStream.reduceByWindow"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.reduceByWindow</span></code></a>(reduceFunc,&nbsp;…)</p></td>
<td><p>Return a new DStream in which each RDD has a single element generated by reducing all elements in a sliding window over this DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.repartition.html#pyspark.streaming.DStream.repartition" title="pyspark.streaming.DStream.repartition"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.repartition</span></code></a>(numPartitions)</p></td>
<td><p>Return a new DStream with an increased or decreased level of parallelism.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.rightOuterJoin.html#pyspark.streaming.DStream.rightOuterJoin" title="pyspark.streaming.DStream.rightOuterJoin"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.rightOuterJoin</span></code></a>(other[,&nbsp;numPartitions])</p></td>
<td><p>Return a new DStream by applying ‘right outer join’ between RDDs of this DStream and <cite>other</cite> DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.slice.html#pyspark.streaming.DStream.slice" title="pyspark.streaming.DStream.slice"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.slice</span></code></a>(begin,&nbsp;end)</p></td>
<td><p>Return all the RDDs between ‘begin’ to ‘end’ (both included)</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.transform.html#pyspark.streaming.DStream.transform" title="pyspark.streaming.DStream.transform"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.transform</span></code></a>(func)</p></td>
<td><p>Return a new DStream in which each RDD is generated by applying a function on each RDD of this DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.transformWith.html#pyspark.streaming.DStream.transformWith" title="pyspark.streaming.DStream.transformWith"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.transformWith</span></code></a>(func,&nbsp;other[,&nbsp;…])</p></td>
<td><p>Return a new DStream in which each RDD is generated by applying a function on each RDD of this DStream and ‘other’ DStream.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.union.html#pyspark.streaming.DStream.union" title="pyspark.streaming.DStream.union"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.union</span></code></a>(other)</p></td>
<td><p>Return a new DStream by unifying data of another DStream with this DStream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.updateStateByKey.html#pyspark.streaming.DStream.updateStateByKey" title="pyspark.streaming.DStream.updateStateByKey"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.updateStateByKey</span></code></a>(updateFunc[,&nbsp;…])</p></td>
<td><p>Return a new “state” DStream where the state for each key is updated by applying the given function on the previous state of the key and the new values of the key.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.DStream.window.html#pyspark.streaming.DStream.window" title="pyspark.streaming.DStream.window"><code class="xref py py-obj docutils literal notranslate"><span class="pre">DStream.window</span></code></a>(windowDuration[,&nbsp;slideDuration])</p></td>
<td><p>Return a new DStream in which each RDD contains all the elements in seen in a sliding window of time over this DStream.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="kinesis">
<h2>Kinesis<a class="headerlink" href="#kinesis" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.kinesis.KinesisUtils.createStream.html#pyspark.streaming.kinesis.KinesisUtils.createStream" title="pyspark.streaming.kinesis.KinesisUtils.createStream"><code class="xref py py-obj docutils literal notranslate"><span class="pre">KinesisUtils.createStream</span></code></a>(ssc,&nbsp;…[,&nbsp;…])</p></td>
<td><p>Create an input stream that pulls messages from a Kinesis stream.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.streaming.kinesis.InitialPositionInStream.LATEST.html#pyspark.streaming.kinesis.InitialPositionInStream.LATEST" title="pyspark.streaming.kinesis.InitialPositionInStream.LATEST"><code class="xref py py-obj docutils literal notranslate"><span class="pre">InitialPositionInStream.LATEST</span></code></a></p></td>
<td><p></p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.streaming.kinesis.InitialPositionInStream.TRIM_HORIZON.html#pyspark.streaming.kinesis.InitialPositionInStream.TRIM_HORIZON" title="pyspark.streaming.kinesis.InitialPositionInStream.TRIM_HORIZON"><code class="xref py py-obj docutils literal notranslate"><span class="pre">InitialPositionInStream.TRIM_HORIZON</span></code></a></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>
</section>
</section>
</div>
</main>
