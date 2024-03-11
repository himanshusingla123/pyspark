## Functions
A collections of builtin functions available for DataFrame operations. From Apache Spark 3.5.0, all functions support Spark Connect.

Normal Functions
col(col)

Returns a Column based on the given column name.

column(col)

Returns a Column based on the given column name.

lit(col)

Creates a Column of literal value.

broadcast(df)

Marks a DataFrame as small enough for use in broadcast joins.

coalesce(*cols)

Returns the first column that is not null.

input_file_name()

Creates a string column for the file name of the current Spark task.

isnan(col)

An expression that returns true if the column is NaN.

isnull(col)

An expression that returns true if the column is null.

monotonically_increasing_id()

A column that generates monotonically increasing 64-bit integers.

named_struct(*cols)

Creates a struct with the given field names and values.

nanvl(col1, col2)

Returns col1 if it is not NaN, or col2 if col1 is NaN.

rand([seed])

Generates a random column with independent and identically distributed (i.i.d.) samples uniformly distributed in [0.0, 1.0).

randn([seed])

Generates a column with independent and identically distributed (i.i.d.) samples from the standard normal distribution.

spark_partition_id()

A column for partition ID.

when(condition, value)

Evaluates a list of conditions and returns one of multiple possible result expressions.

bitwise_not(col)

Computes bitwise not.

bitwiseNOT(col)

Computes bitwise not.

expr(str)

Parses the expression string into the column that it represents

greatest(*cols)

Returns the greatest value of the list of column names, skipping null values.

least(*cols)

Returns the least value of the list of column names, skipping null values.

Math Functions
sqrt(col)

Computes the square root of the specified float value.

abs(col)

Computes the absolute value.

acos(col)

Computes inverse cosine of the input column.

acosh(col)

Computes inverse hyperbolic cosine of the input column.

asin(col)

Computes inverse sine of the input column.

asinh(col)

Computes inverse hyperbolic sine of the input column.

atan(col)

Compute inverse tangent of the input column.

atanh(col)

Computes inverse hyperbolic tangent of the input column.

atan2(col1, col2)

New in version 1.4.0.

bin(col)

Returns the string representation of the binary value of the given column.

cbrt(col)

Computes the cube-root of the given value.

ceil(col)

Computes the ceiling of the given value.

ceiling(col)

Computes the ceiling of the given value.

conv(col, fromBase, toBase)

Convert a number in a string column from one base to another.

cos(col)

Computes cosine of the input column.

cosh(col)

Computes hyperbolic cosine of the input column.

cot(col)

Computes cotangent of the input column.

csc(col)

Computes cosecant of the input column.

e()

Returns Euler’s number.

exp(col)

Computes the exponential of the given value.

expm1(col)

Computes the exponential of the given value minus one.

factorial(col)

Computes the factorial of the given value.

floor(col)

Computes the floor of the given value.

hex(col)

Computes hex value of the given column, which could be pyspark.sql.types.StringType, pyspark.sql.types.BinaryType, pyspark.sql.types.IntegerType or pyspark.sql.types.LongType.

unhex(col)

Inverse of hex.

hypot(col1, col2)

Computes sqrt(a^2 + b^2) without intermediate overflow or underflow.

ln(col)

Returns the natural logarithm of the argument.

log(arg1[, arg2])

Returns the first argument-based logarithm of the second argument.

log10(col)

Computes the logarithm of the given value in Base 10.

log1p(col)

Computes the natural logarithm of the “given value plus one”.

log2(col)

Returns the base-2 logarithm of the argument.

negate(col)

Returns the negative value.

negative(col)

Returns the negative value.

pi()

Returns Pi.

pmod(dividend, divisor)

Returns the positive value of dividend mod divisor.

positive(col)

Returns the value.

pow(col1, col2)

Returns the value of the first argument raised to the power of the second argument.

power(col1, col2)

Returns the value of the first argument raised to the power of the second argument.

rint(col)

Returns the double value that is closest in value to the argument and is equal to a mathematical integer.

round(col[, scale])

Round the given value to scale decimal places using HALF_UP rounding mode if scale >= 0 or at integral part when scale < 0.

bround(col[, scale])

Round the given value to scale decimal places using HALF_EVEN rounding mode if scale >= 0 or at integral part when scale < 0.

sec(col)

Computes secant of the input column.

shiftleft(col, numBits)

Shift the given value numBits left.

shiftright(col, numBits)

(Signed) shift the given value numBits right.

shiftrightunsigned(col, numBits)

Unsigned shift the given value numBits right.

sign(col)

Computes the signum of the given value.

signum(col)

