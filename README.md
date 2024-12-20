Grazioso Salvare Dashboard Project
Overview
This project involves building an interactive dashboard for Grazioso Salvare, allowing the company to visualize animal shelter data dynamically. The dashboard provides functionalities such as filtering rescue types, displaying animal breed distribution through a pie chart, and mapping animal geolocations.
Required Functionality
Achieved Features:
1.	Interactive Filtering: 
o	Users can filter data by rescue types (Water, Mountain, Disaster, or Reset).
2.	Dynamic Data Table: 
o	Displays the filtered data dynamically based on user selection.
3.	Pie Chart: 
o	Visualizes the breed distribution for the filtered dataset.
4.	Geolocation Map: 
o	Maps the latitude and longitude of the selected animal, updating dynamically.
Screencast:
 

Tools and Rationale
1. MongoDB
•	Why MongoDB? 
o	Document-based NoSQL database ideal for storing JSON-like documents.
o	Flexible schema allows dynamic changes in the data structure without breaking the application.
o	Provides efficient indexing and querying for large datasets, ensuring quick data retrieval for the dashboard.
o	Python’s PyMongo library simplifies CRUD operations, enabling seamless integration with the application.
2. Python and Dash Framework
•	Dash Framework: 
o	Open-source framework for building interactive, web-based data visualizations in Python.
o	Combines the interactivity of JavaScript with the power of Python for data analysis.
o	Provides built-in components such as dcc.Graph, dash_table.DataTable, and dash_leaflet.Map.
•	Python: 
o	Core programming language for integrating MongoDB, data processing, and building the dashboard.
o	Libraries like pandas, dash, and plotly simplify the creation of visualizations and backend logic.
3. Other Tools
•	Jupyter Notebook: 
o	Used for developing and testing the dashboard in an interactive environment.
•	Dash Leaflet: 
o	Maps geolocation data dynamically based on user selection.
•	Base64: 
o	Encodes and displays the Grazioso Salvare logo within the dashboard.
________________________________________
Project Steps
Step 1: Setting Up the Environment
•	Install required libraries: 
•	pip install dash jupyter-dash dash-leaflet pandas plotly pymongo
•	Import the dataset (aac_shelter_outcomes.csv) into a MongoDB database.
Step 2: Developing the CRUD Module
•	Created the AnimalShelter Python class for connecting to MongoDB and performing CRUD operations.
Step 3: Building the Dashboard
•	Designed the layout using Dash components: 
o	Header section with title and logo.
o	Filters for rescue types.
o	Data table for displaying the data dynamically.
o	Pie chart and geolocation map for visualization.
Step 4: Adding Interactivity
•	Implemented callbacks to: 
o	Update the data table based on filters.
o	Dynamically generate the pie chart based on filtered data.
o	Display geolocation data on the map for the selected row.
Step 5: Testing
•	Verified the application using test data and ensured functionality for all filters and interactive elements.
Step 6: Deployment
•	Run the dashboard locally in Jupyter Notebook and captured screenshots to demonstrate functionality.
________________________________________
Challenges and Solutions
Challenge 1: Missing Latitude/Longitude Data
•	Solution: 
o	Ensured the dataset included location_lat and location_long columns.
o	Defaulted to Austin, TX coordinates for rows missing geolocation data.
Challenge 2: Port Conflict
•	Solution: 
o	Changed the port number in the app.run_server() method.
o	Restarted the kernel to stop any existing Dash instances.
Challenge 3: Dynamic Filtering Issues
•	Solution: 
o	Implemented debugging with print() statements to verify filter conditions.
o	Corrected filter logic to align with MongoDB query syntax.
________________________________________
Resources
•	Dash Framework Documentation: https://dash.plotly.com/
•	MongoDB Documentation: https://www.mongodb.com/docs/
•	Dash Leaflet Documentation: https://dash-leaflet.herokuapp.com/
•	Python Pandas Documentation: https://pandas.pydata.org/
•	Grazioso Salvare Logo: Provided in project files.
________________________________________
Reproducing the Project
Prerequisites:
1.	Install MongoDB and import the dataset (aac_shelter_outcomes.csv).
2.	Install required Python libraries: 
3.	pip install dash jupyter-dash dash-leaflet pandas plotly pymongo
4.	Place the Grazioso Salvare logo (Grazioso Salvare Logo.png) in the project directory.
Steps to Run:
1.	Open the ProjectTwoDashboard.ipynb file in Jupyter Notebook.
2.	Run all cells to start the dashboard.
3.	Open the provided URL to interact with the application.
