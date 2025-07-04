# Supplier Optimization
## Overview
This project applies **clustering** and **linear programming** techniques to analyze supplier performance and optimize supply allocation.
- Identify distinct supplier groups through K-means clustering
- Explore relationships between supplier clusters and characteristics
- Develop a cost-minimization supply plan through linear programming<br>

**Part 1:** Cluster suppliers based on quality, cost, delivery time, and flexibility.<br>
**Part 2:** Use linear programming to minimize transportation and manufacturing costs while satisfying customer demand.<br>

## Part 1 – Supplier Clustering

### Goal
Group suppliers based on performance to uncover meaningful patterns.

### Cluster Interpretations
**cluster 1**: Suitable for situations requiring high quality and consistency, with less concern about cost or customization.<br>
**cluster 2**: Suitable for cost-sensitive needs with high delivery and customization flexibility, but less focus on quality.<br>
**cluster 3**: Good for standardized, high-volume production that values quality and cost over customization<br>
**cluster 4**: high-risk suppliers with inconsistent performance, but advantages in speed and adaptability.

## Part 2 – Linear Programming Optimization

### Goal
Minimize total cost while fulfilling customer demand across multiple nodes in a supply chain.

### Supply Chain Network
![Supply Chain Network](https://github.com/user-attachments/assets/65db39e1-d3f0-401e-af68-b648105c80d5)<br>
There are two suppliers (S1 and S2), two warehouses (D1 and D2) and three retailers (R1, R2 and R3).<br>
The demand at the retailers are 1500 units, 2000 units and 1000 units respectively for R1, R2, and R3.

### Transportation Cost Table
| From → To         | W1      | W2      | R1      | R2      | R3      |
|------------------|---------|---------|---------|---------|---------|
| **Supplier 1**   | 150     | 200     | 325     | 260     | 390     |
| **Supplier 2**   | 400     | 350     | 585     | 650     | 520     |
| **Warehouse 1**  |         |         | 65      | 65      | 65      |
| **Warehouse 2**  |         |         | 97.5    | 32.5    | 32.5    |

### Results
- **Minimum Total Cost**: \$9,967,500
- **Optimal Plan**: All shipments are fulfilled directly from Supplier S2 to the retailers.
- **Insight**: Warehouses were unused in the optimal plan, indicating that direct shipping was more cost-efficient.

