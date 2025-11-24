# 3D Body Scan Comparative Analysis

A Python-based computational geometry tool for quantitative comparison of 3D body scans using advanced geometric algorithms.

## Overview

This project analyzes and compares two 3D body scans (OBJ format) to quantify morphological differences with a focus on the torso region. It employs mathematical algorithms to provide objective, comprehensive measurements across multiple dimensions.

## Features

- **Geometric Analysis**: Utilizes Convex Hull algorithm for precise cross-sectional measurements
- **Volume Estimation**: Trapezoidal integration across 80 height slices for accurate volume calculation
- **Multi-Metric Assessment**: 
  - Torso volume (liters)
  - Cross-sectional area (cm²)
  - Circumference (cm)
  - Width and depth measurements (mm)
- **Interactive Visualizations**: 3D and 2D plots using Plotly for data exploration
- **JSON Export**: Structured output of all analysis results

## Methodology

The analysis pipeline:
1. Loads 3D body scans from OBJ files
2. Extracts torso region based on configurable height percentiles
3. Generates 80 horizontal slices across the torso height
4. Computes convex hull for each cross-section
5. Calculates geometric properties (area, perimeter, width, depth)
6. Integrates measurements to estimate total volume
7. Produces comparative visualizations and exports results

## Requirements

```bash
pip install trimesh shapely pyglet numpy plotly
```

## Usage

1. Place your OBJ scan files (`scan1.obj`, `scan2.obj`) in the notebook directory
2. Open and run `body_scan_analysis_FINAL.ipynb`
3. Review interactive visualizations
4. Export results to `analysis_results.json`

## Input Format

- **File Type**: OBJ (Wavefront Object files)
- **Requirements**: 3D mesh with vertices (v), faces (f), and optionally normals (vn) and texture coordinates (vt)

## Output

The analysis generates:
- Interactive 3D mesh visualizations
- Comparative line plots for all metrics
- JSON file with comprehensive measurements:
  - Individual scan statistics
  - Percentage differences between scans
  - Height ranges and average measurements

## Applications

- Body composition research
- Garment sizing and fashion design
- Clinical assessment and health tracking
- Fitness progress monitoring
- Ergonomic product design

## Customization

Key parameters can be adjusted in the code:
- `lower_percentile` / `upper_percentile`: Define torso extraction region
- `num_slices`: Control analysis granularity (default: 80)
- Height ranges: Focus on specific body regions

## Author

**Vincent Techo**

## License

This project is available for educational and research purposes.
