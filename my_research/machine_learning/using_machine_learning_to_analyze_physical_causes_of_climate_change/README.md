# Using Machine Learning to Analyze Physical Causes of Climate Change: A Case Study of U.S. Midwest Extreme Precipitation
> This is a research letter.

Frances V. Davenpor and Noah S. Diffenbaugh

[Paper PDF](https://agupubs.onlinelibrary.wiley.com/doi/pdf/10.1029/2021GL093787)


# Motivation
- Identify large-scale atomospheric circulation patterns associated with extreme precipitation using CNN.

# Method
- Using dataset of PRISM Climate Group to calculate extreme precipitation days in a rectangle are in US. They denoted extreme rainfalls day as more than 95th percentile threthold of daily precipitation. Extreme precipitation day is called as EPCP (non-EPCP, vice varsa).

- Trained CNN to predict two classes of EPCP and non-EPCP. Input variable is daily Sea level pressure and 500-hPa GPH anomiles.

# Insight
- The CNN correctly classifies 91% of Midwest precipitation days as EPCPs, with an overall accuracy of 88% across both classes.

- From the LRP results of trained CNN, the rigional SLP and 500-hPa pixel relevance shows interensting relation. In EPCP days, the resutls were very localized compare with non-EPCP days.

# Contribution Summary
- Classification of precipitation using machiene learning method will work and LRP helps to understand the curculation pattern of SLP and 500-hPa fields associated extreme rainfalls.

# Keyword
- Layer-Wise Relevence Propagation (LRP)

# Unknown
- Some EPCP missed by the argorothms.

# Reflection
- Understaingin phisical process of the precipitations using ML(Ebert-Uphoff & Hilburn, 2020; Gagne et al., 2019;McGovern et al., 2019; Toms et al., 2020).

# Reference
- [Ham, Y. G., Kim, J. H., & Luo, J. J. (2019). Deep learning for multi-year ENSO forecasts. Nature, 573(7775), 568–572.](https://doi.org/10.1038/s41586-019-1559-7)

- About Layer-Wise Relevance Propagation. [Hilburn, K. A., Ebert-Uphoff, I., & Miller, S. D. (2021). Development and interpretation of a neural-network-based synthetic radar reflectivity estimator using GOES-R satellite observations. Journal of Applied Meteorology and Climatology, 60(1), 3–21.](https://doi.org/10.1175/JAMC-D-20-0084.1)


---
