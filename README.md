This code implements a web-based graph visualization using the Sigma.js library using a Gephi GEXF output. The data is from the Letters 1916 project. Sigma.js is a lightweight JavaScript library for creating and rendering graphs in web browsers. The script is a functional implementation of a graph visualization system with features like filtering, node interaction, and graph rendering.

### Key Features:

1.  **Graph Rendering:**
    
    *   The graph is rendered using the Sigma.js library, with support for multiple renderers such as Canvas, WebGL, and SVG.
        
2.  **Node and Edge Customization:**
    
    *   Nodes and edges are drawn with custom styles, including borders, colors, and labels.
        
    *   A custom renderer (sigma.canvas.nodes.border) is defined for nodes, adding borders with adjustable colors and widths.
        
3.  **Dynamic Filters:**
    
    *   A **degree filter** adjusts the visibility of nodes based on their connection degree (number of edges).
        
    *   A **category filter** displays nodes based on specific labels or categories.
        
4.  **Interactive Features:**
    
    *   **Node Highlighting:** Clicking a node highlights its neighbors while graying out non-neighbors.
        
    *   **Reset:** Clicking the canvas resets the graph to its original colors.
        
    *   **Export:** Provides a feature to export the current filter chain as JSON.
        
5.  **User Interface:**
    
    *   A control panel with sliders and dropdown menus is used for adjusting filters and exporting data.
        
    *   The control panel also displays the degree range and allows selection of node categories.
        
6.  **Graph Parsing:**
    
    *   The graph data is loaded from a .gexf file (letterToTopic.gexf) using the Sigma GEXF parser plugin.
        
7.  **Sigma.js Plugins:**
    
    *   The sigma.plugins.filter plugin is used for implementing graph filtering based on conditions.
        
    *   The sigma.parsers.gexf plugin parses GEXF files to load graph data.
        

### Functional Details:

1.  **Graph Initialization:**
    
    *   The graph is initialized and rendered using Sigma.js's sigma.parsers.gexf() method.
        
    *   Settings like node size, edge size, zoom ratio, and edge type are configured.
        
2.  **Node and Edge Behavior:**
    
    *   Each node and edge has an originalColor property that stores its default color. This is used to reset the graph to its initial state.
        
3.  **Interactive UI Elements:**
    
    *   A slider (min-degree) lets users filter nodes based on degree.
        
    *   A dropdown (node-category) filters nodes by their labels.
        
    *   Buttons allow users to reset filters or export the current filter settings.
        
4.  **Event Handling:**
    
    *   Node and stage clicks trigger events to highlight nodes or reset the graph.
        
    *   Slider and dropdown changes trigger filtering.
        
5.  **Graph Methods:**
    
    *   A custom graph method, neighbors, is added to retrieve all neighboring nodes of a specific node.
        

### Code Organization:

*   **Head Section:**
    
    *   Loads Sigma.js core, plugins, and stylesheets.
        
*   **Body Section:**
    
    *   Contains HTML elements for the graph container (sigma-container) and the control panel (control-pane).
        
*   **JavaScript Section:**
    
    *   Includes all the logic for graph rendering, filtering, and interaction.
        

### Requirements:

1.  **Dependencies:**
    
    *   Sigma.js library and its associated plugins are required.
        
    *   GEXF file (letterToTopic.gexf) must be in the correct format and accessible.
        
2.  **Browser Compatibility:**
    
    *   Modern browsers with support for Canvas and WebGL are required for proper rendering.
        

### Usage:

1.  Place the code in an HTML file.
    
2.  Ensure the letterToTopic.gexf file and required scripts are correctly placed in the referenced paths.
    
3.  Open the HTML file in a web browser to view and interact with the graph.
    

### Application:

This script is particularly useful for visualizing complex networks like:

*   Social networks
    
*   Collaboration networks
    
*   Citation or communication networks
    
*   Topic or text analysis graphs
