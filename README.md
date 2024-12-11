Overview:
This Power BI dashboard provides insights into maritime operations by analyzing data on vessels, crew members, ports, and shipments. The data model is designed with a Star Schema to ensure optimal performance and usability, facilitating detailed analysis across various dimensions.

Data Sources:
Vessels: Details about ships, including specifications such as capacity (TEU), draught, and age.
Crew: Information about sailors, including their position, years of experience, and names.
Ports: Geographic and operational data for origin and destination ports.
Shipments: Historical records of vessel movements, including shipment weight, dates, and port details.

Data Model:
Fact Table:
Shipments:
Contains transactional data for vessel movements (e.g., origin port, destination port, shipment weight).
Dimension Tables:
Vessels: Contains static attributes of ships, such as capacity, draught, and build year.
Crew: Captures sailor-specific details like position and experience level.
Ports: Holds geographic details for mapping and analysis.
Intermediate Table:
Includes calculated columns such as Gregorian dates derived from Shamsi dates.

Key Calculations and Measures
Vessel Age:
A calculated column that determines the age of each vessel using its build year and the current year.
Traffic Volume:
Aggregates the total volume of shipments between ports.
Crew Grouping:
Categorizes crew members based on their years of experience (e.g., Junior: 0-5 years, Mid-level: 6-15 years, Senior: 16+ years).

Data Cleaning and Transformation:
All data transformations, including imputations and date conversions, are handled in the Staging Area of Power BI.
The intermediate tables (e.g., for date conversions) are disabled for report view but remain active for relationships.

Usage Instructions:
Filters and Slicers:
Use slicers to filter data by year, port, vessel type, or crew category.
Interactive Maps:
Hover over ports or traffic lines for detailed information.
Exporting Reports:
Use the built-in export feature to save visuals as PDFs or images.

Future Enhancements:
Integration with live data sources for real-time updates.
Advanced analytics such as predictive modeling for traffic patterns.
Enhanced crew analysis by adding training and certification data.

Notes:
Ensure all intermediate tables are disabled in the data model view to improve performance.
Review the data source updates regularly to maintain accuracy.
If you encounter issues or need further customization, please contact the dashboard developer.
