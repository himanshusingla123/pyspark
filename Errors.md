<main class="col-12 col-md-9 col-xl-7 py-md-5 pl-md-5 pr-md-4 bd-content" role="main">
 <div>
<section id="errors">
<h1>Errors<a class="headerlink" href="#errors" title="Permalink to this headline">¶</a></h1>
<section id="classes">
<h2>Classes<a class="headerlink" href="#classes" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.errors.PySparkException.html#pyspark.errors.PySparkException" title="pyspark.errors.PySparkException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">PySparkException</span></code></a>([message,&nbsp;error_class,&nbsp;…])</p></td>
<td><p>Base Exception for handling errors generated from PySpark.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.errors.AnalysisException.html#pyspark.errors.AnalysisException" title="pyspark.errors.AnalysisException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">AnalysisException</span></code></a>([message,&nbsp;error_class,&nbsp;…])</p></td>
<td><p>Failed to analyze a SQL query plan.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.errors.TempTableAlreadyExistsException.html#pyspark.errors.TempTableAlreadyExistsException" title="pyspark.errors.TempTableAlreadyExistsException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">TempTableAlreadyExistsException</span></code></a>([message,&nbsp;…])</p></td>
<td><p>Failed to create temp view since it is already exists.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.errors.ParseException.html#pyspark.errors.ParseException" title="pyspark.errors.ParseException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ParseException</span></code></a>([message,&nbsp;error_class,&nbsp;…])</p></td>
<td><p>Failed to parse a SQL command.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.errors.IllegalArgumentException.html#pyspark.errors.IllegalArgumentException" title="pyspark.errors.IllegalArgumentException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">IllegalArgumentException</span></code></a>([message,&nbsp;…])</p></td>
<td><p>Passed an illegal or inappropriate argument.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.errors.StreamingQueryException.html#pyspark.errors.StreamingQueryException" title="pyspark.errors.StreamingQueryException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">StreamingQueryException</span></code></a>([message,&nbsp;…])</p></td>
<td><p>Exception that stopped a <code class="xref py py-class docutils literal notranslate"><span class="pre">StreamingQuery</span></code>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.errors.QueryExecutionException.html#pyspark.errors.QueryExecutionException" title="pyspark.errors.QueryExecutionException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">QueryExecutionException</span></code></a>([message,&nbsp;…])</p></td>
<td><p>Failed to execute a query.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.errors.PythonException.html#pyspark.errors.PythonException" title="pyspark.errors.PythonException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">PythonException</span></code></a>([message,&nbsp;error_class,&nbsp;…])</p></td>
<td><p>Exceptions thrown from Python workers.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.errors.UnknownException.html#pyspark.errors.UnknownException" title="pyspark.errors.UnknownException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">UnknownException</span></code></a>([message,&nbsp;error_class,&nbsp;…])</p></td>
<td><p>None of the above exceptions.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.errors.SparkUpgradeException.html#pyspark.errors.SparkUpgradeException" title="pyspark.errors.SparkUpgradeException"><code class="xref py py-obj docutils literal notranslate"><span class="pre">SparkUpgradeException</span></code></a>([message,&nbsp;…])</p></td>
<td><p>Exception thrown because of Spark upgrade.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="methods">
<h2>Methods<a class="headerlink" href="#methods" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.errors.PySparkException.getErrorClass.html#pyspark.errors.PySparkException.getErrorClass" title="pyspark.errors.PySparkException.getErrorClass"><code class="xref py py-obj docutils literal notranslate"><span class="pre">PySparkException.getErrorClass</span></code></a>()</p></td>
<td><p>Returns an error class as a string.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.errors.PySparkException.getMessageParameters.html#pyspark.errors.PySparkException.getMessageParameters" title="pyspark.errors.PySparkException.getMessageParameters"><code class="xref py py-obj docutils literal notranslate"><span class="pre">PySparkException.getMessageParameters</span></code></a>()</p></td>
<td><p>Returns a message parameters as a dictionary.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.errors.PySparkException.getSqlState.html#pyspark.errors.PySparkException.getSqlState" title="pyspark.errors.PySparkException.getSqlState"><code class="xref py py-obj docutils literal notranslate"><span class="pre">PySparkException.getSqlState</span></code></a>()</p></td>
<td><p>Returns an SQLSTATE as a string.</p></td>
</tr>
</tbody>
</table>
</section>
</section>
</div>
</main>
