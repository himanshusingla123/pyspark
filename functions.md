<main class="col-12 col-md-9 col-xl-7 py-md-5 pl-md-5 pr-md-4 bd-content" role="main">
<div>               
  <section id="functions">
<h1>Functions<a class="headerlink" href="#functions" title="Permalink to this headline">¶</a></h1>
<p>A collections of builtin functions available for DataFrame operations.
From Apache Spark 3.5.0, all functions support Spark Connect.</p>
<section id="normal-functions">
<h2>Normal Functions<a class="headerlink" href="#normal-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.col.html#pyspark.sql.functions.col" title="pyspark.sql.functions.col"><code class="xref py py-obj docutils literal notranslate"><span class="pre">col</span></code></a>(col)</p></td>
<td><p>Returns a <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> based on the given column name.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.column.html#pyspark.sql.functions.column" title="pyspark.sql.functions.column"><code class="xref py py-obj docutils literal notranslate"><span class="pre">column</span></code></a>(col)</p></td>
<td><p>Returns a <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> based on the given column name.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.lit.html#pyspark.sql.functions.lit" title="pyspark.sql.functions.lit"><code class="xref py py-obj docutils literal notranslate"><span class="pre">lit</span></code></a>(col)</p></td>
<td><p>Creates a <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> of literal value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.broadcast.html#pyspark.sql.functions.broadcast" title="pyspark.sql.functions.broadcast"><code class="xref py py-obj docutils literal notranslate"><span class="pre">broadcast</span></code></a>(df)</p></td>
<td><p>Marks a DataFrame as small enough for use in broadcast joins.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.coalesce.html#pyspark.sql.functions.coalesce" title="pyspark.sql.functions.coalesce"><code class="xref py py-obj docutils literal notranslate"><span class="pre">coalesce</span></code></a>(*cols)</p></td>
<td><p>Returns the first column that is not null.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.input_file_name.html#pyspark.sql.functions.input_file_name" title="pyspark.sql.functions.input_file_name"><code class="xref py py-obj docutils literal notranslate"><span class="pre">input_file_name</span></code></a>()</p></td>
<td><p>Creates a string column for the file name of the current Spark task.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.isnan.html#pyspark.sql.functions.isnan" title="pyspark.sql.functions.isnan"><code class="xref py py-obj docutils literal notranslate"><span class="pre">isnan</span></code></a>(col)</p></td>
<td><p>An expression that returns true if the column is NaN.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.isnull.html#pyspark.sql.functions.isnull" title="pyspark.sql.functions.isnull"><code class="xref py py-obj docutils literal notranslate"><span class="pre">isnull</span></code></a>(col)</p></td>
<td><p>An expression that returns true if the column is null.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.monotonically_increasing_id.html#pyspark.sql.functions.monotonically_increasing_id" title="pyspark.sql.functions.monotonically_increasing_id"><code class="xref py py-obj docutils literal notranslate"><span class="pre">monotonically_increasing_id</span></code></a>()</p></td>
<td><p>A column that generates monotonically increasing 64-bit integers.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.named_struct.html#pyspark.sql.functions.named_struct" title="pyspark.sql.functions.named_struct"><code class="xref py py-obj docutils literal notranslate"><span class="pre">named_struct</span></code></a>(*cols)</p></td>
<td><p>Creates a struct with the given field names and values.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.nanvl.html#pyspark.sql.functions.nanvl" title="pyspark.sql.functions.nanvl"><code class="xref py py-obj docutils literal notranslate"><span class="pre">nanvl</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns col1 if it is not NaN, or col2 if col1 is NaN.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.rand.html#pyspark.sql.functions.rand" title="pyspark.sql.functions.rand"><code class="xref py py-obj docutils literal notranslate"><span class="pre">rand</span></code></a>([seed])</p></td>
<td><p>Generates a random column with independent and identically distributed (i.i.d.) samples uniformly distributed in [0.0, 1.0).</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.randn.html#pyspark.sql.functions.randn" title="pyspark.sql.functions.randn"><code class="xref py py-obj docutils literal notranslate"><span class="pre">randn</span></code></a>([seed])</p></td>
<td><p>Generates a column with independent and identically distributed (i.i.d.) samples from the standard normal distribution.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.spark_partition_id.html#pyspark.sql.functions.spark_partition_id" title="pyspark.sql.functions.spark_partition_id"><code class="xref py py-obj docutils literal notranslate"><span class="pre">spark_partition_id</span></code></a>()</p></td>
<td><p>A column for partition ID.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.when.html#pyspark.sql.functions.when" title="pyspark.sql.functions.when"><code class="xref py py-obj docutils literal notranslate"><span class="pre">when</span></code></a>(condition,&nbsp;value)</p></td>
<td><p>Evaluates a list of conditions and returns one of multiple possible result expressions.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bitwise_not.html#pyspark.sql.functions.bitwise_not" title="pyspark.sql.functions.bitwise_not"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bitwise_not</span></code></a>(col)</p></td>
<td><p>Computes bitwise not.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bitwiseNOT.html#pyspark.sql.functions.bitwiseNOT" title="pyspark.sql.functions.bitwiseNOT"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bitwiseNOT</span></code></a>(col)</p></td>
<td><p>Computes bitwise not.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.expr.html#pyspark.sql.functions.expr" title="pyspark.sql.functions.expr"><code class="xref py py-obj docutils literal notranslate"><span class="pre">expr</span></code></a>(str)</p></td>
<td><p>Parses the expression string into the column that it represents</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.greatest.html#pyspark.sql.functions.greatest" title="pyspark.sql.functions.greatest"><code class="xref py py-obj docutils literal notranslate"><span class="pre">greatest</span></code></a>(*cols)</p></td>
<td><p>Returns the greatest value of the list of column names, skipping null values.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.least.html#pyspark.sql.functions.least" title="pyspark.sql.functions.least"><code class="xref py py-obj docutils literal notranslate"><span class="pre">least</span></code></a>(*cols)</p></td>
<td><p>Returns the least value of the list of column names, skipping null values.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="math-functions">
<h2>Math Functions<a class="headerlink" href="#math-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sqrt.html#pyspark.sql.functions.sqrt" title="pyspark.sql.functions.sqrt"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sqrt</span></code></a>(col)</p></td>
<td><p>Computes the square root of the specified float value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.abs.html#pyspark.sql.functions.abs" title="pyspark.sql.functions.abs"><code class="xref py py-obj docutils literal notranslate"><span class="pre">abs</span></code></a>(col)</p></td>
<td><p>Computes the absolute value.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.acos.html#pyspark.sql.functions.acos" title="pyspark.sql.functions.acos"><code class="xref py py-obj docutils literal notranslate"><span class="pre">acos</span></code></a>(col)</p></td>
<td><p>Computes inverse cosine of the input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.acosh.html#pyspark.sql.functions.acosh" title="pyspark.sql.functions.acosh"><code class="xref py py-obj docutils literal notranslate"><span class="pre">acosh</span></code></a>(col)</p></td>
<td><p>Computes inverse hyperbolic cosine of the input column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.asin.html#pyspark.sql.functions.asin" title="pyspark.sql.functions.asin"><code class="xref py py-obj docutils literal notranslate"><span class="pre">asin</span></code></a>(col)</p></td>
<td><p>Computes inverse sine of the input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.asinh.html#pyspark.sql.functions.asinh" title="pyspark.sql.functions.asinh"><code class="xref py py-obj docutils literal notranslate"><span class="pre">asinh</span></code></a>(col)</p></td>
<td><p>Computes inverse hyperbolic sine of the input column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.atan.html#pyspark.sql.functions.atan" title="pyspark.sql.functions.atan"><code class="xref py py-obj docutils literal notranslate"><span class="pre">atan</span></code></a>(col)</p></td>
<td><p>Compute inverse tangent of the input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.atanh.html#pyspark.sql.functions.atanh" title="pyspark.sql.functions.atanh"><code class="xref py py-obj docutils literal notranslate"><span class="pre">atanh</span></code></a>(col)</p></td>
<td><p>Computes inverse hyperbolic tangent of the input column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.atan2.html#pyspark.sql.functions.atan2" title="pyspark.sql.functions.atan2"><code class="xref py py-obj docutils literal notranslate"><span class="pre">atan2</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p></p><div class="versionadded">
<p><span class="versionmodified added">New in version 1.4.0.</span></p>
</div>
<p></p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bin.html#pyspark.sql.functions.bin" title="pyspark.sql.functions.bin"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bin</span></code></a>(col)</p></td>
<td><p>Returns the string representation of the binary value of the given column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.cbrt.html#pyspark.sql.functions.cbrt" title="pyspark.sql.functions.cbrt"><code class="xref py py-obj docutils literal notranslate"><span class="pre">cbrt</span></code></a>(col)</p></td>
<td><p>Computes the cube-root of the given value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.ceil.html#pyspark.sql.functions.ceil" title="pyspark.sql.functions.ceil"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ceil</span></code></a>(col)</p></td>
<td><p>Computes the ceiling of the given value.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.ceiling.html#pyspark.sql.functions.ceiling" title="pyspark.sql.functions.ceiling"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ceiling</span></code></a>(col)</p></td>
<td><p>Computes the ceiling of the given value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.conv.html#pyspark.sql.functions.conv" title="pyspark.sql.functions.conv"><code class="xref py py-obj docutils literal notranslate"><span class="pre">conv</span></code></a>(col,&nbsp;fromBase,&nbsp;toBase)</p></td>
<td><p>Convert a number in a string column from one base to another.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.cos.html#pyspark.sql.functions.cos" title="pyspark.sql.functions.cos"><code class="xref py py-obj docutils literal notranslate"><span class="pre">cos</span></code></a>(col)</p></td>
<td><p>Computes cosine of the input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.cosh.html#pyspark.sql.functions.cosh" title="pyspark.sql.functions.cosh"><code class="xref py py-obj docutils literal notranslate"><span class="pre">cosh</span></code></a>(col)</p></td>
<td><p>Computes hyperbolic cosine of the input column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.cot.html#pyspark.sql.functions.cot" title="pyspark.sql.functions.cot"><code class="xref py py-obj docutils literal notranslate"><span class="pre">cot</span></code></a>(col)</p></td>
<td><p>Computes cotangent of the input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.csc.html#pyspark.sql.functions.csc" title="pyspark.sql.functions.csc"><code class="xref py py-obj docutils literal notranslate"><span class="pre">csc</span></code></a>(col)</p></td>
<td><p>Computes cosecant of the input column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.e.html#pyspark.sql.functions.e" title="pyspark.sql.functions.e"><code class="xref py py-obj docutils literal notranslate"><span class="pre">e</span></code></a>()</p></td>
<td><p>Returns Euler’s number.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.exp.html#pyspark.sql.functions.exp" title="pyspark.sql.functions.exp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">exp</span></code></a>(col)</p></td>
<td><p>Computes the exponential of the given value.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.expm1.html#pyspark.sql.functions.expm1" title="pyspark.sql.functions.expm1"><code class="xref py py-obj docutils literal notranslate"><span class="pre">expm1</span></code></a>(col)</p></td>
<td><p>Computes the exponential of the given value minus one.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.factorial.html#pyspark.sql.functions.factorial" title="pyspark.sql.functions.factorial"><code class="xref py py-obj docutils literal notranslate"><span class="pre">factorial</span></code></a>(col)</p></td>
<td><p>Computes the factorial of the given value.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.floor.html#pyspark.sql.functions.floor" title="pyspark.sql.functions.floor"><code class="xref py py-obj docutils literal notranslate"><span class="pre">floor</span></code></a>(col)</p></td>
<td><p>Computes the floor of the given value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.hex.html#pyspark.sql.functions.hex" title="pyspark.sql.functions.hex"><code class="xref py py-obj docutils literal notranslate"><span class="pre">hex</span></code></a>(col)</p></td>
<td><p>Computes hex value of the given column, which could be <a class="reference internal" href="api/pyspark.sql.types.StringType.html#pyspark.sql.types.StringType" title="pyspark.sql.types.StringType"><code class="xref py py-class docutils literal notranslate"><span class="pre">pyspark.sql.types.StringType</span></code></a>, <a class="reference internal" href="api/pyspark.sql.types.BinaryType.html#pyspark.sql.types.BinaryType" title="pyspark.sql.types.BinaryType"><code class="xref py py-class docutils literal notranslate"><span class="pre">pyspark.sql.types.BinaryType</span></code></a>, <a class="reference internal" href="api/pyspark.sql.types.IntegerType.html#pyspark.sql.types.IntegerType" title="pyspark.sql.types.IntegerType"><code class="xref py py-class docutils literal notranslate"><span class="pre">pyspark.sql.types.IntegerType</span></code></a> or <a class="reference internal" href="api/pyspark.sql.types.LongType.html#pyspark.sql.types.LongType" title="pyspark.sql.types.LongType"><code class="xref py py-class docutils literal notranslate"><span class="pre">pyspark.sql.types.LongType</span></code></a>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.unhex.html#pyspark.sql.functions.unhex" title="pyspark.sql.functions.unhex"><code class="xref py py-obj docutils literal notranslate"><span class="pre">unhex</span></code></a>(col)</p></td>
<td><p>Inverse of hex.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.hypot.html#pyspark.sql.functions.hypot" title="pyspark.sql.functions.hypot"><code class="xref py py-obj docutils literal notranslate"><span class="pre">hypot</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Computes <code class="docutils literal notranslate"><span class="pre">sqrt(a^2</span> <span class="pre">+</span> <span class="pre">b^2)</span></code> without intermediate overflow or underflow.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.ln.html#pyspark.sql.functions.ln" title="pyspark.sql.functions.ln"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ln</span></code></a>(col)</p></td>
<td><p>Returns the natural logarithm of the argument.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.log.html#pyspark.sql.functions.log" title="pyspark.sql.functions.log"><code class="xref py py-obj docutils literal notranslate"><span class="pre">log</span></code></a>(arg1[,&nbsp;arg2])</p></td>
<td><p>Returns the first argument-based logarithm of the second argument.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.log10.html#pyspark.sql.functions.log10" title="pyspark.sql.functions.log10"><code class="xref py py-obj docutils literal notranslate"><span class="pre">log10</span></code></a>(col)</p></td>
<td><p>Computes the logarithm of the given value in Base 10.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.log1p.html#pyspark.sql.functions.log1p" title="pyspark.sql.functions.log1p"><code class="xref py py-obj docutils literal notranslate"><span class="pre">log1p</span></code></a>(col)</p></td>
<td><p>Computes the natural logarithm of the “given value plus one”.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.log2.html#pyspark.sql.functions.log2" title="pyspark.sql.functions.log2"><code class="xref py py-obj docutils literal notranslate"><span class="pre">log2</span></code></a>(col)</p></td>
<td><p>Returns the base-2 logarithm of the argument.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.negate.html#pyspark.sql.functions.negate" title="pyspark.sql.functions.negate"><code class="xref py py-obj docutils literal notranslate"><span class="pre">negate</span></code></a>(col)</p></td>
<td><p>Returns the negative value.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.negative.html#pyspark.sql.functions.negative" title="pyspark.sql.functions.negative"><code class="xref py py-obj docutils literal notranslate"><span class="pre">negative</span></code></a>(col)</p></td>
<td><p>Returns the negative value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.pi.html#pyspark.sql.functions.pi" title="pyspark.sql.functions.pi"><code class="xref py py-obj docutils literal notranslate"><span class="pre">pi</span></code></a>()</p></td>
<td><p>Returns Pi.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.pmod.html#pyspark.sql.functions.pmod" title="pyspark.sql.functions.pmod"><code class="xref py py-obj docutils literal notranslate"><span class="pre">pmod</span></code></a>(dividend,&nbsp;divisor)</p></td>
<td><p>Returns the positive value of dividend mod divisor.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.positive.html#pyspark.sql.functions.positive" title="pyspark.sql.functions.positive"><code class="xref py py-obj docutils literal notranslate"><span class="pre">positive</span></code></a>(col)</p></td>
<td><p>Returns the value.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.pow.html#pyspark.sql.functions.pow" title="pyspark.sql.functions.pow"><code class="xref py py-obj docutils literal notranslate"><span class="pre">pow</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns the value of the first argument raised to the power of the second argument.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.power.html#pyspark.sql.functions.power" title="pyspark.sql.functions.power"><code class="xref py py-obj docutils literal notranslate"><span class="pre">power</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns the value of the first argument raised to the power of the second argument.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.rint.html#pyspark.sql.functions.rint" title="pyspark.sql.functions.rint"><code class="xref py py-obj docutils literal notranslate"><span class="pre">rint</span></code></a>(col)</p></td>
<td><p>Returns the double value that is closest in value to the argument and is equal to a mathematical integer.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.round.html#pyspark.sql.functions.round" title="pyspark.sql.functions.round"><code class="xref py py-obj docutils literal notranslate"><span class="pre">round</span></code></a>(col[,&nbsp;scale])</p></td>
<td><p>Round the given value to <cite>scale</cite> decimal places using HALF_UP rounding mode if <cite>scale</cite> &gt;= 0 or at integral part when <cite>scale</cite> &lt; 0.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bround.html#pyspark.sql.functions.bround" title="pyspark.sql.functions.bround"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bround</span></code></a>(col[,&nbsp;scale])</p></td>
<td><p>Round the given value to <cite>scale</cite> decimal places using HALF_EVEN rounding mode if <cite>scale</cite> &gt;= 0 or at integral part when <cite>scale</cite> &lt; 0.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sec.html#pyspark.sql.functions.sec" title="pyspark.sql.functions.sec"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sec</span></code></a>(col)</p></td>
<td><p>Computes secant of the input column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.shiftleft.html#pyspark.sql.functions.shiftleft" title="pyspark.sql.functions.shiftleft"><code class="xref py py-obj docutils literal notranslate"><span class="pre">shiftleft</span></code></a>(col,&nbsp;numBits)</p></td>
<td><p>Shift the given value numBits left.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.shiftright.html#pyspark.sql.functions.shiftright" title="pyspark.sql.functions.shiftright"><code class="xref py py-obj docutils literal notranslate"><span class="pre">shiftright</span></code></a>(col,&nbsp;numBits)</p></td>
<td><p>(Signed) shift the given value numBits right.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.shiftrightunsigned.html#pyspark.sql.functions.shiftrightunsigned" title="pyspark.sql.functions.shiftrightunsigned"><code class="xref py py-obj docutils literal notranslate"><span class="pre">shiftrightunsigned</span></code></a>(col,&nbsp;numBits)</p></td>
<td><p>Unsigned shift the given value numBits right.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sign.html#pyspark.sql.functions.sign" title="pyspark.sql.functions.sign"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sign</span></code></a>(col)</p></td>
<td><p>Computes the signum of the given value.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.signum.html#pyspark.sql.functions.signum" title="pyspark.sql.functions.signum"><code class="xref py py-obj docutils literal notranslate"><span class="pre">signum</span></code></a>(col)</p></td>
<td><p>Computes the signum of the given value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sin.html#pyspark.sql.functions.sin" title="pyspark.sql.functions.sin"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sin</span></code></a>(col)</p></td>
<td><p>Computes sine of the input column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sinh.html#pyspark.sql.functions.sinh" title="pyspark.sql.functions.sinh"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sinh</span></code></a>(col)</p></td>
<td><p>Computes hyperbolic sine of the input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.tan.html#pyspark.sql.functions.tan" title="pyspark.sql.functions.tan"><code class="xref py py-obj docutils literal notranslate"><span class="pre">tan</span></code></a>(col)</p></td>
<td><p>Computes tangent of the input column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.tanh.html#pyspark.sql.functions.tanh" title="pyspark.sql.functions.tanh"><code class="xref py py-obj docutils literal notranslate"><span class="pre">tanh</span></code></a>(col)</p></td>
<td><p>Computes hyperbolic tangent of the input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.toDegrees.html#pyspark.sql.functions.toDegrees" title="pyspark.sql.functions.toDegrees"><code class="xref py py-obj docutils literal notranslate"><span class="pre">toDegrees</span></code></a>(col)</p></td>
<td><p></p><div class="versionadded">
<p><span class="versionmodified added">New in version 1.4.0.</span></p>
</div>
<p></p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_add.html#pyspark.sql.functions.try_add" title="pyspark.sql.functions.try_add"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_add</span></code></a>(left,&nbsp;right)</p></td>
<td><p>Returns the sum of <cite>left`and `right</cite> and the result is null on overflow.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_avg.html#pyspark.sql.functions.try_avg" title="pyspark.sql.functions.try_avg"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_avg</span></code></a>(col)</p></td>
<td><p>Returns the mean calculated from values of a group and the result is null on overflow.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_divide.html#pyspark.sql.functions.try_divide" title="pyspark.sql.functions.try_divide"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_divide</span></code></a>(left,&nbsp;right)</p></td>
<td><p>Returns <cite>dividend</cite>/<cite>divisor</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_multiply.html#pyspark.sql.functions.try_multiply" title="pyspark.sql.functions.try_multiply"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_multiply</span></code></a>(left,&nbsp;right)</p></td>
<td><p>Returns <cite>left`*`right</cite> and the result is null on overflow.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_subtract.html#pyspark.sql.functions.try_subtract" title="pyspark.sql.functions.try_subtract"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_subtract</span></code></a>(left,&nbsp;right)</p></td>
<td><p>Returns <cite>left</cite>-<cite>right</cite> and the result is null on overflow.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_sum.html#pyspark.sql.functions.try_sum" title="pyspark.sql.functions.try_sum"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_sum</span></code></a>(col)</p></td>
<td><p>Returns the sum calculated from values of a group and the result is null on overflow.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_to_binary.html#pyspark.sql.functions.try_to_binary" title="pyspark.sql.functions.try_to_binary"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_to_binary</span></code></a>(col[,&nbsp;format])</p></td>
<td><p>This is a special version of <cite>to_binary</cite> that performs the same operation, but returns a NULL value instead of raising an error if the conversion cannot be performed.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_to_number.html#pyspark.sql.functions.try_to_number" title="pyspark.sql.functions.try_to_number"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_to_number</span></code></a>(col,&nbsp;format)</p></td>
<td><p>Convert string ‘col’ to a number based on the string format <cite>format</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.degrees.html#pyspark.sql.functions.degrees" title="pyspark.sql.functions.degrees"><code class="xref py py-obj docutils literal notranslate"><span class="pre">degrees</span></code></a>(col)</p></td>
<td><p>Converts an angle measured in radians to an approximately equivalent angle measured in degrees.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.toRadians.html#pyspark.sql.functions.toRadians" title="pyspark.sql.functions.toRadians"><code class="xref py py-obj docutils literal notranslate"><span class="pre">toRadians</span></code></a>(col)</p></td>
<td><p></p><div class="versionadded">
<p><span class="versionmodified added">New in version 1.4.0.</span></p>
</div>
<p></p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.radians.html#pyspark.sql.functions.radians" title="pyspark.sql.functions.radians"><code class="xref py py-obj docutils literal notranslate"><span class="pre">radians</span></code></a>(col)</p></td>
<td><p>Converts an angle measured in degrees to an approximately equivalent angle measured in radians.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.width_bucket.html#pyspark.sql.functions.width_bucket" title="pyspark.sql.functions.width_bucket"><code class="xref py py-obj docutils literal notranslate"><span class="pre">width_bucket</span></code></a>(v,&nbsp;min,&nbsp;max,&nbsp;numBucket)</p></td>
<td><p>Returns the bucket number into which the value of this expression would fall after being evaluated.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="datetime-functions">
<h2>Datetime Functions<a class="headerlink" href="#datetime-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.add_months.html#pyspark.sql.functions.add_months" title="pyspark.sql.functions.add_months"><code class="xref py py-obj docutils literal notranslate"><span class="pre">add_months</span></code></a>(start,&nbsp;months)</p></td>
<td><p>Returns the date that is <cite>months</cite> months after <cite>start</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.convert_timezone.html#pyspark.sql.functions.convert_timezone" title="pyspark.sql.functions.convert_timezone"><code class="xref py py-obj docutils literal notranslate"><span class="pre">convert_timezone</span></code></a>(sourceTz,&nbsp;targetTz,&nbsp;sourceTs)</p></td>
<td><p>Converts the timestamp without time zone <cite>sourceTs</cite> from the <cite>sourceTz</cite> time zone to <cite>targetTz</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.curdate.html#pyspark.sql.functions.curdate" title="pyspark.sql.functions.curdate"><code class="xref py py-obj docutils literal notranslate"><span class="pre">curdate</span></code></a>()</p></td>
<td><p>Returns the current date at the start of query evaluation as a <code class="xref py py-class docutils literal notranslate"><span class="pre">DateType</span></code> column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.current_date.html#pyspark.sql.functions.current_date" title="pyspark.sql.functions.current_date"><code class="xref py py-obj docutils literal notranslate"><span class="pre">current_date</span></code></a>()</p></td>
<td><p>Returns the current date at the start of query evaluation as a <code class="xref py py-class docutils literal notranslate"><span class="pre">DateType</span></code> column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.current_timestamp.html#pyspark.sql.functions.current_timestamp" title="pyspark.sql.functions.current_timestamp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">current_timestamp</span></code></a>()</p></td>
<td><p>Returns the current timestamp at the start of query evaluation as a <code class="xref py py-class docutils literal notranslate"><span class="pre">TimestampType</span></code> column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.current_timezone.html#pyspark.sql.functions.current_timezone" title="pyspark.sql.functions.current_timezone"><code class="xref py py-obj docutils literal notranslate"><span class="pre">current_timezone</span></code></a>()</p></td>
<td><p>Returns the current session local timezone.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.date_add.html#pyspark.sql.functions.date_add" title="pyspark.sql.functions.date_add"><code class="xref py py-obj docutils literal notranslate"><span class="pre">date_add</span></code></a>(start,&nbsp;days)</p></td>
<td><p>Returns the date that is <cite>days</cite> days after <cite>start</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.date_diff.html#pyspark.sql.functions.date_diff" title="pyspark.sql.functions.date_diff"><code class="xref py py-obj docutils literal notranslate"><span class="pre">date_diff</span></code></a>(end,&nbsp;start)</p></td>
<td><p>Returns the number of days from <cite>start</cite> to <cite>end</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.date_format.html#pyspark.sql.functions.date_format" title="pyspark.sql.functions.date_format"><code class="xref py py-obj docutils literal notranslate"><span class="pre">date_format</span></code></a>(date,&nbsp;format)</p></td>
<td><p>Converts a date/timestamp/string to a value of string in the format specified by the date format given by the second argument.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.date_from_unix_date.html#pyspark.sql.functions.date_from_unix_date" title="pyspark.sql.functions.date_from_unix_date"><code class="xref py py-obj docutils literal notranslate"><span class="pre">date_from_unix_date</span></code></a>(days)</p></td>
<td><p>Create date from the number of <cite>days</cite> since 1970-01-01.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.date_sub.html#pyspark.sql.functions.date_sub" title="pyspark.sql.functions.date_sub"><code class="xref py py-obj docutils literal notranslate"><span class="pre">date_sub</span></code></a>(start,&nbsp;days)</p></td>
<td><p>Returns the date that is <cite>days</cite> days before <cite>start</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.date_trunc.html#pyspark.sql.functions.date_trunc" title="pyspark.sql.functions.date_trunc"><code class="xref py py-obj docutils literal notranslate"><span class="pre">date_trunc</span></code></a>(format,&nbsp;timestamp)</p></td>
<td><p>Returns timestamp truncated to the unit specified by the format.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.dateadd.html#pyspark.sql.functions.dateadd" title="pyspark.sql.functions.dateadd"><code class="xref py py-obj docutils literal notranslate"><span class="pre">dateadd</span></code></a>(start,&nbsp;days)</p></td>
<td><p>Returns the date that is <cite>days</cite> days after <cite>start</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.datediff.html#pyspark.sql.functions.datediff" title="pyspark.sql.functions.datediff"><code class="xref py py-obj docutils literal notranslate"><span class="pre">datediff</span></code></a>(end,&nbsp;start)</p></td>
<td><p>Returns the number of days from <cite>start</cite> to <cite>end</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.day.html#pyspark.sql.functions.day" title="pyspark.sql.functions.day"><code class="xref py py-obj docutils literal notranslate"><span class="pre">day</span></code></a>(col)</p></td>
<td><p>Extract the day of the month of a given date/timestamp as integer.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.date_part.html#pyspark.sql.functions.date_part" title="pyspark.sql.functions.date_part"><code class="xref py py-obj docutils literal notranslate"><span class="pre">date_part</span></code></a>(field,&nbsp;source)</p></td>
<td><p>Extracts a part of the date/timestamp or interval source.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.datepart.html#pyspark.sql.functions.datepart" title="pyspark.sql.functions.datepart"><code class="xref py py-obj docutils literal notranslate"><span class="pre">datepart</span></code></a>(field,&nbsp;source)</p></td>
<td><p>Extracts a part of the date/timestamp or interval source.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.dayofmonth.html#pyspark.sql.functions.dayofmonth" title="pyspark.sql.functions.dayofmonth"><code class="xref py py-obj docutils literal notranslate"><span class="pre">dayofmonth</span></code></a>(col)</p></td>
<td><p>Extract the day of the month of a given date/timestamp as integer.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.dayofweek.html#pyspark.sql.functions.dayofweek" title="pyspark.sql.functions.dayofweek"><code class="xref py py-obj docutils literal notranslate"><span class="pre">dayofweek</span></code></a>(col)</p></td>
<td><p>Extract the day of the week of a given date/timestamp as integer.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.dayofyear.html#pyspark.sql.functions.dayofyear" title="pyspark.sql.functions.dayofyear"><code class="xref py py-obj docutils literal notranslate"><span class="pre">dayofyear</span></code></a>(col)</p></td>
<td><p>Extract the day of the year of a given date/timestamp as integer.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.extract.html#pyspark.sql.functions.extract" title="pyspark.sql.functions.extract"><code class="xref py py-obj docutils literal notranslate"><span class="pre">extract</span></code></a>(field,&nbsp;source)</p></td>
<td><p>Extracts a part of the date/timestamp or interval source.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.second.html#pyspark.sql.functions.second" title="pyspark.sql.functions.second"><code class="xref py py-obj docutils literal notranslate"><span class="pre">second</span></code></a>(col)</p></td>
<td><p>Extract the seconds of a given date as integer.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.weekofyear.html#pyspark.sql.functions.weekofyear" title="pyspark.sql.functions.weekofyear"><code class="xref py py-obj docutils literal notranslate"><span class="pre">weekofyear</span></code></a>(col)</p></td>
<td><p>Extract the week number of a given date as integer.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.year.html#pyspark.sql.functions.year" title="pyspark.sql.functions.year"><code class="xref py py-obj docutils literal notranslate"><span class="pre">year</span></code></a>(col)</p></td>
<td><p>Extract the year of a given date/timestamp as integer.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.quarter.html#pyspark.sql.functions.quarter" title="pyspark.sql.functions.quarter"><code class="xref py py-obj docutils literal notranslate"><span class="pre">quarter</span></code></a>(col)</p></td>
<td><p>Extract the quarter of a given date/timestamp as integer.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.month.html#pyspark.sql.functions.month" title="pyspark.sql.functions.month"><code class="xref py py-obj docutils literal notranslate"><span class="pre">month</span></code></a>(col)</p></td>
<td><p>Extract the month of a given date/timestamp as integer.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.last_day.html#pyspark.sql.functions.last_day" title="pyspark.sql.functions.last_day"><code class="xref py py-obj docutils literal notranslate"><span class="pre">last_day</span></code></a>(date)</p></td>
<td><p>Returns the last day of the month which the given date belongs to.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.localtimestamp.html#pyspark.sql.functions.localtimestamp" title="pyspark.sql.functions.localtimestamp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">localtimestamp</span></code></a>()</p></td>
<td><p>Returns the current timestamp without time zone at the start of query evaluation as a timestamp without time zone column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.make_dt_interval.html#pyspark.sql.functions.make_dt_interval" title="pyspark.sql.functions.make_dt_interval"><code class="xref py py-obj docutils literal notranslate"><span class="pre">make_dt_interval</span></code></a>([days,&nbsp;hours,&nbsp;mins,&nbsp;secs])</p></td>
<td><p>Make DayTimeIntervalType duration from days, hours, mins and secs.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.make_interval.html#pyspark.sql.functions.make_interval" title="pyspark.sql.functions.make_interval"><code class="xref py py-obj docutils literal notranslate"><span class="pre">make_interval</span></code></a>([years,&nbsp;months,&nbsp;weeks,&nbsp;days,&nbsp;…])</p></td>
<td><p>Make interval from years, months, weeks, days, hours, mins and secs.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.make_timestamp.html#pyspark.sql.functions.make_timestamp" title="pyspark.sql.functions.make_timestamp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">make_timestamp</span></code></a>(years,&nbsp;months,&nbsp;days,&nbsp;hours,&nbsp;…)</p></td>
<td><p>Create timestamp from years, months, days, hours, mins, secs and timezone fields.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.make_timestamp_ltz.html#pyspark.sql.functions.make_timestamp_ltz" title="pyspark.sql.functions.make_timestamp_ltz"><code class="xref py py-obj docutils literal notranslate"><span class="pre">make_timestamp_ltz</span></code></a>(years,&nbsp;months,&nbsp;days,&nbsp;…)</p></td>
<td><p>Create the current timestamp with local time zone from years, months, days, hours, mins, secs and timezone fields.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.make_timestamp_ntz.html#pyspark.sql.functions.make_timestamp_ntz" title="pyspark.sql.functions.make_timestamp_ntz"><code class="xref py py-obj docutils literal notranslate"><span class="pre">make_timestamp_ntz</span></code></a>(years,&nbsp;months,&nbsp;days,&nbsp;…)</p></td>
<td><p>Create local date-time from years, months, days, hours, mins, secs fields.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.make_ym_interval.html#pyspark.sql.functions.make_ym_interval" title="pyspark.sql.functions.make_ym_interval"><code class="xref py py-obj docutils literal notranslate"><span class="pre">make_ym_interval</span></code></a>([years,&nbsp;months])</p></td>
<td><p>Make year-month interval from years, months.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.minute.html#pyspark.sql.functions.minute" title="pyspark.sql.functions.minute"><code class="xref py py-obj docutils literal notranslate"><span class="pre">minute</span></code></a>(col)</p></td>
<td><p>Extract the minutes of a given timestamp as integer.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.months_between.html#pyspark.sql.functions.months_between" title="pyspark.sql.functions.months_between"><code class="xref py py-obj docutils literal notranslate"><span class="pre">months_between</span></code></a>(date1,&nbsp;date2[,&nbsp;roundOff])</p></td>
<td><p>Returns number of months between dates date1 and date2.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.next_day.html#pyspark.sql.functions.next_day" title="pyspark.sql.functions.next_day"><code class="xref py py-obj docutils literal notranslate"><span class="pre">next_day</span></code></a>(date,&nbsp;dayOfWeek)</p></td>
<td><p>Returns the first date which is later than the value of the date column based on second <cite>week day</cite> argument.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.hour.html#pyspark.sql.functions.hour" title="pyspark.sql.functions.hour"><code class="xref py py-obj docutils literal notranslate"><span class="pre">hour</span></code></a>(col)</p></td>
<td><p>Extract the hours of a given timestamp as integer.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.make_date.html#pyspark.sql.functions.make_date" title="pyspark.sql.functions.make_date"><code class="xref py py-obj docutils literal notranslate"><span class="pre">make_date</span></code></a>(year,&nbsp;month,&nbsp;day)</p></td>
<td><p>Returns a column with a date built from the year, month and day columns.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.now.html#pyspark.sql.functions.now" title="pyspark.sql.functions.now"><code class="xref py py-obj docutils literal notranslate"><span class="pre">now</span></code></a>()</p></td>
<td><p>Returns the current timestamp at the start of query evaluation.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.from_unixtime.html#pyspark.sql.functions.from_unixtime" title="pyspark.sql.functions.from_unixtime"><code class="xref py py-obj docutils literal notranslate"><span class="pre">from_unixtime</span></code></a>(timestamp[,&nbsp;format])</p></td>
<td><p>Converts the number of seconds from unix epoch (1970-01-01 00:00:00 UTC) to a string representing the timestamp of that moment in the current system time zone in the given format.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.unix_timestamp.html#pyspark.sql.functions.unix_timestamp" title="pyspark.sql.functions.unix_timestamp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">unix_timestamp</span></code></a>([timestamp,&nbsp;format])</p></td>
<td><p>Convert time string with given pattern (‘yyyy-MM-dd HH:mm:ss’, by default) to Unix time stamp (in seconds), using the default timezone and the default locale, returns null if failed.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_unix_timestamp.html#pyspark.sql.functions.to_unix_timestamp" title="pyspark.sql.functions.to_unix_timestamp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_unix_timestamp</span></code></a>(timestamp[,&nbsp;format])</p></td>
<td><p>Returns the UNIX timestamp of the given time.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_timestamp.html#pyspark.sql.functions.to_timestamp" title="pyspark.sql.functions.to_timestamp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_timestamp</span></code></a>(col[,&nbsp;format])</p></td>
<td><p>Converts a <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> into <a class="reference internal" href="api/pyspark.sql.types.TimestampType.html#pyspark.sql.types.TimestampType" title="pyspark.sql.types.TimestampType"><code class="xref py py-class docutils literal notranslate"><span class="pre">pyspark.sql.types.TimestampType</span></code></a> using the optionally specified format.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_timestamp_ltz.html#pyspark.sql.functions.to_timestamp_ltz" title="pyspark.sql.functions.to_timestamp_ltz"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_timestamp_ltz</span></code></a>(timestamp[,&nbsp;format])</p></td>
<td><p>Parses the <cite>timestamp</cite> with the <cite>format</cite> to a timestamp without time zone.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_timestamp_ntz.html#pyspark.sql.functions.to_timestamp_ntz" title="pyspark.sql.functions.to_timestamp_ntz"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_timestamp_ntz</span></code></a>(timestamp[,&nbsp;format])</p></td>
<td><p>Parses the <cite>timestamp</cite> with the <cite>format</cite> to a timestamp without time zone.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_date.html#pyspark.sql.functions.to_date" title="pyspark.sql.functions.to_date"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_date</span></code></a>(col[,&nbsp;format])</p></td>
<td><p>Converts a <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> into <a class="reference internal" href="api/pyspark.sql.types.DateType.html#pyspark.sql.types.DateType" title="pyspark.sql.types.DateType"><code class="xref py py-class docutils literal notranslate"><span class="pre">pyspark.sql.types.DateType</span></code></a> using the optionally specified format.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.trunc.html#pyspark.sql.functions.trunc" title="pyspark.sql.functions.trunc"><code class="xref py py-obj docutils literal notranslate"><span class="pre">trunc</span></code></a>(date,&nbsp;format)</p></td>
<td><p>Returns date truncated to the unit specified by the format.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.from_utc_timestamp.html#pyspark.sql.functions.from_utc_timestamp" title="pyspark.sql.functions.from_utc_timestamp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">from_utc_timestamp</span></code></a>(timestamp,&nbsp;tz)</p></td>
<td><p>This is a common function for databases supporting TIMESTAMP WITHOUT TIMEZONE.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_utc_timestamp.html#pyspark.sql.functions.to_utc_timestamp" title="pyspark.sql.functions.to_utc_timestamp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_utc_timestamp</span></code></a>(timestamp,&nbsp;tz)</p></td>
<td><p>This is a common function for databases supporting TIMESTAMP WITHOUT TIMEZONE.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.weekday.html#pyspark.sql.functions.weekday" title="pyspark.sql.functions.weekday"><code class="xref py py-obj docutils literal notranslate"><span class="pre">weekday</span></code></a>(col)</p></td>
<td><p>Returns the day of the week for date/timestamp (0 = Monday, 1 = Tuesday, …, 6 = Sunday).</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.window.html#pyspark.sql.functions.window" title="pyspark.sql.functions.window"><code class="xref py py-obj docutils literal notranslate"><span class="pre">window</span></code></a>(timeColumn,&nbsp;windowDuration[,&nbsp;…])</p></td>
<td><p>Bucketize rows into one or more time windows given a timestamp specifying column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.session_window.html#pyspark.sql.functions.session_window" title="pyspark.sql.functions.session_window"><code class="xref py py-obj docutils literal notranslate"><span class="pre">session_window</span></code></a>(timeColumn,&nbsp;gapDuration)</p></td>
<td><p>Generates session window given a timestamp specifying column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.timestamp_micros.html#pyspark.sql.functions.timestamp_micros" title="pyspark.sql.functions.timestamp_micros"><code class="xref py py-obj docutils literal notranslate"><span class="pre">timestamp_micros</span></code></a>(col)</p></td>
<td><p>Creates timestamp from the number of microseconds since UTC epoch.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.timestamp_millis.html#pyspark.sql.functions.timestamp_millis" title="pyspark.sql.functions.timestamp_millis"><code class="xref py py-obj docutils literal notranslate"><span class="pre">timestamp_millis</span></code></a>(col)</p></td>
<td><p>Creates timestamp from the number of milliseconds since UTC epoch.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.timestamp_seconds.html#pyspark.sql.functions.timestamp_seconds" title="pyspark.sql.functions.timestamp_seconds"><code class="xref py py-obj docutils literal notranslate"><span class="pre">timestamp_seconds</span></code></a>(col)</p></td>
<td><p>Converts the number of seconds from the Unix epoch (1970-01-01T00:00:00Z) to a timestamp.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_to_timestamp.html#pyspark.sql.functions.try_to_timestamp" title="pyspark.sql.functions.try_to_timestamp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_to_timestamp</span></code></a>(col[,&nbsp;format])</p></td>
<td><p>Parses the <cite>col</cite> with the <cite>format</cite> to a timestamp.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.unix_date.html#pyspark.sql.functions.unix_date" title="pyspark.sql.functions.unix_date"><code class="xref py py-obj docutils literal notranslate"><span class="pre">unix_date</span></code></a>(col)</p></td>
<td><p>Returns the number of days since 1970-01-01.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.unix_micros.html#pyspark.sql.functions.unix_micros" title="pyspark.sql.functions.unix_micros"><code class="xref py py-obj docutils literal notranslate"><span class="pre">unix_micros</span></code></a>(col)</p></td>
<td><p>Returns the number of microseconds since 1970-01-01 00:00:00 UTC.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.unix_millis.html#pyspark.sql.functions.unix_millis" title="pyspark.sql.functions.unix_millis"><code class="xref py py-obj docutils literal notranslate"><span class="pre">unix_millis</span></code></a>(col)</p></td>
<td><p>Returns the number of milliseconds since 1970-01-01 00:00:00 UTC.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.unix_seconds.html#pyspark.sql.functions.unix_seconds" title="pyspark.sql.functions.unix_seconds"><code class="xref py py-obj docutils literal notranslate"><span class="pre">unix_seconds</span></code></a>(col)</p></td>
<td><p>Returns the number of seconds since 1970-01-01 00:00:00 UTC.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.window_time.html#pyspark.sql.functions.window_time" title="pyspark.sql.functions.window_time"><code class="xref py py-obj docutils literal notranslate"><span class="pre">window_time</span></code></a>(windowColumn)</p></td>
<td><p>Computes the event time from a window column.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="collection-functions">
<h2>Collection Functions<a class="headerlink" href="#collection-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array.html#pyspark.sql.functions.array" title="pyspark.sql.functions.array"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array</span></code></a>(*cols)</p></td>
<td><p>Creates a new array column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_contains.html#pyspark.sql.functions.array_contains" title="pyspark.sql.functions.array_contains"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_contains</span></code></a>(col,&nbsp;value)</p></td>
<td><p>Collection function: returns null if the array is null, true if the array contains the given value, and false otherwise.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.arrays_overlap.html#pyspark.sql.functions.arrays_overlap" title="pyspark.sql.functions.arrays_overlap"><code class="xref py py-obj docutils literal notranslate"><span class="pre">arrays_overlap</span></code></a>(a1,&nbsp;a2)</p></td>
<td><p>Collection function: returns true if the arrays contain any common non-null element; if not, returns null if both the arrays are non-empty and any of them contains a null element; returns false otherwise.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_join.html#pyspark.sql.functions.array_join" title="pyspark.sql.functions.array_join"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_join</span></code></a>(col,&nbsp;delimiter[,&nbsp;null_replacement])</p></td>
<td><p>Concatenates the elements of <cite>column</cite> using the <cite>delimiter</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.create_map.html#pyspark.sql.functions.create_map" title="pyspark.sql.functions.create_map"><code class="xref py py-obj docutils literal notranslate"><span class="pre">create_map</span></code></a>(*cols)</p></td>
<td><p>Creates a new map column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.slice.html#pyspark.sql.functions.slice" title="pyspark.sql.functions.slice"><code class="xref py py-obj docutils literal notranslate"><span class="pre">slice</span></code></a>(x,&nbsp;start,&nbsp;length)</p></td>
<td><p>Collection function: returns an array containing all the elements in <cite>x</cite> from index <cite>start</cite> (array indices start at 1, or from the end if <cite>start</cite> is negative) with the specified <cite>length</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.concat.html#pyspark.sql.functions.concat" title="pyspark.sql.functions.concat"><code class="xref py py-obj docutils literal notranslate"><span class="pre">concat</span></code></a>(*cols)</p></td>
<td><p>Concatenates multiple input columns together into a single column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_position.html#pyspark.sql.functions.array_position" title="pyspark.sql.functions.array_position"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_position</span></code></a>(col,&nbsp;value)</p></td>
<td><p>Collection function: Locates the position of the first occurrence of the given value in the given array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.element_at.html#pyspark.sql.functions.element_at" title="pyspark.sql.functions.element_at"><code class="xref py py-obj docutils literal notranslate"><span class="pre">element_at</span></code></a>(col,&nbsp;extraction)</p></td>
<td><p>Collection function: Returns element of array at given index in <cite>extraction</cite> if col is array.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_append.html#pyspark.sql.functions.array_append" title="pyspark.sql.functions.array_append"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_append</span></code></a>(col,&nbsp;value)</p></td>
<td><p>Collection function: returns an array of the elements in col1 along with the added element in col2 at the last of the array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_size.html#pyspark.sql.functions.array_size" title="pyspark.sql.functions.array_size"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_size</span></code></a>(col)</p></td>
<td><p>Returns the total number of elements in the array.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_sort.html#pyspark.sql.functions.array_sort" title="pyspark.sql.functions.array_sort"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_sort</span></code></a>(col[,&nbsp;comparator])</p></td>
<td><p>Collection function: sorts the input array in ascending order.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_insert.html#pyspark.sql.functions.array_insert" title="pyspark.sql.functions.array_insert"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_insert</span></code></a>(arr,&nbsp;pos,&nbsp;value)</p></td>
<td><p>Collection function: adds an item into a given array at a specified array index.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_remove.html#pyspark.sql.functions.array_remove" title="pyspark.sql.functions.array_remove"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_remove</span></code></a>(col,&nbsp;element)</p></td>
<td><p>Collection function: Remove all elements that equal to element from the given array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_prepend.html#pyspark.sql.functions.array_prepend" title="pyspark.sql.functions.array_prepend"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_prepend</span></code></a>(col,&nbsp;value)</p></td>
<td><p>Collection function: Returns an array containing element as well as all elements from array.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_distinct.html#pyspark.sql.functions.array_distinct" title="pyspark.sql.functions.array_distinct"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_distinct</span></code></a>(col)</p></td>
<td><p>Collection function: removes duplicate values from the array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_intersect.html#pyspark.sql.functions.array_intersect" title="pyspark.sql.functions.array_intersect"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_intersect</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Collection function: returns an array of the elements in the intersection of col1 and col2, without duplicates.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_union.html#pyspark.sql.functions.array_union" title="pyspark.sql.functions.array_union"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_union</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Collection function: returns an array of the elements in the union of col1 and col2, without duplicates.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_except.html#pyspark.sql.functions.array_except" title="pyspark.sql.functions.array_except"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_except</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Collection function: returns an array of the elements in col1 but not in col2, without duplicates.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_compact.html#pyspark.sql.functions.array_compact" title="pyspark.sql.functions.array_compact"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_compact</span></code></a>(col)</p></td>
<td><p>Collection function: removes null values from the array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.transform.html#pyspark.sql.functions.transform" title="pyspark.sql.functions.transform"><code class="xref py py-obj docutils literal notranslate"><span class="pre">transform</span></code></a>(col,&nbsp;f)</p></td>
<td><p>Returns an array of elements after applying a transformation to each element in the input array.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.exists.html#pyspark.sql.functions.exists" title="pyspark.sql.functions.exists"><code class="xref py py-obj docutils literal notranslate"><span class="pre">exists</span></code></a>(col,&nbsp;f)</p></td>
<td><p>Returns whether a predicate holds for one or more elements in the array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.forall.html#pyspark.sql.functions.forall" title="pyspark.sql.functions.forall"><code class="xref py py-obj docutils literal notranslate"><span class="pre">forall</span></code></a>(col,&nbsp;f)</p></td>
<td><p>Returns whether a predicate holds for every element in the array.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.filter.html#pyspark.sql.functions.filter" title="pyspark.sql.functions.filter"><code class="xref py py-obj docutils literal notranslate"><span class="pre">filter</span></code></a>(col,&nbsp;f)</p></td>
<td><p>Returns an array of elements for which a predicate holds in a given array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.aggregate.html#pyspark.sql.functions.aggregate" title="pyspark.sql.functions.aggregate"><code class="xref py py-obj docutils literal notranslate"><span class="pre">aggregate</span></code></a>(col,&nbsp;initialValue,&nbsp;merge[,&nbsp;finish])</p></td>
<td><p>Applies a binary operator to an initial state and all elements in the array, and reduces this to a single state.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.zip_with.html#pyspark.sql.functions.zip_with" title="pyspark.sql.functions.zip_with"><code class="xref py py-obj docutils literal notranslate"><span class="pre">zip_with</span></code></a>(left,&nbsp;right,&nbsp;f)</p></td>
<td><p>Merge two given arrays, element-wise, into a single array using a function.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.transform_keys.html#pyspark.sql.functions.transform_keys" title="pyspark.sql.functions.transform_keys"><code class="xref py py-obj docutils literal notranslate"><span class="pre">transform_keys</span></code></a>(col,&nbsp;f)</p></td>
<td><p>Applies a function to every key-value pair in a map and returns a map with the results of those applications as the new keys for the pairs.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.transform_values.html#pyspark.sql.functions.transform_values" title="pyspark.sql.functions.transform_values"><code class="xref py py-obj docutils literal notranslate"><span class="pre">transform_values</span></code></a>(col,&nbsp;f)</p></td>
<td><p>Applies a function to every key-value pair in a map and returns a map with the results of those applications as the new values for the pairs.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.map_filter.html#pyspark.sql.functions.map_filter" title="pyspark.sql.functions.map_filter"><code class="xref py py-obj docutils literal notranslate"><span class="pre">map_filter</span></code></a>(col,&nbsp;f)</p></td>
<td><p>Returns a map whose key-value pairs satisfy a predicate.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.map_from_arrays.html#pyspark.sql.functions.map_from_arrays" title="pyspark.sql.functions.map_from_arrays"><code class="xref py py-obj docutils literal notranslate"><span class="pre">map_from_arrays</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Creates a new map from two arrays.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.map_zip_with.html#pyspark.sql.functions.map_zip_with" title="pyspark.sql.functions.map_zip_with"><code class="xref py py-obj docutils literal notranslate"><span class="pre">map_zip_with</span></code></a>(col1,&nbsp;col2,&nbsp;f)</p></td>
<td><p>Merge two given maps, key-wise into a single map using a function.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.explode.html#pyspark.sql.functions.explode" title="pyspark.sql.functions.explode"><code class="xref py py-obj docutils literal notranslate"><span class="pre">explode</span></code></a>(col)</p></td>
<td><p>Returns a new row for each element in the given array or map.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.explode_outer.html#pyspark.sql.functions.explode_outer" title="pyspark.sql.functions.explode_outer"><code class="xref py py-obj docutils literal notranslate"><span class="pre">explode_outer</span></code></a>(col)</p></td>
<td><p>Returns a new row for each element in the given array or map.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.posexplode.html#pyspark.sql.functions.posexplode" title="pyspark.sql.functions.posexplode"><code class="xref py py-obj docutils literal notranslate"><span class="pre">posexplode</span></code></a>(col)</p></td>
<td><p>Returns a new row for each element with position in the given array or map.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.posexplode_outer.html#pyspark.sql.functions.posexplode_outer" title="pyspark.sql.functions.posexplode_outer"><code class="xref py py-obj docutils literal notranslate"><span class="pre">posexplode_outer</span></code></a>(col)</p></td>
<td><p>Returns a new row for each element with position in the given array or map.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.inline.html#pyspark.sql.functions.inline" title="pyspark.sql.functions.inline"><code class="xref py py-obj docutils literal notranslate"><span class="pre">inline</span></code></a>(col)</p></td>
<td><p>Explodes an array of structs into a table.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.inline_outer.html#pyspark.sql.functions.inline_outer" title="pyspark.sql.functions.inline_outer"><code class="xref py py-obj docutils literal notranslate"><span class="pre">inline_outer</span></code></a>(col)</p></td>
<td><p>Explodes an array of structs into a table.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.get.html#pyspark.sql.functions.get" title="pyspark.sql.functions.get"><code class="xref py py-obj docutils literal notranslate"><span class="pre">get</span></code></a>(col,&nbsp;index)</p></td>
<td><p>Collection function: Returns element of array at given (0-based) index.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.get_json_object.html#pyspark.sql.functions.get_json_object" title="pyspark.sql.functions.get_json_object"><code class="xref py py-obj docutils literal notranslate"><span class="pre">get_json_object</span></code></a>(col,&nbsp;path)</p></td>
<td><p>Extracts json object from a json string based on json <cite>path</cite> specified, and returns json string of the extracted json object.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.json_tuple.html#pyspark.sql.functions.json_tuple" title="pyspark.sql.functions.json_tuple"><code class="xref py py-obj docutils literal notranslate"><span class="pre">json_tuple</span></code></a>(col,&nbsp;*fields)</p></td>
<td><p>Creates a new row for a json column according to the given field names.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.from_json.html#pyspark.sql.functions.from_json" title="pyspark.sql.functions.from_json"><code class="xref py py-obj docutils literal notranslate"><span class="pre">from_json</span></code></a>(col,&nbsp;schema[,&nbsp;options])</p></td>
<td><p>Parses a column containing a JSON string into a <code class="xref py py-class docutils literal notranslate"><span class="pre">MapType</span></code> with <code class="xref py py-class docutils literal notranslate"><span class="pre">StringType</span></code> as keys type, <code class="xref py py-class docutils literal notranslate"><span class="pre">StructType</span></code> or <code class="xref py py-class docutils literal notranslate"><span class="pre">ArrayType</span></code> with the specified schema.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.schema_of_json.html#pyspark.sql.functions.schema_of_json" title="pyspark.sql.functions.schema_of_json"><code class="xref py py-obj docutils literal notranslate"><span class="pre">schema_of_json</span></code></a>(json[,&nbsp;options])</p></td>
<td><p>Parses a JSON string and infers its schema in DDL format.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_json.html#pyspark.sql.functions.to_json" title="pyspark.sql.functions.to_json"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_json</span></code></a>(col[,&nbsp;options])</p></td>
<td><p>Converts a column containing a <code class="xref py py-class docutils literal notranslate"><span class="pre">StructType</span></code>, <code class="xref py py-class docutils literal notranslate"><span class="pre">ArrayType</span></code> or a <code class="xref py py-class docutils literal notranslate"><span class="pre">MapType</span></code> into a JSON string.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.json_array_length.html#pyspark.sql.functions.json_array_length" title="pyspark.sql.functions.json_array_length"><code class="xref py py-obj docutils literal notranslate"><span class="pre">json_array_length</span></code></a>(col)</p></td>
<td><p>Returns the number of elements in the outermost JSON array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.json_object_keys.html#pyspark.sql.functions.json_object_keys" title="pyspark.sql.functions.json_object_keys"><code class="xref py py-obj docutils literal notranslate"><span class="pre">json_object_keys</span></code></a>(col)</p></td>
<td><p>Returns all the keys of the outermost JSON object as an array.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.size.html#pyspark.sql.functions.size" title="pyspark.sql.functions.size"><code class="xref py py-obj docutils literal notranslate"><span class="pre">size</span></code></a>(col)</p></td>
<td><p>Collection function: returns the length of the array or map stored in the column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.cardinality.html#pyspark.sql.functions.cardinality" title="pyspark.sql.functions.cardinality"><code class="xref py py-obj docutils literal notranslate"><span class="pre">cardinality</span></code></a>(col)</p></td>
<td><p>Collection function: returns the length of the array or map stored in the column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.struct.html#pyspark.sql.functions.struct" title="pyspark.sql.functions.struct"><code class="xref py py-obj docutils literal notranslate"><span class="pre">struct</span></code></a>(*cols)</p></td>
<td><p>Creates a new struct column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sort_array.html#pyspark.sql.functions.sort_array" title="pyspark.sql.functions.sort_array"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sort_array</span></code></a>(col[,&nbsp;asc])</p></td>
<td><p>Collection function: sorts the input array in ascending or descending order according to the natural ordering of the array elements.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_max.html#pyspark.sql.functions.array_max" title="pyspark.sql.functions.array_max"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_max</span></code></a>(col)</p></td>
<td><p>Collection function: returns the maximum value of the array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_min.html#pyspark.sql.functions.array_min" title="pyspark.sql.functions.array_min"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_min</span></code></a>(col)</p></td>
<td><p>Collection function: returns the minimum value of the array.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.shuffle.html#pyspark.sql.functions.shuffle" title="pyspark.sql.functions.shuffle"><code class="xref py py-obj docutils literal notranslate"><span class="pre">shuffle</span></code></a>(col)</p></td>
<td><p>Collection function: Generates a random permutation of the given array.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.reverse.html#pyspark.sql.functions.reverse" title="pyspark.sql.functions.reverse"><code class="xref py py-obj docutils literal notranslate"><span class="pre">reverse</span></code></a>(col)</p></td>
<td><p>Collection function: returns a reversed string or an array with reverse order of elements.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.flatten.html#pyspark.sql.functions.flatten" title="pyspark.sql.functions.flatten"><code class="xref py py-obj docutils literal notranslate"><span class="pre">flatten</span></code></a>(col)</p></td>
<td><p>Collection function: creates a single array from an array of arrays.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sequence.html#pyspark.sql.functions.sequence" title="pyspark.sql.functions.sequence"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sequence</span></code></a>(start,&nbsp;stop[,&nbsp;step])</p></td>
<td><p>Generate a sequence of integers from <cite>start</cite> to <cite>stop</cite>, incrementing by <cite>step</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_repeat.html#pyspark.sql.functions.array_repeat" title="pyspark.sql.functions.array_repeat"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_repeat</span></code></a>(col,&nbsp;count)</p></td>
<td><p>Collection function: creates an array containing a column repeated count times.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.map_contains_key.html#pyspark.sql.functions.map_contains_key" title="pyspark.sql.functions.map_contains_key"><code class="xref py py-obj docutils literal notranslate"><span class="pre">map_contains_key</span></code></a>(col,&nbsp;value)</p></td>
<td><p>Returns true if the map contains the key.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.map_keys.html#pyspark.sql.functions.map_keys" title="pyspark.sql.functions.map_keys"><code class="xref py py-obj docutils literal notranslate"><span class="pre">map_keys</span></code></a>(col)</p></td>
<td><p>Collection function: Returns an unordered array containing the keys of the map.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.map_values.html#pyspark.sql.functions.map_values" title="pyspark.sql.functions.map_values"><code class="xref py py-obj docutils literal notranslate"><span class="pre">map_values</span></code></a>(col)</p></td>
<td><p>Collection function: Returns an unordered array containing the values of the map.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.map_entries.html#pyspark.sql.functions.map_entries" title="pyspark.sql.functions.map_entries"><code class="xref py py-obj docutils literal notranslate"><span class="pre">map_entries</span></code></a>(col)</p></td>
<td><p>Collection function: Returns an unordered array of all entries in the given map.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.map_from_entries.html#pyspark.sql.functions.map_from_entries" title="pyspark.sql.functions.map_from_entries"><code class="xref py py-obj docutils literal notranslate"><span class="pre">map_from_entries</span></code></a>(col)</p></td>
<td><p>Collection function: Converts an array of entries (key value struct types) to a map of values.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.arrays_zip.html#pyspark.sql.functions.arrays_zip" title="pyspark.sql.functions.arrays_zip"><code class="xref py py-obj docutils literal notranslate"><span class="pre">arrays_zip</span></code></a>(*cols)</p></td>
<td><p>Collection function: Returns a merged array of structs in which the N-th struct contains all N-th values of input arrays.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.map_concat.html#pyspark.sql.functions.map_concat" title="pyspark.sql.functions.map_concat"><code class="xref py py-obj docutils literal notranslate"><span class="pre">map_concat</span></code></a>(*cols)</p></td>
<td><p>Returns the union of all the given maps.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.from_csv.html#pyspark.sql.functions.from_csv" title="pyspark.sql.functions.from_csv"><code class="xref py py-obj docutils literal notranslate"><span class="pre">from_csv</span></code></a>(col,&nbsp;schema[,&nbsp;options])</p></td>
<td><p>Parses a column containing a CSV string to a row with the specified schema.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.schema_of_csv.html#pyspark.sql.functions.schema_of_csv" title="pyspark.sql.functions.schema_of_csv"><code class="xref py py-obj docutils literal notranslate"><span class="pre">schema_of_csv</span></code></a>(csv[,&nbsp;options])</p></td>
<td><p>Parses a CSV string and infers its schema in DDL format.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.str_to_map.html#pyspark.sql.functions.str_to_map" title="pyspark.sql.functions.str_to_map"><code class="xref py py-obj docutils literal notranslate"><span class="pre">str_to_map</span></code></a>(text[,&nbsp;pairDelim,&nbsp;keyValueDelim])</p></td>
<td><p>Creates a map after splitting the text into key/value pairs using delimiters.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_csv.html#pyspark.sql.functions.to_csv" title="pyspark.sql.functions.to_csv"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_csv</span></code></a>(col[,&nbsp;options])</p></td>
<td><p>Converts a column containing a <code class="xref py py-class docutils literal notranslate"><span class="pre">StructType</span></code> into a CSV string.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_element_at.html#pyspark.sql.functions.try_element_at" title="pyspark.sql.functions.try_element_at"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_element_at</span></code></a>(col,&nbsp;extraction)</p></td>
<td><p>(array, index) - Returns element of array at given (1-based) index.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="partition-transformation-functions">
<h2>Partition Transformation Functions<a class="headerlink" href="#partition-transformation-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.years.html#pyspark.sql.functions.years" title="pyspark.sql.functions.years"><code class="xref py py-obj docutils literal notranslate"><span class="pre">years</span></code></a>(col)</p></td>
<td><p>Partition transform function: A transform for timestamps and dates to partition data into years.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.months.html#pyspark.sql.functions.months" title="pyspark.sql.functions.months"><code class="xref py py-obj docutils literal notranslate"><span class="pre">months</span></code></a>(col)</p></td>
<td><p>Partition transform function: A transform for timestamps and dates to partition data into months.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.days.html#pyspark.sql.functions.days" title="pyspark.sql.functions.days"><code class="xref py py-obj docutils literal notranslate"><span class="pre">days</span></code></a>(col)</p></td>
<td><p>Partition transform function: A transform for timestamps and dates to partition data into days.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.hours.html#pyspark.sql.functions.hours" title="pyspark.sql.functions.hours"><code class="xref py py-obj docutils literal notranslate"><span class="pre">hours</span></code></a>(col)</p></td>
<td><p>Partition transform function: A transform for timestamps to partition data into hours.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bucket.html#pyspark.sql.functions.bucket" title="pyspark.sql.functions.bucket"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bucket</span></code></a>(numBuckets,&nbsp;col)</p></td>
<td><p>Partition transform function: A transform for any type that partitions by a hash of the input column.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="aggregate-functions">
<h2>Aggregate Functions<a class="headerlink" href="#aggregate-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.any_value.html#pyspark.sql.functions.any_value" title="pyspark.sql.functions.any_value"><code class="xref py py-obj docutils literal notranslate"><span class="pre">any_value</span></code></a>(col[,&nbsp;ignoreNulls])</p></td>
<td><p>Returns some value of <cite>col</cite> for a group of rows.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.approxCountDistinct.html#pyspark.sql.functions.approxCountDistinct" title="pyspark.sql.functions.approxCountDistinct"><code class="xref py py-obj docutils literal notranslate"><span class="pre">approxCountDistinct</span></code></a>(col[,&nbsp;rsd])</p></td>
<td><p></p><div class="versionadded">
<p><span class="versionmodified added">New in version 1.3.0.</span></p>
</div>
<p></p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.approx_count_distinct.html#pyspark.sql.functions.approx_count_distinct" title="pyspark.sql.functions.approx_count_distinct"><code class="xref py py-obj docutils literal notranslate"><span class="pre">approx_count_distinct</span></code></a>(col[,&nbsp;rsd])</p></td>
<td><p>Aggregate function: returns a new <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> for approximate distinct count of column <cite>col</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.approx_percentile.html#pyspark.sql.functions.approx_percentile" title="pyspark.sql.functions.approx_percentile"><code class="xref py py-obj docutils literal notranslate"><span class="pre">approx_percentile</span></code></a>(col,&nbsp;percentage[,&nbsp;accuracy])</p></td>
<td><p>Returns the approximate <cite>percentile</cite> of the numeric column <cite>col</cite> which is the smallest value in the ordered <cite>col</cite> values (sorted from least to greatest) such that no more than <cite>percentage</cite> of <cite>col</cite> values is less than the value or equal to that value.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.array_agg.html#pyspark.sql.functions.array_agg" title="pyspark.sql.functions.array_agg"><code class="xref py py-obj docutils literal notranslate"><span class="pre">array_agg</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns a list of objects with duplicates.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.avg.html#pyspark.sql.functions.avg" title="pyspark.sql.functions.avg"><code class="xref py py-obj docutils literal notranslate"><span class="pre">avg</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the average of the values in a group.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bit_and.html#pyspark.sql.functions.bit_and" title="pyspark.sql.functions.bit_and"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bit_and</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the bitwise AND of all non-null input values, or null if none.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bit_or.html#pyspark.sql.functions.bit_or" title="pyspark.sql.functions.bit_or"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bit_or</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the bitwise OR of all non-null input values, or null if none.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bit_xor.html#pyspark.sql.functions.bit_xor" title="pyspark.sql.functions.bit_xor"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bit_xor</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the bitwise XOR of all non-null input values, or null if none.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bool_and.html#pyspark.sql.functions.bool_and" title="pyspark.sql.functions.bool_and"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bool_and</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns true if all values of <cite>col</cite> are true.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bool_or.html#pyspark.sql.functions.bool_or" title="pyspark.sql.functions.bool_or"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bool_or</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns true if at least one value of <cite>col</cite> is true.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.collect_list.html#pyspark.sql.functions.collect_list" title="pyspark.sql.functions.collect_list"><code class="xref py py-obj docutils literal notranslate"><span class="pre">collect_list</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns a list of objects with duplicates.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.collect_set.html#pyspark.sql.functions.collect_set" title="pyspark.sql.functions.collect_set"><code class="xref py py-obj docutils literal notranslate"><span class="pre">collect_set</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns a set of objects with duplicate elements eliminated.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.corr.html#pyspark.sql.functions.corr" title="pyspark.sql.functions.corr"><code class="xref py py-obj docutils literal notranslate"><span class="pre">corr</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns a new <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> for the Pearson Correlation Coefficient for <code class="docutils literal notranslate"><span class="pre">col1</span></code> and <code class="docutils literal notranslate"><span class="pre">col2</span></code>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.count.html#pyspark.sql.functions.count" title="pyspark.sql.functions.count"><code class="xref py py-obj docutils literal notranslate"><span class="pre">count</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the number of items in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.count_distinct.html#pyspark.sql.functions.count_distinct" title="pyspark.sql.functions.count_distinct"><code class="xref py py-obj docutils literal notranslate"><span class="pre">count_distinct</span></code></a>(col,&nbsp;*cols)</p></td>
<td><p>Returns a new <code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code> for distinct count of <code class="docutils literal notranslate"><span class="pre">col</span></code> or <code class="docutils literal notranslate"><span class="pre">cols</span></code>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.countDistinct.html#pyspark.sql.functions.countDistinct" title="pyspark.sql.functions.countDistinct"><code class="xref py py-obj docutils literal notranslate"><span class="pre">countDistinct</span></code></a>(col,&nbsp;*cols)</p></td>
<td><p>Returns a new <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> for distinct count of <code class="docutils literal notranslate"><span class="pre">col</span></code> or <code class="docutils literal notranslate"><span class="pre">cols</span></code>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.count_min_sketch.html#pyspark.sql.functions.count_min_sketch" title="pyspark.sql.functions.count_min_sketch"><code class="xref py py-obj docutils literal notranslate"><span class="pre">count_min_sketch</span></code></a>(col,&nbsp;eps,&nbsp;confidence,&nbsp;seed)</p></td>
<td><p>Returns a count-min sketch of a column with the given esp, confidence and seed.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.count_if.html#pyspark.sql.functions.count_if" title="pyspark.sql.functions.count_if"><code class="xref py py-obj docutils literal notranslate"><span class="pre">count_if</span></code></a>(col)</p></td>
<td><p>Returns the number of <cite>TRUE</cite> values for the <cite>col</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.covar_pop.html#pyspark.sql.functions.covar_pop" title="pyspark.sql.functions.covar_pop"><code class="xref py py-obj docutils literal notranslate"><span class="pre">covar_pop</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns a new <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> for the population covariance of <code class="docutils literal notranslate"><span class="pre">col1</span></code> and <code class="docutils literal notranslate"><span class="pre">col2</span></code>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.covar_samp.html#pyspark.sql.functions.covar_samp" title="pyspark.sql.functions.covar_samp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">covar_samp</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns a new <a class="reference internal" href="api/pyspark.sql.Column.html#pyspark.sql.Column" title="pyspark.sql.Column"><code class="xref py py-class docutils literal notranslate"><span class="pre">Column</span></code></a> for the sample covariance of <code class="docutils literal notranslate"><span class="pre">col1</span></code> and <code class="docutils literal notranslate"><span class="pre">col2</span></code>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.every.html#pyspark.sql.functions.every" title="pyspark.sql.functions.every"><code class="xref py py-obj docutils literal notranslate"><span class="pre">every</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns true if all values of <cite>col</cite> are true.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.first.html#pyspark.sql.functions.first" title="pyspark.sql.functions.first"><code class="xref py py-obj docutils literal notranslate"><span class="pre">first</span></code></a>(col[,&nbsp;ignorenulls])</p></td>
<td><p>Aggregate function: returns the first value in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.first_value.html#pyspark.sql.functions.first_value" title="pyspark.sql.functions.first_value"><code class="xref py py-obj docutils literal notranslate"><span class="pre">first_value</span></code></a>(col[,&nbsp;ignoreNulls])</p></td>
<td><p>Returns the first value of <cite>col</cite> for a group of rows.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.grouping.html#pyspark.sql.functions.grouping" title="pyspark.sql.functions.grouping"><code class="xref py py-obj docutils literal notranslate"><span class="pre">grouping</span></code></a>(col)</p></td>
<td><p>Aggregate function: indicates whether a specified column in a GROUP BY list is aggregated or not, returns 1 for aggregated or 0 for not aggregated in the result set.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.grouping_id.html#pyspark.sql.functions.grouping_id" title="pyspark.sql.functions.grouping_id"><code class="xref py py-obj docutils literal notranslate"><span class="pre">grouping_id</span></code></a>(*cols)</p></td>
<td><p>Aggregate function: returns the level of grouping, equals to</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.histogram_numeric.html#pyspark.sql.functions.histogram_numeric" title="pyspark.sql.functions.histogram_numeric"><code class="xref py py-obj docutils literal notranslate"><span class="pre">histogram_numeric</span></code></a>(col,&nbsp;nBins)</p></td>
<td><p>Computes a histogram on numeric ‘col’ using nb bins.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.hll_sketch_agg.html#pyspark.sql.functions.hll_sketch_agg" title="pyspark.sql.functions.hll_sketch_agg"><code class="xref py py-obj docutils literal notranslate"><span class="pre">hll_sketch_agg</span></code></a>(col[,&nbsp;lgConfigK])</p></td>
<td><p>Aggregate function: returns the updatable binary representation of the Datasketches HllSketch configured with lgConfigK arg.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.hll_union_agg.html#pyspark.sql.functions.hll_union_agg" title="pyspark.sql.functions.hll_union_agg"><code class="xref py py-obj docutils literal notranslate"><span class="pre">hll_union_agg</span></code></a>(col[,&nbsp;allowDifferentLgConfigK])</p></td>
<td><p>Aggregate function: returns the updatable binary representation of the Datasketches HllSketch, generated by merging previously created Datasketches HllSketch instances via a Datasketches Union instance.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.kurtosis.html#pyspark.sql.functions.kurtosis" title="pyspark.sql.functions.kurtosis"><code class="xref py py-obj docutils literal notranslate"><span class="pre">kurtosis</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the kurtosis of the values in a group.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.last.html#pyspark.sql.functions.last" title="pyspark.sql.functions.last"><code class="xref py py-obj docutils literal notranslate"><span class="pre">last</span></code></a>(col[,&nbsp;ignorenulls])</p></td>
<td><p>Aggregate function: returns the last value in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.last_value.html#pyspark.sql.functions.last_value" title="pyspark.sql.functions.last_value"><code class="xref py py-obj docutils literal notranslate"><span class="pre">last_value</span></code></a>(col[,&nbsp;ignoreNulls])</p></td>
<td><p>Returns the last value of <cite>col</cite> for a group of rows.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.max.html#pyspark.sql.functions.max" title="pyspark.sql.functions.max"><code class="xref py py-obj docutils literal notranslate"><span class="pre">max</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the maximum value of the expression in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.max_by.html#pyspark.sql.functions.max_by" title="pyspark.sql.functions.max_by"><code class="xref py py-obj docutils literal notranslate"><span class="pre">max_by</span></code></a>(col,&nbsp;ord)</p></td>
<td><p>Returns the value associated with the maximum value of ord.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.mean.html#pyspark.sql.functions.mean" title="pyspark.sql.functions.mean"><code class="xref py py-obj docutils literal notranslate"><span class="pre">mean</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the average of the values in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.median.html#pyspark.sql.functions.median" title="pyspark.sql.functions.median"><code class="xref py py-obj docutils literal notranslate"><span class="pre">median</span></code></a>(col)</p></td>
<td><p>Returns the median of the values in a group.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.min.html#pyspark.sql.functions.min" title="pyspark.sql.functions.min"><code class="xref py py-obj docutils literal notranslate"><span class="pre">min</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the minimum value of the expression in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.min_by.html#pyspark.sql.functions.min_by" title="pyspark.sql.functions.min_by"><code class="xref py py-obj docutils literal notranslate"><span class="pre">min_by</span></code></a>(col,&nbsp;ord)</p></td>
<td><p>Returns the value associated with the minimum value of ord.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.mode.html#pyspark.sql.functions.mode" title="pyspark.sql.functions.mode"><code class="xref py py-obj docutils literal notranslate"><span class="pre">mode</span></code></a>(col)</p></td>
<td><p>Returns the most frequent value in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.percentile.html#pyspark.sql.functions.percentile" title="pyspark.sql.functions.percentile"><code class="xref py py-obj docutils literal notranslate"><span class="pre">percentile</span></code></a>(col,&nbsp;percentage[,&nbsp;frequency])</p></td>
<td><p>Returns the exact percentile(s) of numeric column <cite>expr</cite> at the given percentage(s) with value range in [0.0, 1.0].</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.percentile_approx.html#pyspark.sql.functions.percentile_approx" title="pyspark.sql.functions.percentile_approx"><code class="xref py py-obj docutils literal notranslate"><span class="pre">percentile_approx</span></code></a>(col,&nbsp;percentage[,&nbsp;accuracy])</p></td>
<td><p>Returns the approximate <cite>percentile</cite> of the numeric column <cite>col</cite> which is the smallest value in the ordered <cite>col</cite> values (sorted from least to greatest) such that no more than <cite>percentage</cite> of <cite>col</cite> values is less than the value or equal to that value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.product.html#pyspark.sql.functions.product" title="pyspark.sql.functions.product"><code class="xref py py-obj docutils literal notranslate"><span class="pre">product</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the product of the values in a group.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.reduce.html#pyspark.sql.functions.reduce" title="pyspark.sql.functions.reduce"><code class="xref py py-obj docutils literal notranslate"><span class="pre">reduce</span></code></a>(col,&nbsp;initialValue,&nbsp;merge[,&nbsp;finish])</p></td>
<td><p>Applies a binary operator to an initial state and all elements in the array, and reduces this to a single state.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regr_avgx.html#pyspark.sql.functions.regr_avgx" title="pyspark.sql.functions.regr_avgx"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regr_avgx</span></code></a>(y,&nbsp;x)</p></td>
<td><p>Aggregate function: returns the average of the independent variable for non-null pairs in a group, where <cite>y</cite> is the dependent variable and <cite>x</cite> is the independent variable.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regr_avgy.html#pyspark.sql.functions.regr_avgy" title="pyspark.sql.functions.regr_avgy"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regr_avgy</span></code></a>(y,&nbsp;x)</p></td>
<td><p>Aggregate function: returns the average of the dependent variable for non-null pairs in a group, where <cite>y</cite> is the dependent variable and <cite>x</cite> is the independent variable.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regr_count.html#pyspark.sql.functions.regr_count" title="pyspark.sql.functions.regr_count"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regr_count</span></code></a>(y,&nbsp;x)</p></td>
<td><p>Aggregate function: returns the number of non-null number pairs in a group, where <cite>y</cite> is the dependent variable and <cite>x</cite> is the independent variable.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regr_intercept.html#pyspark.sql.functions.regr_intercept" title="pyspark.sql.functions.regr_intercept"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regr_intercept</span></code></a>(y,&nbsp;x)</p></td>
<td><p>Aggregate function: returns the intercept of the univariate linear regression line for non-null pairs in a group, where <cite>y</cite> is the dependent variable and <cite>x</cite> is the independent variable.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regr_r2.html#pyspark.sql.functions.regr_r2" title="pyspark.sql.functions.regr_r2"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regr_r2</span></code></a>(y,&nbsp;x)</p></td>
<td><p>Aggregate function: returns the coefficient of determination for non-null pairs in a group, where <cite>y</cite> is the dependent variable and <cite>x</cite> is the independent variable.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regr_slope.html#pyspark.sql.functions.regr_slope" title="pyspark.sql.functions.regr_slope"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regr_slope</span></code></a>(y,&nbsp;x)</p></td>
<td><p>Aggregate function: returns the slope of the linear regression line for non-null pairs in a group, where <cite>y</cite> is the dependent variable and <cite>x</cite> is the independent variable.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regr_sxx.html#pyspark.sql.functions.regr_sxx" title="pyspark.sql.functions.regr_sxx"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regr_sxx</span></code></a>(y,&nbsp;x)</p></td>
<td><p>Aggregate function: returns REGR_COUNT(y, x) * VAR_POP(x) for non-null pairs in a group, where <cite>y</cite> is the dependent variable and <cite>x</cite> is the independent variable.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regr_sxy.html#pyspark.sql.functions.regr_sxy" title="pyspark.sql.functions.regr_sxy"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regr_sxy</span></code></a>(y,&nbsp;x)</p></td>
<td><p>Aggregate function: returns REGR_COUNT(y, x) * COVAR_POP(y, x) for non-null pairs in a group, where <cite>y</cite> is the dependent variable and <cite>x</cite> is the independent variable.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regr_syy.html#pyspark.sql.functions.regr_syy" title="pyspark.sql.functions.regr_syy"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regr_syy</span></code></a>(y,&nbsp;x)</p></td>
<td><p>Aggregate function: returns REGR_COUNT(y, x) * VAR_POP(y) for non-null pairs in a group, where <cite>y</cite> is the dependent variable and <cite>x</cite> is the independent variable.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.skewness.html#pyspark.sql.functions.skewness" title="pyspark.sql.functions.skewness"><code class="xref py py-obj docutils literal notranslate"><span class="pre">skewness</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the skewness of the values in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.some.html#pyspark.sql.functions.some" title="pyspark.sql.functions.some"><code class="xref py py-obj docutils literal notranslate"><span class="pre">some</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns true if at least one value of <cite>col</cite> is true.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.std.html#pyspark.sql.functions.std" title="pyspark.sql.functions.std"><code class="xref py py-obj docutils literal notranslate"><span class="pre">std</span></code></a>(col)</p></td>
<td><p>Aggregate function: alias for stddev_samp.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.stddev.html#pyspark.sql.functions.stddev" title="pyspark.sql.functions.stddev"><code class="xref py py-obj docutils literal notranslate"><span class="pre">stddev</span></code></a>(col)</p></td>
<td><p>Aggregate function: alias for stddev_samp.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.stddev_pop.html#pyspark.sql.functions.stddev_pop" title="pyspark.sql.functions.stddev_pop"><code class="xref py py-obj docutils literal notranslate"><span class="pre">stddev_pop</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns population standard deviation of the expression in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.stddev_samp.html#pyspark.sql.functions.stddev_samp" title="pyspark.sql.functions.stddev_samp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">stddev_samp</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the unbiased sample standard deviation of the expression in a group.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sum.html#pyspark.sql.functions.sum" title="pyspark.sql.functions.sum"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sum</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the sum of all values in the expression.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sum_distinct.html#pyspark.sql.functions.sum_distinct" title="pyspark.sql.functions.sum_distinct"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sum_distinct</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the sum of distinct values in the expression.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sumDistinct.html#pyspark.sql.functions.sumDistinct" title="pyspark.sql.functions.sumDistinct"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sumDistinct</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the sum of distinct values in the expression.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.var_pop.html#pyspark.sql.functions.var_pop" title="pyspark.sql.functions.var_pop"><code class="xref py py-obj docutils literal notranslate"><span class="pre">var_pop</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the population variance of the values in a group.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.var_samp.html#pyspark.sql.functions.var_samp" title="pyspark.sql.functions.var_samp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">var_samp</span></code></a>(col)</p></td>
<td><p>Aggregate function: returns the unbiased sample variance of the values in a group.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.variance.html#pyspark.sql.functions.variance" title="pyspark.sql.functions.variance"><code class="xref py py-obj docutils literal notranslate"><span class="pre">variance</span></code></a>(col)</p></td>
<td><p>Aggregate function: alias for var_samp</p></td>
</tr>
</tbody>
</table>
</section>
<section id="window-functions">
<h2>Window Functions<a class="headerlink" href="#window-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.cume_dist.html#pyspark.sql.functions.cume_dist" title="pyspark.sql.functions.cume_dist"><code class="xref py py-obj docutils literal notranslate"><span class="pre">cume_dist</span></code></a>()</p></td>
<td><p>Window function: returns the cumulative distribution of values within a window partition, i.e.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.dense_rank.html#pyspark.sql.functions.dense_rank" title="pyspark.sql.functions.dense_rank"><code class="xref py py-obj docutils literal notranslate"><span class="pre">dense_rank</span></code></a>()</p></td>
<td><p>Window function: returns the rank of rows within a window partition, without any gaps.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.lag.html#pyspark.sql.functions.lag" title="pyspark.sql.functions.lag"><code class="xref py py-obj docutils literal notranslate"><span class="pre">lag</span></code></a>(col[,&nbsp;offset,&nbsp;default])</p></td>
<td><p>Window function: returns the value that is <cite>offset</cite> rows before the current row, and <cite>default</cite> if there is less than <cite>offset</cite> rows before the current row.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.lead.html#pyspark.sql.functions.lead" title="pyspark.sql.functions.lead"><code class="xref py py-obj docutils literal notranslate"><span class="pre">lead</span></code></a>(col[,&nbsp;offset,&nbsp;default])</p></td>
<td><p>Window function: returns the value that is <cite>offset</cite> rows after the current row, and <cite>default</cite> if there is less than <cite>offset</cite> rows after the current row.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.nth_value.html#pyspark.sql.functions.nth_value" title="pyspark.sql.functions.nth_value"><code class="xref py py-obj docutils literal notranslate"><span class="pre">nth_value</span></code></a>(col,&nbsp;offset[,&nbsp;ignoreNulls])</p></td>
<td><p>Window function: returns the value that is the <cite>offset</cite>th row of the window frame (counting from 1), and <cite>null</cite> if the size of window frame is less than <cite>offset</cite> rows.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.ntile.html#pyspark.sql.functions.ntile" title="pyspark.sql.functions.ntile"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ntile</span></code></a>(n)</p></td>
<td><p>Window function: returns the ntile group id (from 1 to <cite>n</cite> inclusive) in an ordered window partition.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.percent_rank.html#pyspark.sql.functions.percent_rank" title="pyspark.sql.functions.percent_rank"><code class="xref py py-obj docutils literal notranslate"><span class="pre">percent_rank</span></code></a>()</p></td>
<td><p>Window function: returns the relative rank (i.e.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.rank.html#pyspark.sql.functions.rank" title="pyspark.sql.functions.rank"><code class="xref py py-obj docutils literal notranslate"><span class="pre">rank</span></code></a>()</p></td>
<td><p>Window function: returns the rank of rows within a window partition.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.row_number.html#pyspark.sql.functions.row_number" title="pyspark.sql.functions.row_number"><code class="xref py py-obj docutils literal notranslate"><span class="pre">row_number</span></code></a>()</p></td>
<td><p>Window function: returns a sequential number starting at 1 within a window partition.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="sort-functions">
<h2>Sort Functions<a class="headerlink" href="#sort-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.asc.html#pyspark.sql.functions.asc" title="pyspark.sql.functions.asc"><code class="xref py py-obj docutils literal notranslate"><span class="pre">asc</span></code></a>(col)</p></td>
<td><p>Returns a sort expression based on the ascending order of the given column name.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.asc_nulls_first.html#pyspark.sql.functions.asc_nulls_first" title="pyspark.sql.functions.asc_nulls_first"><code class="xref py py-obj docutils literal notranslate"><span class="pre">asc_nulls_first</span></code></a>(col)</p></td>
<td><p>Returns a sort expression based on the ascending order of the given column name, and null values return before non-null values.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.asc_nulls_last.html#pyspark.sql.functions.asc_nulls_last" title="pyspark.sql.functions.asc_nulls_last"><code class="xref py py-obj docutils literal notranslate"><span class="pre">asc_nulls_last</span></code></a>(col)</p></td>
<td><p>Returns a sort expression based on the ascending order of the given column name, and null values appear after non-null values.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.desc.html#pyspark.sql.functions.desc" title="pyspark.sql.functions.desc"><code class="xref py py-obj docutils literal notranslate"><span class="pre">desc</span></code></a>(col)</p></td>
<td><p>Returns a sort expression based on the descending order of the given column name.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.desc_nulls_first.html#pyspark.sql.functions.desc_nulls_first" title="pyspark.sql.functions.desc_nulls_first"><code class="xref py py-obj docutils literal notranslate"><span class="pre">desc_nulls_first</span></code></a>(col)</p></td>
<td><p>Returns a sort expression based on the descending order of the given column name, and null values appear before non-null values.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.desc_nulls_last.html#pyspark.sql.functions.desc_nulls_last" title="pyspark.sql.functions.desc_nulls_last"><code class="xref py py-obj docutils literal notranslate"><span class="pre">desc_nulls_last</span></code></a>(col)</p></td>
<td><p>Returns a sort expression based on the descending order of the given column name, and null values appear after non-null values.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="string-functions">
<h2>String Functions<a class="headerlink" href="#string-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.ascii.html#pyspark.sql.functions.ascii" title="pyspark.sql.functions.ascii"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ascii</span></code></a>(col)</p></td>
<td><p>Computes the numeric value of the first character of the string column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.base64.html#pyspark.sql.functions.base64" title="pyspark.sql.functions.base64"><code class="xref py py-obj docutils literal notranslate"><span class="pre">base64</span></code></a>(col)</p></td>
<td><p>Computes the BASE64 encoding of a binary column and returns it as a string column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bit_length.html#pyspark.sql.functions.bit_length" title="pyspark.sql.functions.bit_length"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bit_length</span></code></a>(col)</p></td>
<td><p>Calculates the bit length for the specified string column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.btrim.html#pyspark.sql.functions.btrim" title="pyspark.sql.functions.btrim"><code class="xref py py-obj docutils literal notranslate"><span class="pre">btrim</span></code></a>(str[,&nbsp;trim])</p></td>
<td><p>Remove the leading and trailing <cite>trim</cite> characters from <cite>str</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.char.html#pyspark.sql.functions.char" title="pyspark.sql.functions.char"><code class="xref py py-obj docutils literal notranslate"><span class="pre">char</span></code></a>(col)</p></td>
<td><p>Returns the ASCII character having the binary equivalent to <cite>col</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.character_length.html#pyspark.sql.functions.character_length" title="pyspark.sql.functions.character_length"><code class="xref py py-obj docutils literal notranslate"><span class="pre">character_length</span></code></a>(str)</p></td>
<td><p>Returns the character length of string data or number of bytes of binary data.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.char_length.html#pyspark.sql.functions.char_length" title="pyspark.sql.functions.char_length"><code class="xref py py-obj docutils literal notranslate"><span class="pre">char_length</span></code></a>(str)</p></td>
<td><p>Returns the character length of string data or number of bytes of binary data.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.concat_ws.html#pyspark.sql.functions.concat_ws" title="pyspark.sql.functions.concat_ws"><code class="xref py py-obj docutils literal notranslate"><span class="pre">concat_ws</span></code></a>(sep,&nbsp;*cols)</p></td>
<td><p>Concatenates multiple input string columns together into a single string column, using the given separator.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.contains.html#pyspark.sql.functions.contains" title="pyspark.sql.functions.contains"><code class="xref py py-obj docutils literal notranslate"><span class="pre">contains</span></code></a>(left,&nbsp;right)</p></td>
<td><p>Returns a boolean.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.decode.html#pyspark.sql.functions.decode" title="pyspark.sql.functions.decode"><code class="xref py py-obj docutils literal notranslate"><span class="pre">decode</span></code></a>(col,&nbsp;charset)</p></td>
<td><p>Computes the first argument into a string from a binary using the provided character set (one of ‘US-ASCII’, ‘ISO-8859-1’, ‘UTF-8’, ‘UTF-16BE’, ‘UTF-16LE’, ‘UTF-16’).</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.elt.html#pyspark.sql.functions.elt" title="pyspark.sql.functions.elt"><code class="xref py py-obj docutils literal notranslate"><span class="pre">elt</span></code></a>(*inputs)</p></td>
<td><p>Returns the <cite>n</cite>-th input, e.g., returns <cite>input2</cite> when <cite>n</cite> is 2.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.encode.html#pyspark.sql.functions.encode" title="pyspark.sql.functions.encode"><code class="xref py py-obj docutils literal notranslate"><span class="pre">encode</span></code></a>(col,&nbsp;charset)</p></td>
<td><p>Computes the first argument into a binary from a string using the provided character set (one of ‘US-ASCII’, ‘ISO-8859-1’, ‘UTF-8’, ‘UTF-16BE’, ‘UTF-16LE’, ‘UTF-16’).</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.endswith.html#pyspark.sql.functions.endswith" title="pyspark.sql.functions.endswith"><code class="xref py py-obj docutils literal notranslate"><span class="pre">endswith</span></code></a>(str,&nbsp;suffix)</p></td>
<td><p>Returns a boolean.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.find_in_set.html#pyspark.sql.functions.find_in_set" title="pyspark.sql.functions.find_in_set"><code class="xref py py-obj docutils literal notranslate"><span class="pre">find_in_set</span></code></a>(str,&nbsp;str_array)</p></td>
<td><p>Returns the index (1-based) of the given string (<cite>str</cite>) in the comma-delimited list (<cite>strArray</cite>).</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.format_number.html#pyspark.sql.functions.format_number" title="pyspark.sql.functions.format_number"><code class="xref py py-obj docutils literal notranslate"><span class="pre">format_number</span></code></a>(col,&nbsp;d)</p></td>
<td><p>Formats the number X to a format like ‘#,–#,–#.–’, rounded to d decimal places with HALF_EVEN round mode, and returns the result as a string.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.format_string.html#pyspark.sql.functions.format_string" title="pyspark.sql.functions.format_string"><code class="xref py py-obj docutils literal notranslate"><span class="pre">format_string</span></code></a>(format,&nbsp;*cols)</p></td>
<td><p>Formats the arguments in printf-style and returns the result as a string column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.ilike.html#pyspark.sql.functions.ilike" title="pyspark.sql.functions.ilike"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ilike</span></code></a>(str,&nbsp;pattern[,&nbsp;escapeChar])</p></td>
<td><p>Returns true if str matches <cite>pattern</cite> with <cite>escape</cite> case-insensitively, null if any arguments are null, false otherwise.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.initcap.html#pyspark.sql.functions.initcap" title="pyspark.sql.functions.initcap"><code class="xref py py-obj docutils literal notranslate"><span class="pre">initcap</span></code></a>(col)</p></td>
<td><p>Translate the first letter of each word to upper case in the sentence.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.instr.html#pyspark.sql.functions.instr" title="pyspark.sql.functions.instr"><code class="xref py py-obj docutils literal notranslate"><span class="pre">instr</span></code></a>(str,&nbsp;substr)</p></td>
<td><p>Locate the position of the first occurrence of substr column in the given string.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.lcase.html#pyspark.sql.functions.lcase" title="pyspark.sql.functions.lcase"><code class="xref py py-obj docutils literal notranslate"><span class="pre">lcase</span></code></a>(str)</p></td>
<td><p>Returns <cite>str</cite> with all characters changed to lowercase.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.length.html#pyspark.sql.functions.length" title="pyspark.sql.functions.length"><code class="xref py py-obj docutils literal notranslate"><span class="pre">length</span></code></a>(col)</p></td>
<td><p>Computes the character length of string data or number of bytes of binary data.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.like.html#pyspark.sql.functions.like" title="pyspark.sql.functions.like"><code class="xref py py-obj docutils literal notranslate"><span class="pre">like</span></code></a>(str,&nbsp;pattern[,&nbsp;escapeChar])</p></td>
<td><p>Returns true if str matches <cite>pattern</cite> with <cite>escape</cite>, null if any arguments are null, false otherwise.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.lower.html#pyspark.sql.functions.lower" title="pyspark.sql.functions.lower"><code class="xref py py-obj docutils literal notranslate"><span class="pre">lower</span></code></a>(col)</p></td>
<td><p>Converts a string expression to lower case.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.left.html#pyspark.sql.functions.left" title="pyspark.sql.functions.left"><code class="xref py py-obj docutils literal notranslate"><span class="pre">left</span></code></a>(str,&nbsp;len)</p></td>
<td><p>Returns the leftmost <cite>len`(`len</cite> can be string type) characters from the string <cite>str</cite>, if <cite>len</cite> is less or equal than 0 the result is an empty string.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.levenshtein.html#pyspark.sql.functions.levenshtein" title="pyspark.sql.functions.levenshtein"><code class="xref py py-obj docutils literal notranslate"><span class="pre">levenshtein</span></code></a>(left,&nbsp;right[,&nbsp;threshold])</p></td>
<td><p>Computes the Levenshtein distance of the two given strings.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.locate.html#pyspark.sql.functions.locate" title="pyspark.sql.functions.locate"><code class="xref py py-obj docutils literal notranslate"><span class="pre">locate</span></code></a>(substr,&nbsp;str[,&nbsp;pos])</p></td>
<td><p>Locate the position of the first occurrence of substr in a string column, after position pos.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.lpad.html#pyspark.sql.functions.lpad" title="pyspark.sql.functions.lpad"><code class="xref py py-obj docutils literal notranslate"><span class="pre">lpad</span></code></a>(col,&nbsp;len,&nbsp;pad)</p></td>
<td><p>Left-pad the string column to width <cite>len</cite> with <cite>pad</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.ltrim.html#pyspark.sql.functions.ltrim" title="pyspark.sql.functions.ltrim"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ltrim</span></code></a>(col)</p></td>
<td><p>Trim the spaces from left end for the specified string value.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.mask.html#pyspark.sql.functions.mask" title="pyspark.sql.functions.mask"><code class="xref py py-obj docutils literal notranslate"><span class="pre">mask</span></code></a>(col[,&nbsp;upperChar,&nbsp;lowerChar,&nbsp;digitChar,&nbsp;…])</p></td>
<td><p>Masks the given string value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.octet_length.html#pyspark.sql.functions.octet_length" title="pyspark.sql.functions.octet_length"><code class="xref py py-obj docutils literal notranslate"><span class="pre">octet_length</span></code></a>(col)</p></td>
<td><p>Calculates the byte length for the specified string column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.parse_url.html#pyspark.sql.functions.parse_url" title="pyspark.sql.functions.parse_url"><code class="xref py py-obj docutils literal notranslate"><span class="pre">parse_url</span></code></a>(url,&nbsp;partToExtract[,&nbsp;key])</p></td>
<td><p>Extracts a part from a URL.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.position.html#pyspark.sql.functions.position" title="pyspark.sql.functions.position"><code class="xref py py-obj docutils literal notranslate"><span class="pre">position</span></code></a>(substr,&nbsp;str[,&nbsp;start])</p></td>
<td><p>Returns the position of the first occurrence of <cite>substr</cite> in <cite>str</cite> after position <cite>start</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.printf.html#pyspark.sql.functions.printf" title="pyspark.sql.functions.printf"><code class="xref py py-obj docutils literal notranslate"><span class="pre">printf</span></code></a>(format,&nbsp;*cols)</p></td>
<td><p>Formats the arguments in printf-style and returns the result as a string column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.rlike.html#pyspark.sql.functions.rlike" title="pyspark.sql.functions.rlike"><code class="xref py py-obj docutils literal notranslate"><span class="pre">rlike</span></code></a>(str,&nbsp;regexp)</p></td>
<td><p>Returns true if <cite>str</cite> matches the Java regex <cite>regexp</cite>, or false otherwise.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regexp.html#pyspark.sql.functions.regexp" title="pyspark.sql.functions.regexp"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regexp</span></code></a>(str,&nbsp;regexp)</p></td>
<td><p>Returns true if <cite>str</cite> matches the Java regex <cite>regexp</cite>, or false otherwise.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regexp_like.html#pyspark.sql.functions.regexp_like" title="pyspark.sql.functions.regexp_like"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regexp_like</span></code></a>(str,&nbsp;regexp)</p></td>
<td><p>Returns true if <cite>str</cite> matches the Java regex <cite>regexp</cite>, or false otherwise.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regexp_count.html#pyspark.sql.functions.regexp_count" title="pyspark.sql.functions.regexp_count"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regexp_count</span></code></a>(str,&nbsp;regexp)</p></td>
<td><p>Returns a count of the number of times that the Java regex pattern <cite>regexp</cite> is matched in the string <cite>str</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regexp_extract.html#pyspark.sql.functions.regexp_extract" title="pyspark.sql.functions.regexp_extract"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regexp_extract</span></code></a>(str,&nbsp;pattern,&nbsp;idx)</p></td>
<td><p>Extract a specific group matched by the Java regex <cite>regexp</cite>, from the specified string column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regexp_extract_all.html#pyspark.sql.functions.regexp_extract_all" title="pyspark.sql.functions.regexp_extract_all"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regexp_extract_all</span></code></a>(str,&nbsp;regexp[,&nbsp;idx])</p></td>
<td><p>Extract all strings in the <cite>str</cite> that match the Java regex <cite>regexp</cite> and corresponding to the regex group index.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regexp_replace.html#pyspark.sql.functions.regexp_replace" title="pyspark.sql.functions.regexp_replace"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regexp_replace</span></code></a>(string,&nbsp;pattern,&nbsp;replacement)</p></td>
<td><p>Replace all substrings of the specified string value that match regexp with replacement.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regexp_substr.html#pyspark.sql.functions.regexp_substr" title="pyspark.sql.functions.regexp_substr"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regexp_substr</span></code></a>(str,&nbsp;regexp)</p></td>
<td><p>Returns the substring that matches the Java regex <cite>regexp</cite> within the string <cite>str</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.regexp_instr.html#pyspark.sql.functions.regexp_instr" title="pyspark.sql.functions.regexp_instr"><code class="xref py py-obj docutils literal notranslate"><span class="pre">regexp_instr</span></code></a>(str,&nbsp;regexp[,&nbsp;idx])</p></td>
<td><p>Extract all strings in the <cite>str</cite> that match the Java regex <cite>regexp</cite> and corresponding to the regex group index.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.replace.html#pyspark.sql.functions.replace" title="pyspark.sql.functions.replace"><code class="xref py py-obj docutils literal notranslate"><span class="pre">replace</span></code></a>(src,&nbsp;search[,&nbsp;replace])</p></td>
<td><p>Replaces all occurrences of <cite>search</cite> with <cite>replace</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.right.html#pyspark.sql.functions.right" title="pyspark.sql.functions.right"><code class="xref py py-obj docutils literal notranslate"><span class="pre">right</span></code></a>(str,&nbsp;len)</p></td>
<td><p>Returns the rightmost <cite>len`(`len</cite> can be string type) characters from the string <cite>str</cite>, if <cite>len</cite> is less or equal than 0 the result is an empty string.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.ucase.html#pyspark.sql.functions.ucase" title="pyspark.sql.functions.ucase"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ucase</span></code></a>(str)</p></td>
<td><p>Returns <cite>str</cite> with all characters changed to uppercase.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.unbase64.html#pyspark.sql.functions.unbase64" title="pyspark.sql.functions.unbase64"><code class="xref py py-obj docutils literal notranslate"><span class="pre">unbase64</span></code></a>(col)</p></td>
<td><p>Decodes a BASE64 encoded string column and returns it as a binary column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.rpad.html#pyspark.sql.functions.rpad" title="pyspark.sql.functions.rpad"><code class="xref py py-obj docutils literal notranslate"><span class="pre">rpad</span></code></a>(col,&nbsp;len,&nbsp;pad)</p></td>
<td><p>Right-pad the string column to width <cite>len</cite> with <cite>pad</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.repeat.html#pyspark.sql.functions.repeat" title="pyspark.sql.functions.repeat"><code class="xref py py-obj docutils literal notranslate"><span class="pre">repeat</span></code></a>(col,&nbsp;n)</p></td>
<td><p>Repeats a string column n times, and returns it as a new string column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.rtrim.html#pyspark.sql.functions.rtrim" title="pyspark.sql.functions.rtrim"><code class="xref py py-obj docutils literal notranslate"><span class="pre">rtrim</span></code></a>(col)</p></td>
<td><p>Trim the spaces from right end for the specified string value.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.soundex.html#pyspark.sql.functions.soundex" title="pyspark.sql.functions.soundex"><code class="xref py py-obj docutils literal notranslate"><span class="pre">soundex</span></code></a>(col)</p></td>
<td><p>Returns the SoundEx encoding for a string</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.split.html#pyspark.sql.functions.split" title="pyspark.sql.functions.split"><code class="xref py py-obj docutils literal notranslate"><span class="pre">split</span></code></a>(str,&nbsp;pattern[,&nbsp;limit])</p></td>
<td><p>Splits str around matches of the given pattern.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.split_part.html#pyspark.sql.functions.split_part" title="pyspark.sql.functions.split_part"><code class="xref py py-obj docutils literal notranslate"><span class="pre">split_part</span></code></a>(src,&nbsp;delimiter,&nbsp;partNum)</p></td>
<td><p>Splits <cite>str</cite> by delimiter and return requested part of the split (1-based).</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.startswith.html#pyspark.sql.functions.startswith" title="pyspark.sql.functions.startswith"><code class="xref py py-obj docutils literal notranslate"><span class="pre">startswith</span></code></a>(str,&nbsp;prefix)</p></td>
<td><p>Returns a boolean.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.substr.html#pyspark.sql.functions.substr" title="pyspark.sql.functions.substr"><code class="xref py py-obj docutils literal notranslate"><span class="pre">substr</span></code></a>(str,&nbsp;pos[,&nbsp;len])</p></td>
<td><p>Returns the substring of <cite>str</cite> that starts at <cite>pos</cite> and is of length <cite>len</cite>, or the slice of byte array that starts at <cite>pos</cite> and is of length <cite>len</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.substring.html#pyspark.sql.functions.substring" title="pyspark.sql.functions.substring"><code class="xref py py-obj docutils literal notranslate"><span class="pre">substring</span></code></a>(str,&nbsp;pos,&nbsp;len)</p></td>
<td><p>Substring starts at <cite>pos</cite> and is of length <cite>len</cite> when str is String type or returns the slice of byte array that starts at <cite>pos</cite> in byte and is of length <cite>len</cite> when str is Binary type.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.substring_index.html#pyspark.sql.functions.substring_index" title="pyspark.sql.functions.substring_index"><code class="xref py py-obj docutils literal notranslate"><span class="pre">substring_index</span></code></a>(str,&nbsp;delim,&nbsp;count)</p></td>
<td><p>Returns the substring from string str before count occurrences of the delimiter delim.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.overlay.html#pyspark.sql.functions.overlay" title="pyspark.sql.functions.overlay"><code class="xref py py-obj docutils literal notranslate"><span class="pre">overlay</span></code></a>(src,&nbsp;replace,&nbsp;pos[,&nbsp;len])</p></td>
<td><p>Overlay the specified portion of <cite>src</cite> with <cite>replace</cite>, starting from byte position <cite>pos</cite> of <cite>src</cite> and proceeding for <cite>len</cite> bytes.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sentences.html#pyspark.sql.functions.sentences" title="pyspark.sql.functions.sentences"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sentences</span></code></a>(string[,&nbsp;language,&nbsp;country])</p></td>
<td><p>Splits a string into arrays of sentences, where each sentence is an array of words.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_binary.html#pyspark.sql.functions.to_binary" title="pyspark.sql.functions.to_binary"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_binary</span></code></a>(col[,&nbsp;format])</p></td>
<td><p>Converts the input <cite>col</cite> to a binary value based on the supplied <cite>format</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_char.html#pyspark.sql.functions.to_char" title="pyspark.sql.functions.to_char"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_char</span></code></a>(col,&nbsp;format)</p></td>
<td><p>Convert <cite>col</cite> to a string based on the <cite>format</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_number.html#pyspark.sql.functions.to_number" title="pyspark.sql.functions.to_number"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_number</span></code></a>(col,&nbsp;format)</p></td>
<td><p>Convert string ‘col’ to a number based on the string format ‘format’.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.to_varchar.html#pyspark.sql.functions.to_varchar" title="pyspark.sql.functions.to_varchar"><code class="xref py py-obj docutils literal notranslate"><span class="pre">to_varchar</span></code></a>(col,&nbsp;format)</p></td>
<td><p>Convert <cite>col</cite> to a string based on the <cite>format</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.translate.html#pyspark.sql.functions.translate" title="pyspark.sql.functions.translate"><code class="xref py py-obj docutils literal notranslate"><span class="pre">translate</span></code></a>(srcCol,&nbsp;matching,&nbsp;replace)</p></td>
<td><p>A function translate any character in the <cite>srcCol</cite> by a character in <cite>matching</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.trim.html#pyspark.sql.functions.trim" title="pyspark.sql.functions.trim"><code class="xref py py-obj docutils literal notranslate"><span class="pre">trim</span></code></a>(col)</p></td>
<td><p>Trim the spaces from both ends for the specified string column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.upper.html#pyspark.sql.functions.upper" title="pyspark.sql.functions.upper"><code class="xref py py-obj docutils literal notranslate"><span class="pre">upper</span></code></a>(col)</p></td>
<td><p>Converts a string expression to upper case.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.url_decode.html#pyspark.sql.functions.url_decode" title="pyspark.sql.functions.url_decode"><code class="xref py py-obj docutils literal notranslate"><span class="pre">url_decode</span></code></a>(str)</p></td>
<td><p>Decodes a <cite>str</cite> in ‘application/x-www-form-urlencoded’ format using a specific encoding scheme.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.url_encode.html#pyspark.sql.functions.url_encode" title="pyspark.sql.functions.url_encode"><code class="xref py py-obj docutils literal notranslate"><span class="pre">url_encode</span></code></a>(str)</p></td>
<td><p>Translates a string into ‘application/x-www-form-urlencoded’ format using a specific encoding scheme.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="bitwise-functions">
<h2>Bitwise Functions<a class="headerlink" href="#bitwise-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bit_count.html#pyspark.sql.functions.bit_count" title="pyspark.sql.functions.bit_count"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bit_count</span></code></a>(col)</p></td>
<td><p>Returns the number of bits that are set in the argument expr as an unsigned 64-bit integer, or NULL if the argument is NULL.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bit_get.html#pyspark.sql.functions.bit_get" title="pyspark.sql.functions.bit_get"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bit_get</span></code></a>(col,&nbsp;pos)</p></td>
<td><p>Returns the value of the bit (0 or 1) at the specified position.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.getbit.html#pyspark.sql.functions.getbit" title="pyspark.sql.functions.getbit"><code class="xref py py-obj docutils literal notranslate"><span class="pre">getbit</span></code></a>(col,&nbsp;pos)</p></td>
<td><p>Returns the value of the bit (0 or 1) at the specified position.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="call-functions">
<h2>Call Functions<a class="headerlink" href="#call-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.call_function.html#pyspark.sql.functions.call_function" title="pyspark.sql.functions.call_function"><code class="xref py py-obj docutils literal notranslate"><span class="pre">call_function</span></code></a>(funcName,&nbsp;*cols)</p></td>
<td><p>Call a SQL function.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.call_udf.html#pyspark.sql.functions.call_udf" title="pyspark.sql.functions.call_udf"><code class="xref py py-obj docutils literal notranslate"><span class="pre">call_udf</span></code></a>(udfName,&nbsp;*cols)</p></td>
<td><p>Call an user-defined function.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.pandas_udf.html#pyspark.sql.functions.pandas_udf" title="pyspark.sql.functions.pandas_udf"><code class="xref py py-obj docutils literal notranslate"><span class="pre">pandas_udf</span></code></a>([f,&nbsp;returnType,&nbsp;functionType])</p></td>
<td><p>Creates a pandas user defined function (a.k.a.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.udf.html#pyspark.sql.functions.udf" title="pyspark.sql.functions.udf"><code class="xref py py-obj docutils literal notranslate"><span class="pre">udf</span></code></a>([f,&nbsp;returnType,&nbsp;useArrow])</p></td>
<td><p>Creates a user defined function (UDF).</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.udtf.html#pyspark.sql.functions.udtf" title="pyspark.sql.functions.udtf"><code class="xref py py-obj docutils literal notranslate"><span class="pre">udtf</span></code></a>([cls,&nbsp;useArrow])</p></td>
<td><p>Creates a user defined table function (UDTF).</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.unwrap_udt.html#pyspark.sql.functions.unwrap_udt" title="pyspark.sql.functions.unwrap_udt"><code class="xref py py-obj docutils literal notranslate"><span class="pre">unwrap_udt</span></code></a>(col)</p></td>
<td><p>Unwrap UDT data type column into its underlying type.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="misc-functions">
<h2>Misc Functions<a class="headerlink" href="#misc-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.aes_decrypt.html#pyspark.sql.functions.aes_decrypt" title="pyspark.sql.functions.aes_decrypt"><code class="xref py py-obj docutils literal notranslate"><span class="pre">aes_decrypt</span></code></a>(input,&nbsp;key[,&nbsp;mode,&nbsp;padding,&nbsp;aad])</p></td>
<td><p>Returns a decrypted value of <cite>input</cite> using AES in <cite>mode</cite> with <cite>padding</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.aes_encrypt.html#pyspark.sql.functions.aes_encrypt" title="pyspark.sql.functions.aes_encrypt"><code class="xref py py-obj docutils literal notranslate"><span class="pre">aes_encrypt</span></code></a>(input,&nbsp;key[,&nbsp;mode,&nbsp;padding,&nbsp;iv,&nbsp;aad])</p></td>
<td><p>Returns an encrypted value of <cite>input</cite> using AES in given <cite>mode</cite> with the specified <cite>padding</cite>.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bitmap_bit_position.html#pyspark.sql.functions.bitmap_bit_position" title="pyspark.sql.functions.bitmap_bit_position"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bitmap_bit_position</span></code></a>(col)</p></td>
<td><p>Returns the bit position for the given input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bitmap_bucket_number.html#pyspark.sql.functions.bitmap_bucket_number" title="pyspark.sql.functions.bitmap_bucket_number"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bitmap_bucket_number</span></code></a>(col)</p></td>
<td><p>Returns the bucket number for the given input column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bitmap_construct_agg.html#pyspark.sql.functions.bitmap_construct_agg" title="pyspark.sql.functions.bitmap_construct_agg"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bitmap_construct_agg</span></code></a>(col)</p></td>
<td><p>Returns a bitmap with the positions of the bits set from all the values from the input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bitmap_count.html#pyspark.sql.functions.bitmap_count" title="pyspark.sql.functions.bitmap_count"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bitmap_count</span></code></a>(col)</p></td>
<td><p>Returns the number of set bits in the input bitmap.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.bitmap_or_agg.html#pyspark.sql.functions.bitmap_or_agg" title="pyspark.sql.functions.bitmap_or_agg"><code class="xref py py-obj docutils literal notranslate"><span class="pre">bitmap_or_agg</span></code></a>(col)</p></td>
<td><p>Returns a bitmap that is the bitwise OR of all of the bitmaps from the input column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.current_catalog.html#pyspark.sql.functions.current_catalog" title="pyspark.sql.functions.current_catalog"><code class="xref py py-obj docutils literal notranslate"><span class="pre">current_catalog</span></code></a>()</p></td>
<td><p>Returns the current catalog.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.current_database.html#pyspark.sql.functions.current_database" title="pyspark.sql.functions.current_database"><code class="xref py py-obj docutils literal notranslate"><span class="pre">current_database</span></code></a>()</p></td>
<td><p>Returns the current database.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.current_schema.html#pyspark.sql.functions.current_schema" title="pyspark.sql.functions.current_schema"><code class="xref py py-obj docutils literal notranslate"><span class="pre">current_schema</span></code></a>()</p></td>
<td><p>Returns the current database.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.current_user.html#pyspark.sql.functions.current_user" title="pyspark.sql.functions.current_user"><code class="xref py py-obj docutils literal notranslate"><span class="pre">current_user</span></code></a>()</p></td>
<td><p>Returns the current database.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.input_file_block_length.html#pyspark.sql.functions.input_file_block_length" title="pyspark.sql.functions.input_file_block_length"><code class="xref py py-obj docutils literal notranslate"><span class="pre">input_file_block_length</span></code></a>()</p></td>
<td><p>Returns the length of the block being read, or -1 if not available.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.input_file_block_start.html#pyspark.sql.functions.input_file_block_start" title="pyspark.sql.functions.input_file_block_start"><code class="xref py py-obj docutils literal notranslate"><span class="pre">input_file_block_start</span></code></a>()</p></td>
<td><p>Returns the start offset of the block being read, or -1 if not available.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.md5.html#pyspark.sql.functions.md5" title="pyspark.sql.functions.md5"><code class="xref py py-obj docutils literal notranslate"><span class="pre">md5</span></code></a>(col)</p></td>
<td><p>Calculates the MD5 digest and returns the value as a 32 character hex string.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sha.html#pyspark.sql.functions.sha" title="pyspark.sql.functions.sha"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sha</span></code></a>(col)</p></td>
<td><p>Returns a sha1 hash value as a hex string of the <cite>col</cite>.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sha1.html#pyspark.sql.functions.sha1" title="pyspark.sql.functions.sha1"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sha1</span></code></a>(col)</p></td>
<td><p>Returns the hex string result of SHA-1.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.sha2.html#pyspark.sql.functions.sha2" title="pyspark.sql.functions.sha2"><code class="xref py py-obj docutils literal notranslate"><span class="pre">sha2</span></code></a>(col,&nbsp;numBits)</p></td>
<td><p>Returns the hex string result of SHA-2 family of hash functions (SHA-224, SHA-256, SHA-384, and SHA-512).</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.crc32.html#pyspark.sql.functions.crc32" title="pyspark.sql.functions.crc32"><code class="xref py py-obj docutils literal notranslate"><span class="pre">crc32</span></code></a>(col)</p></td>
<td><p>Calculates the cyclic redundancy check value  (CRC32) of a binary column and returns the value as a bigint.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.hash.html#pyspark.sql.functions.hash" title="pyspark.sql.functions.hash"><code class="xref py py-obj docutils literal notranslate"><span class="pre">hash</span></code></a>(*cols)</p></td>
<td><p>Calculates the hash code of given columns, and returns the result as an int column.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xxhash64.html#pyspark.sql.functions.xxhash64" title="pyspark.sql.functions.xxhash64"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xxhash64</span></code></a>(*cols)</p></td>
<td><p>Calculates the hash code of given columns using the 64-bit variant of the xxHash algorithm, and returns the result as a long column.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.assert_true.html#pyspark.sql.functions.assert_true" title="pyspark.sql.functions.assert_true"><code class="xref py py-obj docutils literal notranslate"><span class="pre">assert_true</span></code></a>(col[,&nbsp;errMsg])</p></td>
<td><p>Returns <cite>null</cite> if the input column is <cite>true</cite>; throws an exception with the provided error message otherwise.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.raise_error.html#pyspark.sql.functions.raise_error" title="pyspark.sql.functions.raise_error"><code class="xref py py-obj docutils literal notranslate"><span class="pre">raise_error</span></code></a>(errMsg)</p></td>
<td><p>Throws an exception with the provided error message.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.reflect.html#pyspark.sql.functions.reflect" title="pyspark.sql.functions.reflect"><code class="xref py py-obj docutils literal notranslate"><span class="pre">reflect</span></code></a>(*cols)</p></td>
<td><p>Calls a method with reflection.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.hll_sketch_estimate.html#pyspark.sql.functions.hll_sketch_estimate" title="pyspark.sql.functions.hll_sketch_estimate"><code class="xref py py-obj docutils literal notranslate"><span class="pre">hll_sketch_estimate</span></code></a>(col)</p></td>
<td><p>Returns the estimated number of unique values given the binary representation of a Datasketches HllSketch.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.hll_union.html#pyspark.sql.functions.hll_union" title="pyspark.sql.functions.hll_union"><code class="xref py py-obj docutils literal notranslate"><span class="pre">hll_union</span></code></a>(col1,&nbsp;col2[,&nbsp;allowDifferentLgConfigK])</p></td>
<td><p>Merges two binary representations of Datasketches HllSketch objects, using a Datasketches Union object.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.java_method.html#pyspark.sql.functions.java_method" title="pyspark.sql.functions.java_method"><code class="xref py py-obj docutils literal notranslate"><span class="pre">java_method</span></code></a>(*cols)</p></td>
<td><p>Calls a method with reflection.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.stack.html#pyspark.sql.functions.stack" title="pyspark.sql.functions.stack"><code class="xref py py-obj docutils literal notranslate"><span class="pre">stack</span></code></a>(*cols)</p></td>
<td><p>Separates <cite>col1</cite>, …, <cite>colk</cite> into <cite>n</cite> rows.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.try_aes_decrypt.html#pyspark.sql.functions.try_aes_decrypt" title="pyspark.sql.functions.try_aes_decrypt"><code class="xref py py-obj docutils literal notranslate"><span class="pre">try_aes_decrypt</span></code></a>(input,&nbsp;key[,&nbsp;mode,&nbsp;padding,&nbsp;aad])</p></td>
<td><p>This is a special version of <cite>aes_decrypt</cite> that performs the same operation, but returns a NULL value instead of raising an error if the decryption cannot be performed.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.typeof.html#pyspark.sql.functions.typeof" title="pyspark.sql.functions.typeof"><code class="xref py py-obj docutils literal notranslate"><span class="pre">typeof</span></code></a>(col)</p></td>
<td><p>Return DDL-formatted type string for the data type of the input.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.user.html#pyspark.sql.functions.user" title="pyspark.sql.functions.user"><code class="xref py py-obj docutils literal notranslate"><span class="pre">user</span></code></a>()</p></td>
<td><p>Returns the current database.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.version.html#pyspark.sql.functions.version" title="pyspark.sql.functions.version"><code class="xref py py-obj docutils literal notranslate"><span class="pre">version</span></code></a>()</p></td>
<td><p>Returns the Spark version.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="predicate-functions">
<h2>Predicate Functions<a class="headerlink" href="#predicate-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.equal_null.html#pyspark.sql.functions.equal_null" title="pyspark.sql.functions.equal_null"><code class="xref py py-obj docutils literal notranslate"><span class="pre">equal_null</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns same result as the EQUAL(=) operator for non-null operands, but returns true if both are null, false if one of the them is null.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.ifnull.html#pyspark.sql.functions.ifnull" title="pyspark.sql.functions.ifnull"><code class="xref py py-obj docutils literal notranslate"><span class="pre">ifnull</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns <cite>col2</cite> if <cite>col1</cite> is null, or <cite>col1</cite> otherwise.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.isnotnull.html#pyspark.sql.functions.isnotnull" title="pyspark.sql.functions.isnotnull"><code class="xref py py-obj docutils literal notranslate"><span class="pre">isnotnull</span></code></a>(col)</p></td>
<td><p>Returns true if <cite>col</cite> is not null, or false otherwise.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.nullif.html#pyspark.sql.functions.nullif" title="pyspark.sql.functions.nullif"><code class="xref py py-obj docutils literal notranslate"><span class="pre">nullif</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns null if <cite>col1</cite> equals to <cite>col2</cite>, or <cite>col1</cite> otherwise.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.nvl.html#pyspark.sql.functions.nvl" title="pyspark.sql.functions.nvl"><code class="xref py py-obj docutils literal notranslate"><span class="pre">nvl</span></code></a>(col1,&nbsp;col2)</p></td>
<td><p>Returns <cite>col2</cite> if <cite>col1</cite> is null, or <cite>col1</cite> otherwise.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.nvl2.html#pyspark.sql.functions.nvl2" title="pyspark.sql.functions.nvl2"><code class="xref py py-obj docutils literal notranslate"><span class="pre">nvl2</span></code></a>(col1,&nbsp;col2,&nbsp;col3)</p></td>
<td><p>Returns <cite>col2</cite> if <cite>col1</cite> is not null, or <cite>col3</cite> otherwise.</p></td>
</tr>
</tbody>
</table>
</section>
<section id="xml-functions">
<h2>Xml Functions<a class="headerlink" href="#xml-functions" title="Permalink to this headline">¶</a></h2>
<table class="longtable table autosummary">
<colgroup>
<col style="width: 10%">
<col style="width: 90%">
</colgroup>
<tbody>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xpath.html#pyspark.sql.functions.xpath" title="pyspark.sql.functions.xpath"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xpath</span></code></a>(xml,&nbsp;path)</p></td>
<td><p>Returns a string array of values within the nodes of xml that match the XPath expression.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xpath_boolean.html#pyspark.sql.functions.xpath_boolean" title="pyspark.sql.functions.xpath_boolean"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xpath_boolean</span></code></a>(xml,&nbsp;path)</p></td>
<td><p>Returns true if the XPath expression evaluates to true, or if a matching node is found.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xpath_double.html#pyspark.sql.functions.xpath_double" title="pyspark.sql.functions.xpath_double"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xpath_double</span></code></a>(xml,&nbsp;path)</p></td>
<td><p>Returns a double value, the value zero if no match is found, or NaN if a match is found but the value is non-numeric.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xpath_float.html#pyspark.sql.functions.xpath_float" title="pyspark.sql.functions.xpath_float"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xpath_float</span></code></a>(xml,&nbsp;path)</p></td>
<td><p>Returns a float value, the value zero if no match is found, or NaN if a match is found but the value is non-numeric.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xpath_int.html#pyspark.sql.functions.xpath_int" title="pyspark.sql.functions.xpath_int"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xpath_int</span></code></a>(xml,&nbsp;path)</p></td>
<td><p>Returns an integer value, or the value zero if no match is found, or a match is found but the value is non-numeric.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xpath_long.html#pyspark.sql.functions.xpath_long" title="pyspark.sql.functions.xpath_long"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xpath_long</span></code></a>(xml,&nbsp;path)</p></td>
<td><p>Returns a long integer value, or the value zero if no match is found, or a match is found but the value is non-numeric.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xpath_number.html#pyspark.sql.functions.xpath_number" title="pyspark.sql.functions.xpath_number"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xpath_number</span></code></a>(xml,&nbsp;path)</p></td>
<td><p>Returns a double value, the value zero if no match is found, or NaN if a match is found but the value is non-numeric.</p></td>
</tr>
<tr class="row-even"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xpath_short.html#pyspark.sql.functions.xpath_short" title="pyspark.sql.functions.xpath_short"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xpath_short</span></code></a>(xml,&nbsp;path)</p></td>
<td><p>Returns a short integer value, or the value zero if no match is found, or a match is found but the value is non-numeric.</p></td>
</tr>
<tr class="row-odd"><td><p><a class="reference internal" href="api/pyspark.sql.functions.xpath_string.html#pyspark.sql.functions.xpath_string" title="pyspark.sql.functions.xpath_string"><code class="xref py py-obj docutils literal notranslate"><span class="pre">xpath_string</span></code></a>(xml,&nbsp;path)</p></td>
<td><p>Returns the text contents of the first xml node that matches the XPath expression.</p></td>
</tr>
</tbody>
</table>
</section>
</section>
</div>
</main>