Computes the signum of the given value.

sin(col)

Computes sine of the input column.

sinh(col)

Computes hyperbolic sine of the input column.

tan(col)

Computes tangent of the input column.

tanh(col)

Computes hyperbolic tangent of the input column.

toDegrees(col)

New in version 1.4.0.

try_add(left, right)

Returns the sum of left`and `right and the result is null on overflow.

try_avg(col)

Returns the mean calculated from values of a group and the result is null on overflow.

try_divide(left, right)

Returns dividend/divisor.

try_multiply(left, right)

Returns left`*`right and the result is null on overflow.

try_subtract(left, right)

Returns left-right and the result is null on overflow.

try_sum(col)

Returns the sum calculated from values of a group and the result is null on overflow.

try_to_binary(col[, format])

This is a special version of to_binary that performs the same operation, but returns a NULL value instead of raising an error if the conversion cannot be performed.

try_to_number(col, format)

Convert string ‘col’ to a number based on the string format format.

degrees(col)

Converts an angle measured in radians to an approximately equivalent angle measured in degrees.

toRadians(col)

New in version 1.4.0.

radians(col)

Converts an angle measured in degrees to an approximately equivalent angle measured in radians.

width_bucket(v, min, max, numBucket)

Returns the bucket number into which the value of this expression would fall after being evaluated.

Datetime Functions
add_months(start, months)

Returns the date that is months months after start.

convert_timezone(sourceTz, targetTz, sourceTs)

Converts the timestamp without time zone sourceTs from the sourceTz time zone to targetTz.

curdate()

Returns the current date at the start of query evaluation as a DateType column.

current_date()

Returns the current date at the start of query evaluation as a DateType column.

current_timestamp()

Returns the current timestamp at the start of query evaluation as a TimestampType column.

current_timezone()

Returns the current session local timezone.

date_add(start, days)

Returns the date that is days days after start.

date_diff(end, start)

Returns the number of days from start to end.

date_format(date, format)

Converts a date/timestamp/string to a value of string in the format specified by the date format given by the second argument.

date_from_unix_date(days)

Create date from the number of days since 1970-01-01.

date_sub(start, days)

Returns the date that is days days before start.

date_trunc(format, timestamp)

Returns timestamp truncated to the unit specified by the format.

dateadd(start, days)

Returns the date that is days days after start.

datediff(end, start)

Returns the number of days from start to end.

day(col)

Extract the day of the month of a given date/timestamp as integer.

date_part(field, source)

Extracts a part of the date/timestamp or interval source.

datepart(field, source)

Extracts a part of the date/timestamp or interval source.

dayofmonth(col)

Extract the day of the month of a given date/timestamp as integer.

dayofweek(col)

Extract the day of the week of a given date/timestamp as integer.

dayofyear(col)

Extract the day of the year of a given date/timestamp as integer.

extract(field, source)

Extracts a part of the date/timestamp or interval source.

second(col)

Extract the seconds of a given date as integer.

weekofyear(col)

Extract the week number of a given date as integer.

year(col)

Extract the year of a given date/timestamp as integer.

quarter(col)

Extract the quarter of a given date/timestamp as integer.

month(col)

Extract the month of a given date/timestamp as integer.

last_day(date)

Returns the last day of the month which the given date belongs to.

localtimestamp()

Returns the current timestamp without time zone at the start of query evaluation as a timestamp without time zone column.

make_dt_interval([days, hours, mins, secs])

Make DayTimeIntervalType duration from days, hours, mins and secs.

make_interval([years, months, weeks, days, …])

Make interval from years, months, weeks, days, hours, mins and secs.

make_timestamp(years, months, days, hours, …)

Create timestamp from years, months, days, hours, mins, secs and timezone fields.

make_timestamp_ltz(years, months, days, …)

Create the current timestamp with local time zone from years, months, days, hours, mins, secs and timezone fields.

make_timestamp_ntz(years, months, days, …)

Create local date-time from years, months, days, hours, mins, secs fields.

make_ym_interval([years, months])

Make year-month interval from years, months.

minute(col)

Extract the minutes of a given timestamp as integer.

months_between(date1, date2[, roundOff])

Returns number of months between dates date1 and date2.

next_day(date, dayOfWeek)

Returns the first date which is later than the value of the date column based on second week day argument.

hour(col)

Extract the hours of a given timestamp as integer.

make_date(year, month, day)

Returns a column with a date built from the year, month and day columns.

now()

Returns the current timestamp at the start of query evaluation.

from_unixtime(timestamp[, format])

