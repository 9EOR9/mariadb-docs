# VEC\_DISTANCE\_COSINE

{% include "https://app.gitbook.com/s/GxVnu02ec8KJuFSxmB93/~/reusable/pBQsCgBA6SJpi0m3pZuk/" %}

**MariaDB starting with** [**11.7**](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117)

Vectors were introduced in [MariaDB 11.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117)

## Syntax

```
VEC_DISTANCE_COSINE(v, s)
```

## Description

`VEC_Distance_Cosine` is an SQL function that calculates a [Cosine distance](https://en.wikipedia.org/wiki/Cosine_similarity#Cosine_distance) between two vectors.

Vectors must be of the same length, a distance between two vectors of different lengths is not defined and `VEC_Distance_Cosine` will return `NULL` in such a case.

If the vector index was not built for the cosine function (see [CREATE TABLE with Vectors](../create-table-with-vectors.md)), the index will not be used, and a full table scan performed instead. The [VEC\_DISTANCE](vector-functions-vec_distance.md) function is a generic function that behaves either as [VEC\_DISTANCE\_EUCLIDEAN](vec_distance_euclidean.md) or VEC\_DISTANCE\_COSINE, depending on the underlying index type.

## Example

```
select vec_distance_cosine(vec_fromtext('[1,2,3]'), vec_fromtext('[3,5,7]'));
+-----------------------------------------------------------------------+
| vec_distance_cosine(vec_fromtext('[1,2,3]'), vec_fromtext('[3,5,7]')) |
+-----------------------------------------------------------------------+
|                                                   0.00258509695694209 |
+-----------------------------------------------------------------------+
```

## See Also

* [VEC\_DISTANCE](vector-functions-vec_distance.md)
* [VEC\_DISTANCE\_EUCLIDEAN](vec_distance_euclidean.md)
* [Vector Overview](../vector-overview.md)
* [CREATE TABLE with Vectors](../create-table-with-vectors.md)

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
