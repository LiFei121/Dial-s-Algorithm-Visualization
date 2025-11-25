# Dial's Algorithm Visualization

This project contains two interactive visualizations of Dial's algorithm for finding shortest paths in weighted graphs:

1. **DialBuckets.html** - Single-level bucket implementation
2. **DialBucketsTwoLevel.html** - Two-level bucket (super bucket + bucket) implementation

## How to Run

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari)
- No additional dependencies or installation required

### Running the Visualizations

1. **Option 1: Direct File Opening**
   - Simply double-click on either HTML file to open it in your default web browser
   - Or right-click and select "Open with" → choose your preferred browser

2. **Option 2: Using a Local Web Server (Recommended)**
   - If you have Python installed:
     ```bash
     # Python 3
     python -m http.server 8000
     
     # Python 2
     python -m SimpleHTTPServer 8000
     ```
   - Then open your browser and navigate to:
     ```
     http://localhost:8000/DialBuckets.html
     # or
     http://localhost:8000/DialBucketsTwoLevel.html
     ```
## Features

### DialBuckets.html (Single-Level Buckets)
- Interactive graph visualization with draggable nodes
- Step-by-step visualization of Dial's algorithm
- Real-time bucket structure display
- Play/Pause controls with adjustable speed
- Random graph generation
- Two modes: Tracked min_bucket or Sequential scan

### DialBucketsTwoLevel.html (Two-Level Buckets)
- All features from single-level version
- Two-level bucket structure (super buckets + buckets)
- Adjustable block size (b parameter)
- Enhanced visualization showing block-level operations

## Usage Instructions

1. **View the Graph**: The weighted directed graph is displayed in the main panel
2. **Control the Algorithm**:
   - Click "Next" to advance step by step
   - Click "Previous" to go back
   - Click "Play" to auto-play the algorithm
   - Adjust the speed slider to control playback speed
   - Click "Reset" to restart from the beginning
3. **Generate Random Graphs**:
   - Adjust the number of nodes and edges
   - Click "Generate Random Graph" to create a new graph
4. **Switch Modes**:
   - Use the "min_bucket Mode" dropdown to switch between:
     - **Track min bucket**: Highlights the current minimum bucket
     - **Sequential scan**: Animates the scanning process

## File Structure

```
.
├── README.md                    # This file
├── DialBuckets.html            # Single-level bucket visualization
├── DialBucketsTwoLevel.html    # Two-level bucket visualization
├── visualPages.css             # Shared CSS styles
└── bit.png                     # School logo image
```

## Algorithm Overview

Dial's algorithm is an efficient shortest path algorithm for graphs with non-negative integer edge weights. It uses a bucket-based data structure where:

- **Single-level**: Nodes are placed in buckets based on their distance from the source
- **Two-level**: Buckets are organized into blocks (super buckets) for better efficiency

The algorithm maintains:
- Distance array: shortest known distance to each node
- Bucket structure: nodes organized by distance
- Settled set: nodes with finalized shortest paths

