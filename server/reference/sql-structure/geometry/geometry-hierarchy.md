---
icon: earth-africa
---

# Geometry Hierarchy

## Description

Geometry is the base class. It is an abstract class. The instantiable\
subclasses of Geometry are restricted to zero-, one-, and\
two-dimensional geometric objects that exist in two-dimensional\
coordinate space. All instantiable geometry classes are defined so\
that valid instances of a geometry class are topologically closed\
(that is, all defined geometries include their boundary).

The base Geometry class has subclasses for Point, Curve, Surface, and\
GeometryCollection:

* [Point](../../sql-statements/geometry-constructors/geometry-constructors/point.md) represents zero-dimensional objects.
* Curve represents one-dimensional objects, and has subclass [LineString](../../sql-statements/geometry-constructors/geometry-constructors/linestring.md), with sub-subclasses Line and LinearRing.
* Surface is designed for two-dimensional objects and has subclass [Polygon](../../sql-statements/geometry-constructors/geometry-constructors/polygon.md).
* [GeometryCollection](../../sql-statements/geometry-constructors/geometry-constructors/geometrycollection.md) has specialized zero-, one-, and two-dimensional collection classes named [MultiPoint](../../sql-statements/geometry-constructors/geometry-constructors/multipoint.md), [MultiLineString](../../sql-statements/geometry-constructors/geometry-constructors/multilinestring.md), and [MultiPolygon](../../sql-statements/geometry-constructors/geometry-constructors/multipolygon.md) for modeling geometries corresponding to collections of Points, LineStrings, and Polygons, respectively. MultiCurve and MultiSurface are introduced as abstract superclasses that generalize the collection interfaces to handle Curves and Surfaces.

Geometry, Curve, Surface, MultiCurve, and MultiSurface are defined as\
non-instantiable classes. They define a common set of methods for\
their subclasses and are included for extensibility.

[Point](point-properties/), [LineString](linestring-properties/), [Polygon](polygon-properties/), [GeometryCollection](../../sql-statements/geometry-constructors/geometry-constructors/geometrycollection.md), [MultiPoint](../../sql-statements/geometry-constructors/geometry-constructors/multipoint.md),[MultiLineString](../../sql-statements/geometry-constructors/geometry-constructors/multilinestring.md), and [MultiPolygon](../../sql-statements/geometry-constructors/geometry-constructors/multipolygon.md) are instantiable classes.

GPLv2 fill\_help\_tables.sql