Converts the number of seconds from unix epoch (1970-01-01 00:00:00 UTC) to a string representing the timestamp of that moment in the current system time zone in the given format.

unix_timestamp([timestamp, format])

Convert time string with given pattern (‘yyyy-MM-dd HH:mm:ss’, by default) to Unix time stamp (in seconds), using the default timezone and the default locale, returns null if failed.

to_unix_timestamp(timestamp[, format])

Returns the UNIX timestamp of the given time.

to_timestamp(col[, format])

Converts a Column into pyspark.sql.types.TimestampType using the optionally specified format.

to_timestamp_ltz(timestamp[, format])

Parses the timestamp with the format to a timestamp without time zone.

to_timestamp_ntz(timestamp[, format])

Parses the timestamp with the format to a timestamp without time zone.

to_date(col[, format])

Converts a Column into pyspark.sql.types.DateType using the optionally specified format.

trunc(date, format)

Returns date truncated to the unit specified by the format.

from_utc_timestamp(timestamp, tz)

This is a common function for databases supporting TIMESTAMP WITHOUT TIMEZONE.

to_utc_timestamp(timestamp, tz)

This is a common function for databases supporting TIMESTAMP WITHOUT TIMEZONE.

weekday(col)

Returns the day of the week for date/timestamp (0 = Monday, 1 = Tuesday, …, 6 = Sunday).

window(timeColumn, windowDuration[, …])

Bucketize rows into one or more time windows given a timestamp specifying column.

session_window(timeColumn, gapDuration)

Generates session window given a timestamp specifying column.

timestamp_micros(col)

Creates timestamp from the number of microseconds since UTC epoch.

timestamp_millis(col)

Creates timestamp from the number of milliseconds since UTC epoch.

timestamp_seconds(col)

Converts the number of seconds from the Unix epoch (1970-01-01T00:00:00Z) to a timestamp.

try_to_timestamp(col[, format])

Parses the col with the format to a timestamp.

unix_date(col)

Returns the number of days since 1970-01-01.

unix_micros(col)

Returns the number of microseconds since 1970-01-01 00:00:00 UTC.

unix_millis(col)

Returns the number of milliseconds since 1970-01-01 00:00:00 UTC.

unix_seconds(col)

Returns the number of seconds since 1970-01-01 00:00:00 UTC.

window_time(windowColumn)

Computes the event time from a window column.

Collection Functions
array(*cols)

Creates a new array column.

array_contains(col, value)

Collection function: returns null if the array is null, true if the array contains the given value, and false otherwise.

arrays_overlap(a1, a2)

Collection function: returns true if the arrays contain any common non-null element; if not, returns null if both the arrays are non-empty and any of them contains a null element; returns false otherwise.

array_join(col, delimiter[, null_replacement])

Concatenates the elements of column using the delimiter.

create_map(*cols)

Creates a new map column.

slice(x, start, length)

Collection function: returns an array containing all the elements in x from index start (array indices start at 1, or from the end if start is negative) with the specified length.

concat(*cols)

Concatenates multiple input columns together into a single column.

array_position(col, value)

Collection function: Locates the position of the first occurrence of the given value in the given array.

element_at(col, extraction)

Collection function: Returns element of array at given index in extraction if col is array.

array_append(col, value)

Collection function: returns an array of the elements in col1 along with the added element in col2 at the last of the array.

array_size(col)

Returns the total number of elements in the array.

array_sort(col[, comparator])

Collection function: sorts the input array in ascending order.

array_insert(arr, pos, value)

Collection function: adds an item into a given array at a specified array index.

array_remove(col, element)

Collection function: Remove all elements that equal to element from the given array.

array_prepend(col, value)

Collection function: Returns an array containing element as well as all elements from array.

array_distinct(col)

Collection function: removes duplicate values from the array.

array_intersect(col1, col2)

Collection function: returns an array of the elements in the intersection of col1 and col2, without duplicates.

array_union(col1, col2)

Collection function: returns an array of the elements in the union of col1 and col2, without duplicates.

array_except(col1, col2)

Collection function: returns an array of the elements in col1 but not in col2, without duplicates.

array_compact(col)

Collection function: removes null values from the array.

transform(col, f)

Returns an array of elements after applying a transformation to each element in the input array.

exists(col, f)

Returns whether a predicate holds for one or more elements in the array.

forall(col, f)

Returns whether a predicate holds for every element in the array.

filter(col, f)

Returns an array of elements for which a predicate holds in a given array.

aggregate(col, initialValue, merge[, finish])

Applies a binary operator to an initial state and all elements in the array, and reduces this to a single state.

zip_with(left, right, f)

