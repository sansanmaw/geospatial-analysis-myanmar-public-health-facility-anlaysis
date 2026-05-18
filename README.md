# geospatial-analysis-myanmar-public-health-facility-anlaysis

Geospatial Analysis on Public Healthcare Facilities in Myanmar (2020)
Project Overview
This project provides a comprehensive spatial analysis of healthcare accessibility across Myanmar. By leveraging Geographic Information Systems (GIS) and 2016 Census population data, the study identifies critical infrastructure gaps, travel burdens, and 'healthcare deserts' to support evidence-based decision-making for public health resource allocation.

Key Research Questions
How are health facilities distributed across different States and Regions?
What is the relationship between population density and hospital bed capacity?
Which townships face the highest travel burden (person-km exposure) to reach care?
What percentage of the population lives within a 5km reachable distance of a hospital?
Datasets Used
Health Facility Data (2020): Provided by the Myanmar Information Management Unit (MIMU). Includes locations, types (General, Township, Station), and bed capacities.
Population Data (2016): Census baseline data at the township level (MIMU).
Geographic Boundaries: WFS Administrative boundaries (ADM3) from the MIMU GeoNode.
Methodology
Nearest Neighbor Analysis: Using scipy.spatial.cKDTree to calculate the Euclidean distance to the nearest facility.
Buffer Analysis: Creating 5km catchment areas around facilities to evaluate physical coverage.
Composite Accessibility Index: A weighted model combining Facility Density (35%), Bed-to-Population Ratio (35%), and Buffer Coverage (30%).
Risk Metrics: Calculating 'Person-km Exposure' to identify systemic vs. absolute travel burdens.
Installation & Usage
Clone this repository.
Ensure the required datasets (.csv and .xlsx) are present in the directory.
Install dependencies:
pip install geopandas mapclassify scikit-learn scipy matplotlib seaborn folium
Run the Jupyter Notebook Myanmar_Healthcare_Analysis.ipynb.
Key Findings
National Coverage: Only 28% of the national area falls within a 5km buffer of a health facility.
Regional Gaps: Kayin and Shan (North/East) exhibit the lowest accessibility scores.
Travel Burden: Identified townships where the average distance to a hospital exceeds 60km.
Author
San San Maw
Course: Geospatial Analysis

