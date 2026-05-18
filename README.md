# Geospatial Analysis on Public Healthcare Facilities in Myanmar (2020)

## 📖 Project Overview
This project provides a comprehensive spatial analysis of healthcare accessibility across Myanmar. By leveraging **Geographic Information Systems (GIS)** and 2016 Census population data, the study identifies critical infrastructure gaps, travel burdens, and 'healthcare deserts' to support evidence-based decision-making for public health resource allocation.

---

## Key Research Questions
* How are health facilities distributed across different States and Regions?
* What is the relationship between population density and hospital bed capacity?
* Which townships face the highest travel burden (person-km exposure) to reach care?
* What percentage of the population lives within a 5km reachable distance of a hospital?

---

## 📊 Datasets Used
* **Health Facility Data (2020):** Provided by the Myanmar Information Management Unit (MIMU). Includes locations, types (General, Township, Station), and bed capacities.
* **Population Data (2016):** Census baseline data at the township level (MIMU).
* **Geographic Boundaries:** WFS Administrative boundaries (ADM3) from the MIMU GeoNode.

---

## ⚙️ Methodology
1. **Nearest Neighbor Analysis:** Using `scipy.spatial.cKDTree` to calculate the Euclidean distance to the nearest facility.
2. **Buffer Analysis:** Creating 5km catchment areas around facilities to evaluate physical coverage.
3. **Composite Accessibility Index:** A weighted model combining:
   * Facility Density (35%)
   * Bed-to-Population Ratio (35%)
   * Buffer Coverage (30%)
4. **Risk Metrics:** Calculating *'Person-km Exposure'* to identify systemic vs. absolute travel burdens.

---

## 🚀 Installation & Usage

1. **Clone this repository:**
   ```bash
   git clone [https://github.com/sansanmaw/geospatial-analysis-myanmar-public-health-facility-anlaysis.git](https://github.com/sansnamaw/geospatial-analysis-myanmar-public-health-facility-anlaysis.git)
   cd geospatial-analysis-myanmar-public-health-facility-anlaysis