Merge two given arrays, element-wise, into a single array using a function.

transform_keys(col, f)

Applies a function to every key-value pair in a map and returns a map with the results of those applications as the new keys for the pairs.

transform_values(col, f)

Applies a function to every key-value pair in a map and returns a map with the results of those applications as the new values for the pairs.

map_filter(col, f)

Returns a map whose key-value pairs satisfy a predicate.

map_from_arrays(col1, col2)

Creates a new map from two arrays.

map_zip_with(col1, col2, f)

Merge two given maps, key-wise into a single map using a function.

explode(col)

Returns a new row for each element in the given array or map.

explode_outer(col)

Returns a new row for each element in the given array or map.

posexplode(col)

Returns a new row for each element with position in the given array or map.

posexplode_outer(col)

Returns a new row for each element with position in the given array or map.

inline(col)

Explodes an array of structs into a table.

inline_outer(col)

Explodes an array of structs into a table.

get(col, index)

Collection function: Returns element of array at given (0-based) index.

get_json_object(col, path)

Extracts json object from a json string based on json path specified, and returns json string of the extracted json object.

json_tuple(col, *fields)

Creates a new row for a json column according to the given field names.

from_json(col, schema[, options])

Parses a column containing a JSON string into a MapType with StringType as keys type, StructType or ArrayType with the specified schema.

schema_of_json(json[, options])

Parses a JSON string and infers its schema in DDL format.

to_json(col[, options])

Converts a column containing a StructType, ArrayType or a MapType into a JSON string.

json_array_length(col)

Returns the number of elements in the outermost JSON array.

json_object_keys(col)

Returns all the keys of the outermost JSON object as an array.

size(col)

Collection function: returns the length of the array or map stored in the column.

cardinality(col)

Collection function: returns the length of the array or map stored in the column.

struct(*cols)

Creates a new struct column.

sort_array(col[, asc])

Collection function: sorts the input array in ascending or descending order according to the natural ordering of the array elements.

array_max(col)

Collection function: returns the maximum value of the array.

array_min(col)

Collection function: returns the minimum value of the array.

shuffle(col)

Collection function: Generates a random permutation of the given array.

reverse(col)

Collection function: returns a reversed string or an array with reverse order of elements.

flatten(col)

Collection function: creates a single array from an array of arrays.

sequence(start, stop[, step])

Generate a sequence of integers from start to stop, incrementing by step.

array_repeat(col, count)

Collection function: creates an array containing a column repeated count times.

map_contains_key(col, value)

Returns true if the map contains the key.

map_keys(col)

Collection function: Returns an unordered array containing the keys of the map.

map_values(col)

Collection function: Returns an unordered array containing the values of the map.

map_entries(col)

Collection function: Returns an unordered array of all entries in the given map.

map_from_entries(col)

Collection function: Converts an array of entries (key value struct types) to a map of values.

arrays_zip(*cols)

Collection function: Returns a merged array of structs in which the N-th struct contains all N-th values of input arrays.

map_concat(*cols)

Returns the union of all the given maps.

from_csv(col, schema[, options])

Parses a column containing a CSV string to a row with the specified schema.

schema_of_csv(csv[, options])

Parses a CSV string and infers its schema in DDL format.

str_to_map(text[, pairDelim, keyValueDelim])

Creates a map after splitting the text into key/value pairs using delimiters.

to_csv(col[, options])

Converts a column containing a StructType into a CSV string.

try_element_at(col, extraction)

(array, index) - Returns element of array at given (1-based) index.

Partition Transformation Functions
years(col)

Partition transform function: A transform for timestamps and dates to partition data into years.

months(col)

Partition transform function: A transform for timestamps and dates to partition data into months.

days(col)

Partition transform function: A transform for timestamps and dates to partition data into days.

hours(col)

Partition transform function: A transform for timestamps to partition data into hours.

bucket(numBuckets, col)

Partition transform function: A transform for any type that partitions by a hash of the input column.

Aggregate Functions
any_value(col[, ignoreNulls])

Returns some value of col for a group of rows.

approxCountDistinct(col[, rsd])

New in version 1.3.0.

approx_count_distinct(col[, rsd])

Aggregate function: returns a new Column for approximate distinct count of column col.

approx_percentile(col, percentage[, accuracy])

Returns the approximate percentile of the numeric column col which is the smallest value in the ordered col values (sorted from least to greatest) such that no more than percentage of col values is less than the value or equal to that value.

array_agg(col)

Aggregate function: returns a list of objects with duplicates.

avg(col)

Aggregate function: returns the average of the values in a group.

bit_and(col)

