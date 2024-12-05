# Exploring the use of dust-MS correlation to create age models for Scotia Sea sediment cores
#### Gabriel Mangum Lehmann 
#### Fall 2024

## Motivation 
Sediments deposited in the Scotia Sea, the so-called ‘Iceberg Alley’ in the Atlantic sector of the Southern Ocean (SO), are transported via icebergs, bottom currents, wind, and settling of biogenic particles from the surface ocean (Anderson and Andrews 1999). Studying the spatial distribution and stratigraphic variability of sediments in the Scotia Sea through these co-registered ocean, atmosphere, ecologic, and ice sheet signals provides us with greater insight into Antarctic Ice Sheet, SO, and carbon cycle evolution in modern, glacial, and past warm times. However, the general lack of carbonate microfossils south of the Polar Front inhibits the development of age models for Scotia Sea sediment cores through the backbone of Quaternary orbital resolution marine--benthic ∂18O correlation. Due to the absence of carbonate microfossils, age models must be developed through other methods. Existing chronologies for the Scotia Sea typically rely on magnetic susceptibility (MS), which exhibits marked glacial-interglacial changes, with glacial periods associated with a higher MS; the MS variability displays a remarkably similar pattern to the dust and non-sea salt Ca2+ record in Antarctic ice cores (Weber et al. 2012, Weber et al. 2022, Xiao et al. 2016). However, the ice core record only extends to 800 ka, so MS cannot be correlated to nssCa2+ from ice cores past that time. In this project, I explore the relationship between dust deposition and the Scotia Sea MS signal through time, and I investigate the use of sediment Fe accumulation rate as an alternative to the ice core nssCa2+ record.

## Research Questions
Can ODP Site 1090 Fe accumulation rate be used as an alternative age reference to Antarctic ice core dust records for the creation of sediment core age models that rely on Scotia Sea MS data? 
Does the close relationship between Scotia Sea MS and dust deposition hold for times older than 800 ka, and how does the relationship change over time?

## Datasets 
I will use MS data from IODP Site U1537, which is available in the folder; this data was collected and provided to me by my advisor, Brendan Reilly. MS data from U1537 shows a strong correlation (r=0.85) to the nssCa2+ record from the EDML ice core (Weber et al. 2022).
Fe accumulation rate data from ODP Site 1090 (Martinez-Garcia et al. 2014, available in the folder as well as on the [NOAA Paleo Data Search database](https://doi.pangaea.de/10.1594/PANGAEA.767458). This data has been used to reconstruct dust supply to the Southern Ocean over the past four million years (Martinez-Garcia et al. 2011).

## Analysis 
I first identify tie points between Site U1537 MS and Site 1090 Fe accumulation rate and linearly interpolate between those tiepoints in [Qanalyseries](https://paloz.marum.de/confluence/display/ESPUBLIC/QAnalySeries-Public), a free software for analyzing time series. I then combine the two datasets such that they are in the same dataframe and on the same age scale. Finally, I determine the correlation for the whole record, before and after 800 ka, and over a 1000-data point rolling window (with 15661 data points in the time series). A strong correlation through the whole record would allow for the use of Site 1090 as a reference for the stratigraphic correlation of Scotia Sea MS and thus the development of age models for sediment cores that can illuminate important ocean, atmospheric, and glacial processes for past climate change. If there is a weak relationship between Fe flux at ODP Site 1090 and MS at IODP Site U1537 for the whole record, it would indicate that the process controlling Scotia Sea MS is driven by processes other than dust deposition; if there is a close relationship that breaks down prior to 800 ka, it would indicate changes to climatic processes of the Southern Ocean prior to 800 ka. 

### References
Anderson, John B., and John T. Andrews. "Radiocarbon constraints on ice sheet advance and retreat in the Weddell Sea, Antarctica." *Geology* 27.2 (1999): 179-182.

Kotov S., Pälike H. (2018). QAnalySeries – a cross-platform time series tuning and analysis tool. AGU.

Martinez-Garcia, A., D.M. Sigman, H. Ren, R.F. Anderson, M. Straub, D.A. Hodell, S.L. Jaccard, T.I. Eglinton, and G.H. Haug. 2014. Iron Fertilization of the Subantarctic Ocean During the Last Ice Age. *Science*, 343(6177), 1347-1350. doi: 10.1126/science.1246848

Martínez-Garcia, A., Rosell-Melé, A., Jaccard, S. L., Geibert, W., Sigman, D. M., & Haug, G. H. (2011). Southern Ocean dust–climate coupling over the past four million years. *Nature*, 476(7360), 312-315.

Weber, M. E., Bailey, I., Hemming, S. R., Martos, Y. M., Reilly, B. T., Ronge, T. A., ... & Zheng, X. (2022). Antiphased dust deposition and productivity in the Antarctic Zone over 1.5 million years. *Nature Communications*, 13(1), 2044.

Weber, M. E., Kuhn, G., Sprenk, D., Rolf, C., Ohlwein, C., & Ricken, W. (2012). Dust transport from Patagonia to Antarctica–a new stratigraphic approach from the Scotia Sea and its implications for the last glacial cycle. *Quaternary Science Reviews*, 36, 177-188.

Xiao, W., Frederichs, T., Gersonde, R., Kuhn, G., Esper, O., & Zhang, X. (2016). Constraining the dating of late Quaternary marine sediment records from the Scotia Sea (Southern Ocean). *Quaternary Geochronology*, 31, 97-118.

