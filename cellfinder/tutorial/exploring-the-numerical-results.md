---
description: Understanding the numerical summaries of cellfinder results
---

# Exploring the numerical results

In the `test_brain/output/analysis` directory is a `summary.csv` file which you can open in Microsoft Excel \(or similar\) to view a summary of the results. This file lists, for each brain area, the number of cells detected, the volume of the brain area, and the density of cells \(in cells per mm^3\). This is the file you'll most likely use for statistical analysis. It will look something like this \(but with an entry for each brain area\):	

| structure\_name | left\_cell\_count | right\_cell\_count | total\_cells | left\_volume\_mm3 | right\_volume\_mm3 | total\_volume\_mm3 | left\_cells\_per\_mm3 | right\_cells\_per\_mm3 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Retrosplenial area, ventral part, layer 5 | 1717 | 780 | 2497 | 0.935890625 | 0.907375 | 1.843265625 | 1834.61609095614 | 859.622537539606 |
| Lateral dorsal nucleus of thalamus | 1189 | 0 | 1189 | 0.52415625 | 0.498734375 | 1.022890625 | 2268.40755976868 | 0 |
| Retrosplenial area, dorsal part, layer 5 | 645 | 125 | 770 | 0.659375 | 0.66290625 | 1.32228125 | 978.199052132701 | 188.563616650167 |
| Retrosplenial area, ventral part, layer 2/3 | 147 | 588 | 735 | 0.563359375 | 0.548703125 | 1.1120625 | 260.934683123006 | 1071.61773500014 |
| Retrosplenial area, dorsal part, layer 2/3 | 256 | 301 | 557 | 0.52496875 | 0.532625 | 1.05759375 | 487.648074290136 | 565.125557380897 |