Aggregate function: returns the bitwise AND of all non-null input values, or null if none.

bit_or(col)

Aggregate function: returns the bitwise OR of all non-null input values, or null if none.

bit_xor(col)

Aggregate function: returns the bitwise XOR of all non-null input values, or null if none.

bool_and(col)

Aggregate function: returns true if all values of col are true.

bool_or(col)

Aggregate function: returns true if at least one value of col is true.

collect_list(col)

Aggregate function: returns a list of objects with duplicates.

collect_set(col)

Aggregate function: returns a set of objects with duplicate elements eliminated.

corr(col1, col2)

Returns a new Column for the Pearson Correlation Coefficient for col1 and col2.

count(col)

Aggregate function: returns the number of items in a group.

count_distinct(col, *cols)

Returns a new Column for distinct count of col or cols.

countDistinct(col, *cols)

Returns a new Column for distinct count of col or cols.

count_min_sketch(col, eps, confidence, seed)

Returns a count-min sketch of a column with the given esp, confidence and seed.

count_if(col)

Returns the number of TRUE values for the col.

covar_pop(col1, col2)

Returns a new Column for the population covariance of col1 and col2.

covar_samp(col1, col2)

Returns a new Column for the sample covariance of col1 and col2.

every(col)

Aggregate function: returns true if all values of col are true.

first(col[, ignorenulls])

Aggregate function: returns the first value in a group.

first_value(col[, ignoreNulls])

Returns the first value of col for a group of rows.

grouping(col)

Aggregate function: indicates whether a specified column in a GROUP BY list is aggregated or not, returns 1 for aggregated or 0 for not aggregated in the result set.

grouping_id(*cols)

Aggregate function: returns the level of grouping, equals to

histogram_numeric(col, nBins)

Computes a histogram on numeric ‘col’ using nb bins.

hll_sketch_agg(col[, lgConfigK])

Aggregate function: returns the updatable binary representation of the Datasketches HllSketch configured with lgConfigK arg.

hll_union_agg(col[, allowDifferentLgConfigK])

Aggregate function: returns the updatable binary representation of the Datasketches HllSketch, generated by merging previously created Datasketches HllSketch instances via a Datasketches Union instance.

kurtosis(col)

Aggregate function: returns the kurtosis of the values in a group.

last(col[, ignorenulls])

Aggregate function: returns the last value in a group.

last_value(col[, ignoreNulls])

Returns the last value of col for a group of rows.

max(col)

Aggregate function: returns the maximum value of the expression in a group.

max_by(col, ord)

Returns the value associated with the maximum value of ord.

mean(col)

Aggregate function: returns the average of the values in a group.

median(col)

Returns the median of the values in a group.

min(col)

Aggregate function: returns the minimum value of the expression in a group.

min_by(col, ord)

Returns the value associated with the minimum value of ord.

mode(col)

Returns the most frequent value in a group.

percentile(col, percentage[, frequency])

Returns the exact percentile(s) of numeric column expr at the given percentage(s) with value range in [0.0, 1.0].

percentile_approx(col, percentage[, accuracy])

Returns the approximate percentile of the numeric column col which is the smallest value in the ordered col values (sorted from least to greatest) such that no more than percentage of col values is less than the value or equal to that value.

product(col)

Aggregate function: returns the product of the values in a group.

reduce(col, initialValue, merge[, finish])

Applies a binary operator to an initial state and all elements in the array, and reduces this to a single state.

regr_avgx(y, x)

Aggregate function: returns the average of the independent variable for non-null pairs in a group, where y is the dependent variable and x is the independent variable.

regr_avgy(y, x)

Aggregate function: returns the average of the dependent variable for non-null pairs in a group, where y is the dependent variable and x is the independent variable.

regr_count(y, x)

Aggregate function: returns the number of non-null number pairs in a group, where y is the dependent variable and x is the independent variable.

regr_intercept(y, x)

Aggregate function: returns the intercept of the univariate linear regression line for non-null pairs in a group, where y is the dependent variable and x is the independent variable.

regr_r2(y, x)

Aggregate function: returns the coefficient of determination for non-null pairs in a group, where y is the dependent variable and x is the independent variable.

regr_slope(y, x)

Aggregate function: returns the slope of the linear regression line for non-null pairs in a group, where y is the dependent variable and x is the independent variable.

regr_sxx(y, x)

Aggregate function: returns REGR_COUNT(y, x) * VAR_POP(x) for non-null pairs in a group, where y is the dependent variable and x is the independent variable.

regr_sxy(y, x)

Aggregate function: returns REGR_COUNT(y, x) * COVAR_POP(y, x) for non-null pairs in a group, where y is the dependent variable and x is the independent variable.

