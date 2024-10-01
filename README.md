# 3D Force Graph Visualization with Dataset Selection and Average Execution Time Calculation

## Overview

This project visualizes 3D graphs using the `3d-force-graph` library, where nodes and links represent data structures, and each dataset is loaded dynamically. Users can select from various datasets and observe the 3D force-directed graph layout. The code measures the execution time of the graph rendering process and displays the **average execution time** after running the graph layout 10 times for the selected dataset.

## Features

1. **Dataset Selection**:
   - A dropdown menu is provided to select different datasets.
   - Each dataset is represented as a 3D force-directed graph, where nodes represent data points, and links represent relationships between them.
   
2. **Average Execution Time Calculation**:
   - When a dataset is selected, the graph rendering process is executed **10 times**.
   - The execution time for each run is recorded.
   - After 10 runs, the **average execution time** is calculated and displayed.

3. **Node Export to CSV**:
   - Users can export the current positions of the graph's nodes (x, y, z coordinates) to a CSV file for further analysis.
   
4. **Node Interaction**:
   - Clicking on a node zooms in on that node, providing a focused view.
   
## Functionality

- **Dropdown Dataset Selector**:
  - Select from a list of pre-defined datasets, such as Bacillus, Agrobacterium, and Yeast datasets.
  - When a new dataset is selected, the graph is rendered with nodes and links based on that dataset.
  
- **Average Execution Time**:
  - The graph layout is calculated 10 times for the selected dataset, and the average time it takes to render the graph is displayed.
  - This functionality allows you to assess how long it takes for the graph layout to stabilize for a given dataset.

- **Node Export**:
  - A button is available to **export node coordinates** (id, x, y, z) to a CSV file for use in external analysis or reporting.

## How to Use

1. **Dataset Selection**:
   - Choose a dataset from the dropdown menu.
   - The graph will automatically load and render the selected dataset.
   - The graph will run 10 times, and the average execution time will be displayed in the section labeled "Execution Time".

2. **Export Node Coordinates**:
   - Click on the **"Export Node Coordinates to CSV"** button.
   - This will generate a CSV file containing the `id`, `x`, `y`, and `z` coordinates of each node in the current graph layout.
   
3. **Node Interaction**:
   - Click on any node to zoom in on it. The view will automatically center on the selected node.

## Code Breakdown

### Main Components:

1. **Dataset Dropdown**:
   - Provides a list of datasets available for rendering as 3D force-directed graphs.

2. **ForceGraph3D Initialization**:
   - Initializes the `ForceGraph3D` component with properties such as node colors, link visibility, and cooldown time for the layout engine.

3. **Execution Time Measurement**:
   - Uses `performance.now()` to record the start and end times for each graph rendering process.
   - Runs the rendering process 10 times and calculates the average execution time.
   
4. **CSV Export**:
   - A button is provided to export the node positions to a CSV file.
   
### Key Functions:

- **`runGraph()`**:
   - This function is responsible for running the graph layout for a selected dataset. It records the execution time for each run and repeats the process 10 times. After 10 runs, the average execution time is displayed.

- **CSV Export Button**:
   - This button triggers the export of node coordinates in the format `id,x,y,z` to a downloadable CSV file.

## Example Datasets

- **Bacillus Full**: A dataset representing the Bacillus genome.
- **Agrobacterium 446**: A dataset representing Hi-C data of the Agrobacterium genome.
- **Yeast WT**: A dataset representing wild-type Yeast data.

More datasets can be added by modifying the `<option>` tags in the dataset selector.

## Technologies Used

- **3d-force-graph**: A JavaScript library for creating 3D force-directed graphs.
- **JavaScript**: Handles the interaction, dataset selection, and execution time measurement.
- **HTML**: Structure of the dropdown selector and export button.
- **CSS**: Simple styling for the page layout and execution time display.

## How to Run

1. Download or clone the repository.
2. Open the `index.html` file in your browser.
3. Select a dataset from the dropdown menu to view the graph.
4. Wait for the graph layout to run 10 times, and the average execution time will be displayed.
5. Optionally, click on the "Export Node Coordinates to CSV" button to download the current graph's node positions.

## Future Enhancements

- Add more datasets to provide a broader range of graph visualizations.
- Introduce more interaction capabilities, such as node highlighting and filtering.
- Optimize the performance of larger datasets by improving layout stabilization.

## License

This project is licensed under the MIT License.

