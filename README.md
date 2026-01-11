# 🚚 Strategic Supply Chain Optimization
### *Geospatial Analysis & Distribution Hub Placement*

---

## 🎯 Executive Summary
This project addresses a critical logistics challenge: **Service Level Failures**. By analyzing **180,519 global shipment records**, I identified geographical clusters with high delivery risk and utilized a **Weighted Center of Gravity (CoG)** model to mathematically determine the optimal location for a new strategic distribution hub.



## 🛠 Technical Methodology
The model optimizes the network by minimizing the weighted distance between the warehouse and the customer centers.

### 1. Data Processing
* **Source:** DataCo Smart Supply Chain Dataset.
* **Filtering:** Isolated transactions flagged as `Late_delivery_risk` to focus on service failures.
* **Weighting:** Applied **Order Item Quantity** as the weight factor ($w_i$) to ensure the hub is pulled toward high-volume demand centers rather than just geographical averages.

### 2. The Optimization Formula
The model calculates the optimal Latitude ($\bar{y}$) and Longitude ($\bar{x}$) using the following math:

$$\bar{x} = \frac{\sum (Longitude_i \cdot Quantity_i)}{\sum Quantity_i}$$

$$\bar{y} = \frac{\sum (Latitude_i \cdot Quantity_i)}{\sum Quantity_i}$$



---

## 📈 Key Results
* **Dataset Volume:** 180,000+ Transactions.
* **Primary Bottleneck:** Identified significant concentration of late deliveries within the Western Hemisphere.
* **The Solution:** The model proposed a specific "Center of Mass" for a new hub that balances logistics load and improves **On-Time Delivery (OTD)** rates.

---

## 📂 Repository Structure
| Folder / File | Description |
| :--- | :--- |
| `models/` | Contains the Python Jupyter Notebook with optimization logic. |
| `data/` | Directory for the source CSV (See Instructions). |
| `.gitignore` | Configured to exclude large datasets and virtual environments. |
| `README.md` | Project documentation and business case. |

---

## 🚀 How to Replicate
1.  **Clone the Repo:** ```bash
    git clone [https://github.com/](https://github.com/)[Your-Username]/Inverto-Supply-Chain-Optimization.git
    ```
2.  **Add Data:** Download the CSV from [Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis) and place it in the `/data` folder.
3.  **Run Analysis:** Execute the `.ipynb` file in PyCharm or any Jupyter environment.

---
*Developed as a Strategic Case Study for Supply Chain Consultancy.*