regr_syy(y, x)

Aggregate function: returns REGR_COUNT(y, x) * VAR_POP(y) for non-null pairs in a group, where y is the dependent variable and x is the independent variable.

skewness(col)

Aggregate function: returns the skewness of the values in a group.

some(col)

Aggregate function: returns true if at least one value of col is true.

std(col)

Aggregate function: alias for stddev_samp.

stddev(col)

Aggregate function: alias for stddev_samp.

stddev_pop(col)

Aggregate function: returns population standard deviation of the expression in a group.

stddev_samp(col)

Aggregate function: returns the unbiased sample standard deviation of the expression in a group.

sum(col)

Aggregate function: returns the sum of all values in the expression.

sum_distinct(col)

Aggregate function: returns the sum of distinct values in the expression.

sumDistinct(col)

Aggregate function: returns the sum of distinct values in the expression.

var_pop(col)

Aggregate function: returns the population variance of the values in a group.

var_samp(col)

Aggregate function: returns the unbiased sample variance of the values in a group.

variance(col)

Aggregate function: alias for var_samp

Window Functions
cume_dist()

Window function: returns the cumulative distribution of values within a window partition, i.e.

dense_rank()

Window function: returns the rank of rows within a window partition, without any gaps.

lag(col[, offset, default])

Window function: returns the value that is offset rows before the current row, and default if there is less than offset rows before the current row.

lead(col[, offset, default])

Window function: returns the value that is offset rows after the current row, and default if there is less than offset rows after the current row.

nth_value(col, offset[, ignoreNulls])

Window function: returns the value that is the offsetth row of the window frame (counting from 1), and null if the size of window frame is less than offset rows.

ntile(n)

Window function: returns the ntile group id (from 1 to n inclusive) in an ordered window partition.

percent_rank()

Window function: returns the relative rank (i.e.

rank()

Window function: returns the rank of rows within a window partition.

row_number()

Window function: returns a sequential number starting at 1 within a window partition.

Sort Functions
asc(col)

Returns a sort expression based on the ascending order of the given column name.

asc_nulls_first(col)

Returns a sort expression based on the ascending order of the given column name, and null values return before non-null values.

asc_nulls_last(col)

Returns a sort expression based on the ascending order of the given column name, and null values appear after non-null values.

desc(col)

Returns a sort expression based on the descending order of the given column name.

desc_nulls_first(col)

Returns a sort expression based on the descending order of the given column name, and null values appear before non-null values.

desc_nulls_last(col)

Returns a sort expression based on the descending order of the given column name, and null values appear after non-null values.

String Functions
ascii(col)

Computes the numeric value of the first character of the string column.

base64(col)

Computes the BASE64 encoding of a binary column and returns it as a string column.

bit_length(col)

Calculates the bit length for the specified string column.

btrim(str[, trim])

Remove the leading and trailing trim characters from str.

char(col)

Returns the ASCII character having the binary equivalent to col.

character_length(str)

Returns the character length of string data or number of bytes of binary data.

char_length(str)

Returns the character length of string data or number of bytes of binary data.

concat_ws(sep, *cols)

Concatenates multiple input string columns together into a single string column, using the given separator.

contains(left, right)

Returns a boolean.

decode(col, charset)

Computes the first argument into a string from a binary using the provided character set (one of ‘US-ASCII’, ‘ISO-8859-1’, ‘UTF-8’, ‘UTF-16BE’, ‘UTF-16LE’, ‘UTF-16’).

elt(*inputs)

Returns the n-th input, e.g., returns input2 when n is 2.

encode(col, charset)

Computes the first argument into a binary from a string using the provided character set (one of ‘US-ASCII’, ‘ISO-8859-1’, ‘UTF-8’, ‘UTF-16BE’, ‘UTF-16LE’, ‘UTF-16’).

endswith(str, suffix)

Returns a boolean.

find_in_set(str, str_array)

Returns the index (1-based) of the given string (str) in the comma-delimited list (strArray).

format_number(col, d)

Formats the number X to a format like ‘#,–#,–#.–’, rounded to d decimal places with HALF_EVEN round mode, and returns the result as a string.

format_string(format, *cols)

Formats the arguments in printf-style and returns the result as a string column.

ilike(str, pattern[, escapeChar])

Returns true if str matches pattern with escape case-insensitively, null if any arguments are null, false otherwise.

initcap(col)

Translate the first letter of each word to upper case in the sentence.

instr(str, substr)

Locate the position of the first occurrence of substr column in the given string.

lcase(str)

Returns str with all characters changed to lowercase.

length(col)

Computes the character length of string data or number of bytes of binary data.

like(str, pattern[, escapeChar])

Returns true if str matches pattern with escape, null if any arguments are null, false otherwise.

lower(col)

Converts a string expression to lower case.

left(str, len)

Returns the leftmost len`(`len can be string type) characters from the string str, if len is less or equal than 0 the result is an empty string.

