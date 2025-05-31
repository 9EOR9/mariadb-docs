# VEC\_DISTANCE

**MariaDB starting with** [**11.8**](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/mariadb-11-8-series/what-is-mariadb-118)

VEC\_DISTANCE was introduced in [MariaDB 11.8](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/mariadb-11-8-series/what-is-mariadb-118).

## Syntax

```
VEC_DISTANCE(v, s)
```

## Description

`VEC_DISTANCE` is a generic function that will behave either as [VEC\_DISTANCE\_EUCLIDEAN](vec_distance_euclidean.md), calculating the Euclidean (L2) distance between two points. or [VEC\_DISTANCE\_COSINE](vec_distance_cosine.md), calculating the Cosine distance between two vectors, depending on the underlying index type.

If the underlying index cannot be determined, an [error 4206](../../../mariadb-internals/using-mariadb-with-your-programs-api/error-codes/mariadb-error-codes-4200-to-4299/e4206.md) is returned:

```
ERROR 4206 (HY000): Cannot determine distance type for VEC_DISTANCE, index is not found
```

## Example

```
INSERT INTO v VALUES 
     (1, x'e360d63ebe554f3fcdbc523f4522193f5236083d'),
     (2, x'f511303f72224a3fdd05fe3eb22a133ffae86a3f'),
     (3,x'f09baa3ea172763f123def3e0c7fe53e288bf33e'),
     (4,x'b97a523f2a193e3eb4f62e3f2d23583e9dd60d3f'),
     (5,x'f7c5df3e984b2b3e65e59d3d7376db3eac63773e'),
     (6,x'de01453ffa486d3f10aa4d3fdd66813c71cb163f'),
     (7,x'76edfc3e4b57243f10f8423fb158713f020bda3e'),
     (8,x'56926c3fdf098d3e2c8c5e3d1ad4953daa9d0b3e'),
     (9,x'7b713f3e5258323f80d1113d673b2b3f66e3583f'),
     (10,x'6ca1d43e9df91b3fe580da3e1c247d3f147cf33e');

SELECT id FROM v 
  ORDER BY VEC_DISTANCE(v, x'6ca1d43e9df91b3fe580da3e1c247d3f147cf33e');
+----+
| id |
+----+
| 10 |
|  7 |
|  3 |
|  9 |
|  2 |
|  1 |
|  5 |
|  4 |
|  6 |
|  8 |
+----+
```

## See Also

* [VEC\_DISTANCE\_COSINE](vec_distance_cosine.md)
* [VEC\_DISTANCE\_EUCLIDEAN](vec_distance_euclidean.md)
* [Vector Overview](../vector-overview.md)
* [CREATE TABLE with Vectors](../create-table-with-vectors.md)

CC BY-SA / Gnu FDL
