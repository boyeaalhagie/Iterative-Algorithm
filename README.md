# Introduction
Determining if a point is inside a polygon is a common problem in computer graphics, geospatial analysis, and computational geometry. This project implements the Ray Casting Algorithm, a simple yet effective method to solve this problem. Given a polygon and a test point, the algorithm can quickly determine whether the point lies inside or outside the polygon.

The Ray Casting Algorithm is based on the principle of drawing an imaginary ray from the test point to infinity in one direction and counting how many times the ray intersects the edges of the polygon.

# Algorithm Overview
**Draw a Ray**: From the test point, draw an imaginary horizontal ray extending to the right (infinity).

**Count Intersections**: Count how many times the ray intersects the edges of the polygon.

**Determine Position**:
- *Odd Number of Intersections*: If the ray crosses the polygon edges an odd number of times, the point is inside the polygon.
- *Even Number of Intersections*: If the ray crosses an even number of times, the point is outside the polygon.

The logic behind this is that if a point is inside the polygon, a ray extending outward must pass through an edge to leave the polygon and must cross again to re-enter if it continues. Therefore, if it crosses once (odd), it's inside. If it crosses twice (even), it's outside.

![image](https://github.com/user-attachments/assets/1483c9b4-a43e-4e9a-966f-b4c3a1b90244)

The image above demonstrates this principle with various scenarios:

**Inside**: The ray crosses the polygon edge once, indicating the point is inside.

**Outside**: The ray crosses the polygon edges twice, meaning the point is outside.

This algorithm handles complex and concave polygons, making it a versatile solution for point-in-polygon problems.