levenshtein(left, right[, threshold])

Computes the Levenshtein distance of the two given strings.

locate(substr, str[, pos])

Locate the position of the first occurrence of substr in a string column, after position pos.

lpad(col, len, pad)

Left-pad the string column to width len with pad.

ltrim(col)

Trim the spaces from left end for the specified string value.

mask(col[, upperChar, lowerChar, digitChar, …])

Masks the given string value.

octet_length(col)

Calculates the byte length for the specified string column.

parse_url(url, partToExtract[, key])

Extracts a part from a URL.

position(substr, str[, start])

Returns the position of the first occurrence of substr in str after position start.

printf(format, *cols)

Formats the arguments in printf-style and returns the result as a string column.

rlike(str, regexp)

Returns true if str matches the Java regex regexp, or false otherwise.

regexp(str, regexp)

Returns true if str matches the Java regex regexp, or false otherwise.

regexp_like(str, regexp)

Returns true if str matches the Java regex regexp, or false otherwise.

regexp_count(str, regexp)

Returns a count of the number of times that the Java regex pattern regexp is matched in the string str.

regexp_extract(str, pattern, idx)

Extract a specific group matched by the Java regex regexp, from the specified string column.

regexp_extract_all(str, regexp[, idx])

Extract all strings in the str that match the Java regex regexp and corresponding to the regex group index.

regexp_replace(string, pattern, replacement)

Replace all substrings of the specified string value that match regexp with replacement.

regexp_substr(str, regexp)

Returns the substring that matches the Java regex regexp within the string str.

regexp_instr(str, regexp[, idx])

Extract all strings in the str that match the Java regex regexp and corresponding to the regex group index.

replace(src, search[, replace])

Replaces all occurrences of search with replace.

right(str, len)

Returns the rightmost len`(`len can be string type) characters from the string str, if len is less or equal than 0 the result is an empty string.

ucase(str)

Returns str with all characters changed to uppercase.

unbase64(col)

Decodes a BASE64 encoded string column and returns it as a binary column.

rpad(col, len, pad)

Right-pad the string column to width len with pad.

repeat(col, n)

Repeats a string column n times, and returns it as a new string column.

rtrim(col)

Trim the spaces from right end for the specified string value.

soundex(col)

Returns the SoundEx encoding for a string

split(str, pattern[, limit])

Splits str around matches of the given pattern.

split_part(src, delimiter, partNum)

Splits str by delimiter and return requested part of the split (1-based).

startswith(str, prefix)

Returns a boolean.

substr(str, pos[, len])

Returns the substring of str that starts at pos and is of length len, or the slice of byte array that starts at pos and is of length len.

substring(str, pos, len)

Substring starts at pos and is of length len when str is String type or returns the slice of byte array that starts at pos in byte and is of length len when str is Binary type.

substring_index(str, delim, count)

Returns the substring from string str before count occurrences of the delimiter delim.

overlay(src, replace, pos[, len])

Overlay the specified portion of src with replace, starting from byte position pos of src and proceeding for len bytes.

sentences(string[, language, country])

Splits a string into arrays of sentences, where each sentence is an array of words.

to_binary(col[, format])

Converts the input col to a binary value based on the supplied format.

to_char(col, format)

Convert col to a string based on the format.

to_number(col, format)

Convert string ‘col’ to a number based on the string format ‘format’.

to_varchar(col, format)

Convert col to a string based on the format.

translate(srcCol, matching, replace)

A function translate any character in the srcCol by a character in matching.

trim(col)

Trim the spaces from both ends for the specified string column.

upper(col)

Converts a string expression to upper case.

url_decode(str)

Decodes a str in ‘application/x-www-form-urlencoded’ format using a specific encoding scheme.

url_encode(str)

Translates a string into ‘application/x-www-form-urlencoded’ format using a specific encoding scheme.

Bitwise Functions
bit_count(col)

Returns the number of bits that are set in the argument expr as an unsigned 64-bit integer, or NULL if the argument is NULL.

bit_get(col, pos)

Returns the value of the bit (0 or 1) at the specified position.

getbit(col, pos)

Returns the value of the bit (0 or 1) at the specified position.

Call Functions
call_function(funcName, *cols)

