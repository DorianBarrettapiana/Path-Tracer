# Ray Tracing in One Weekend - Ray Tracer Implementation

This repository contains a C++ ray tracing project based on the *Ray Tracing in One Weekend* ebook by Peter Shirley. The goal of this project is to build a simple yet functional ray tracer from scratch, with a focus on rendering spheres, managing objects, and simulating basic lighting and shading.

## Overview

The project is structured around a few key components:
- **Rays**: Represented by the `ray` class, rays are cast from the camera into the scene to determine if they intersect any objects.
- **Hittable Objects**: Objects that can be "hit" by rays, such as spheres, are represented by the `hittable` interface. Each object must implement the `hit()` function to calculate intersections.
- **Scene Management**: The `hittable_list` class manages multiple objects in the scene, testing for the closest intersection between rays and objects.
- **Shading**: Basic shading is calculated based on the normal vector at the intersection point.

### Features

- **Ray-Sphere Intersection**: Detect if and where a ray intersects a sphere.
- **Surface Normals**: Calculate surface normals at the point of intersection to simulate basic shading.
- **Scene Management**: Handle multiple objects in the scene using the `hittable_list`.
- **Color Gradients**: Implement basic color gradients for the sky background.

## File Structure

The project includes the following key files:

- **`main.cpp`**: The main entry point of the ray tracer. It sets up the scene, the camera, and handles the image output.
- **`color.h`**: Utility functions for handling color and writing the final image in PPM format.
- **`header.h`**: Includes standard library headers and constants used across the project.
- **`hittable.h`**: Abstract base class for objects that can be hit by rays. Defines the `hit_record` structure.
- **`hittable_list.h`**: A container for multiple `hittable` objects. Implements the `hit()` function to check for intersections with any object in the list.
- **`interval.h`**: Defines helper functions for working with floating-point intervals, used in ray-object intersection calculations.
- **`ray.h`**: Defines the `ray` class, representing a ray with an origin and direction.
- **`sphere.h`**: Implements a sphere as a `hittable` object, including the intersection logic.
- **`vec3.h`**: A 3D vector class for handling points and vectors in 3D space. Provides vector arithmetic, dot products, and normalization.

## How to Build

To compile and run the ray tracer, ensure you have a C++ compiler installed.

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Nayrhode/Path-Tracer.git
   cd Path-Tracer
