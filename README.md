# Ocean Current Prediction using Gaussian Processes

## Project Overview
This project aims to model and predict ocean currents within the Philippine Archipelago using Gaussian Processes (GPs). The dataset used in this study was provided by the MSEAS research group at MIT and includes both horizontal and vertical components of ocean flow vectors. The project involves detailed analysis and prediction of ocean currents, leveraging advanced machine learning techniques.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Methodology](#methodology)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Data Description
The dataset comprises ocean flow vectors collected in January 2009 by the MSEAS research group at MIT. The data includes both horizontal and vertical components of the flow, offering a detailed view of the ocean dynamics within the Philippine Archipelago. 

### Characteristics of the Data
- **Flow Vectors:** Provided in kilometers per hour (km/h), representing the speed and direction of ocean currents.
- **Temporal Resolution:** Data recorded every 3 hours, starting from 0 hours.
- **Spatial Resolution:** Grid spacing is 3 km.
- **Vertical Coverage:** From the surface to either near the bottom or 400m of depth, whichever is shallower.

### Organization of the Data Files
- **File Naming:** Each `.csv` file is named to indicate the time step it represents (e.g., `24u.csv`, `24v.csv`).
- **Components:** Files with suffix `u` contain horizontal components, while files with suffix `v` contain vertical components.
- **Grid Layout:** Columns correspond to the horizontal direction (x-axis), and rows correspond to the vertical direction (y-axis).

### Additional Information
- **Units and Measurements:** Flow data in km/h. The first time index corresponds to 0 hours.
- **Land and Water Mask:** A mask file (`mask.csv`) is provided but generally not required.
- **Grid Indexing:** The matrix index (0, 0) corresponds to the coordinate (0km, 0km).

## Methodology
To model and predict the ocean currents, Gaussian Processes (GPs) are employed. GPs are non-parametric models that define a distribution over functions and can provide uncertainty estimates along with predictions. The methodology involves:
1. **Kernel Selection and Model Training:**
   - Select candidate kernels.
   - Perform k-fold cross-validation to estimate the generalization error.
   - Maximize the log marginal likelihood to optimize kernel parameters.
2. **Long-Range Spatial Correlations:**
   - Analyze long-range correlations using graphical network models.
   - Use mutual information to capture non-linear relationships.

## Results
The project demonstrates the application of GPs in predicting ocean currents with high accuracy. Detailed results and visualizations are provided in the project notebook.

## Contributing
Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) before submitting a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