Call a SQL function.

call_udf(udfName, *cols)

Call an user-defined function.

pandas_udf([f, returnType, functionType])

Creates a pandas user defined function (a.k.a.

udf([f, returnType, useArrow])

Creates a user defined function (UDF).

udtf([cls, useArrow])

Creates a user defined table function (UDTF).

unwrap_udt(col)

Unwrap UDT data type column into its underlying type.

Misc Functions
aes_decrypt(input, key[, mode, padding, aad])

Returns a decrypted value of input using AES in mode with padding.

aes_encrypt(input, key[, mode, padding, iv, aad])

Returns an encrypted value of input using AES in given mode with the specified padding.

bitmap_bit_position(col)

Returns the bit position for the given input column.

bitmap_bucket_number(col)

Returns the bucket number for the given input column.

bitmap_construct_agg(col)

Returns a bitmap with the positions of the bits set from all the values from the input column.

bitmap_count(col)

Returns the number of set bits in the input bitmap.

bitmap_or_agg(col)

Returns a bitmap that is the bitwise OR of all of the bitmaps from the input column.

current_catalog()

Returns the current catalog.

current_database()

Returns the current database.

current_schema()

Returns the current database.

current_user()

Returns the current database.

input_file_block_length()

Returns the length of the block being read, or -1 if not available.

input_file_block_start()

Returns the start offset of the block being read, or -1 if not available.

md5(col)

Calculates the MD5 digest and returns the value as a 32 character hex string.

sha(col)

Returns a sha1 hash value as a hex string of the col.

sha1(col)

Returns the hex string result of SHA-1.

sha2(col, numBits)

Returns the hex string result of SHA-2 family of hash functions (SHA-224, SHA-256, SHA-384, and SHA-512).

crc32(col)

Calculates the cyclic redundancy check value (CRC32) of a binary column and returns the value as a bigint.

hash(*cols)

Calculates the hash code of given columns, and returns the result as an int column.

xxhash64(*cols)

Calculates the hash code of given columns using the 64-bit variant of the xxHash algorithm, and returns the result as a long column.

assert_true(col[, errMsg])

Returns null if the input column is true; throws an exception with the provided error message otherwise.

raise_error(errMsg)

Throws an exception with the provided error message.

reflect(*cols)

Calls a method with reflection.

hll_sketch_estimate(col)

Returns the estimated number of unique values given the binary representation of a Datasketches HllSketch.

hll_union(col1, col2[, allowDifferentLgConfigK])

Merges two binary representations of Datasketches HllSketch objects, using a Datasketches Union object.

java_method(*cols)

Calls a method with reflection.

stack(*cols)

Separates col1, …, colk into n rows.

try_aes_decrypt(input, key[, mode, padding, aad])

This is a special version of aes_decrypt that performs the same operation, but returns a NULL value instead of raising an error if the decryption cannot be performed.

typeof(col)

Return DDL-formatted type string for the data type of the input.

user()

Returns the current database.

version()

Returns the Spark version.

Predicate Functions
equal_null(col1, col2)

Returns same result as the EQUAL(=) operator for non-null operands, but returns true if both are null, false if one of the them is null.

ifnull(col1, col2)

Returns col2 if col1 is null, or col1 otherwise.

isnotnull(col)

Returns true if col is not null, or false otherwise.

nullif(col1, col2)

Returns null if col1 equals to col2, or col1 otherwise.

nvl(col1, col2)

Returns col2 if col1 is null, or col1 otherwise.

nvl2(col1, col2, col3)

Returns col2 if col1 is not null, or col3 otherwise.

Xml Functions
xpath(xml, path)

Returns a string array of values within the nodes of xml that match the XPath expression.

xpath_boolean(xml, path)

Returns true if the XPath expression evaluates to true, or if a matching node is found.

xpath_double(xml, path)

Returns a double value, the value zero if no match is found, or NaN if a match is found but the value is non-numeric.

xpath_float(xml, path)

Returns a float value, the value zero if no match is found, or NaN if a match is found but the value is non-numeric.

xpath_int(xml, path)

Returns an integer value, or the value zero if no match is found, or a match is found but the value is non-numeric.

xpath_long(xml, path)

Returns a long integer value, or the value zero if no match is found, or a match is found but the value is non-numeric.

xpath_number(xml, path)

Returns a double value, the value zero if no match is found, or NaN if a match is found but the value is non-numeric.

xpath_short(xml, path)

Returns a short integer value, or the value zero if no match is found, or a match is found but the value is non-numeric.

xpath_string(xml, path)

Returns the text contents of the first xml node that matches the XPath expression.