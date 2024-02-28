<!-- omit in toc -->
# Satellite Image Time Series Datasets
This page presents a list of satellite imagery datasets with a temporal dimension, mainly satellite image time series (SITS) and satellite videos, for various computer vision and deep learning tasks. It covers multi-temporal datasets with more than two acquisitions but not bi-temporal datasets. We focus mainly on annotated datasets.

<!-- omit in toc -->
## Table of Contents
- [Semantic and Instance Segmentation](#semantic-and-instance-segmentation)
  - [Pixel annotations for each image](#pixel-annotations-for-each-image)
  - [Pixel annotations for each time series](#pixel-annotations-for-each-time-series)
  - [Polygon annotations for each image](#polygon-annotations-for-each-image)
  - [Polygon annotations for each time series](#polygon-annotations-for-each-time-series)
  - [Image annotations](#image-annotations)
- [Regression](#regression)
- [Forecasting](#forecasting)
- [Object tracking](#object-tracking)
- [Other tasks](#other-tasks)
- [Citation](#citation)

## Semantic and Instance Segmentation
Datasets are sorted by annotation granularity. We note that polygons annotations are reserved for crop-type identification tasks, while pixel annotations might be considered in more general tasks such as land cover mapping.

### Pixel annotations for each image

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition |
| --- | --- | --- | --- | --- | --- | --- |
| [MultiEarth 2023](https://arxiv.org/abs/2306.04738) | 2023 | Sentinel-1 + Sentinel-2 + Landsat-5 + Landsat-8 | 10m + 10m + 30m + 30m | Weekly acquisitions depending on the source & Monthly annotation | 2 | Amazon (1984-2021) |
| [MultiEarth 2022](https://arxiv.org/abs/2204.07649) | 2022 | Sentinel-1 + Sentinel-2 + Landsat-5 + Landsat-8 | 10m + 10m + 30m + 30m | Weekly acquisitions depending on the source & Monthly annotation | 2 | Amazon (1984-2021) |
| [Dynamic World](https://www.nature.com/articles/s41597-022-01307-4) | 2022 | Sentinel-2 | 10m | Weekly acquisition and weekly automatic annotation without human verification | 9 | Global (2015-present) |
| [DynamicEarthNet](https://openaccess.thecvf.com/content/CVPR2022/html/Toker_DynamicEarthNet_Daily_Multi-Spectral_Satellite_Dataset_for_Semantic_Change_Segmentation_CVPR_2022_paper.html) | 2021 | PlanetFusion | 3m | Daily acquisition & Monthly annotation | 7 | Global (2018-2019) |
| [SpaceNet 7](https://openaccess.thecvf.com/content/CVPR2021/html/Van_Etten_The_Multi-Temporal_Urban_Development_SpaceNet_Dataset_CVPR_2021_paper.html) | 2020 | PlanetScope | 4m | Monthly acquisition & annotation | 2 | Global (2017-2020) |


### Pixel annotations for each time series

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition |
| --- | --- | --- | --- | --- | --- | --- |
| [BraDD-S1TS](https://isprs-annals.copernicus.org/articles/X-1-W1-2023/835/2023/) | 2023 | Sentinel-1 | 10m | Weekly acquisition | 2 | Brazil (2020-2021) |
| [FLAIR #2](https://arxiv.org/pdf/2305.14467.pdf) | 2023 | Sentinel-2 | 10m | Weekly acquisition | 13 | France (1-year aquisition) |
| [MultiSenGE](https://germain-forestier.info/publis/isprs2022.pdf) | 2022 | Sentinel-1 + Sentinel-2 | 5m + 10m | Daily + weekly acquisition | 14 | Eastern France (2019-2020) |
| [PASTIS](https://openaccess.thecvf.com/content/ICCV2021/html/Garnot_Panoptic_Segmentation_of_Satellite_Image_Time_Series_With_Convolutional_Temporal_ICCV_2021_paper.html) | 2021 | Sentinel-2 | 10m | Weekly acquisition | 18 | France (2018-2019) |
| [PASTIS-R](https://www.sciencedirect.com/science/article/pii/S0924271622000855) | 2021 | Sentinel-1 + Sentinel-2 | 5m + 10m | Daily + weekly acquisition | 18 | France (2019) |
| [AI4EO Enhanced Sentinel 2 Agriculture](https://platform.ai4eo.eu/enhanced-sentinel2-agriculture-permanent) | 2021 | Sentinel-2 | 10m | Weekly acquisition | 2 | Slovenia (2019) |
| [UTRNet](https://ieeexplore.ieee.org/document/9771449) | 2021 | Landsat-8 | 30m | Irregular acquisition | 2 | China (2013-2021) |
| [MTLCC](https://www.mdpi.com/2220-9964/7/4/129) | 2018 | Sentinel-2 | 10m | Weekly acquisition & Annual annotation for 2016 and 2017 | 17 | Munich, Germany (2016-2017) |
| [TiSeLaC](https://sites.google.com/site/dinoienco/tiselac-time-series-land-cover-classification-challenge) | 2017 | Landsat-8 | 30m | Bi-monthly acquisition | 9 | Reunion Island (2014) |

### Polygon annotations for each image

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition |
| --- | --- | --- | --- | --- | --- | --- |
| [Sen4AgriNet](https://ieeexplore.ieee.org/abstract/document/9749916) | 2022 | Sentinel-2 | 10m to 60m | Weekly acquisition & Annual annotation | 168 | Catalonia & France (2019-2020) |
| [Deep Crop Rotation](https://www.mdpi.com/2072-4292/13/22/4599) | 2021 | Sentinel-2 | 10m | Weekly acquisition & Annual annotation | 10 | France (2018-2020) |
| [Campo Verde](https://ieeexplore.ieee.org/document/8263605) | 2018 | Landsat-8 + Sentinel-1 | 30m + 10m | Bi-monthly acquisition & annotation | 14 | Brazil (2015-2016) |
| [LEM](https://isprs-archives.copernicus.org/articles/XLII-1/387/2018/isprs-archives-XLII-1-387-2018.pdf) | 2018 | Landsat-8 + Sentinel-1 + Sentinel-2 | 30m + 10m + 10m | Bi-monthly (L8+S1) + weekly (S2) acquisition & Monthly annotation | 14 | Brazil (2017-2018) |

### Polygon annotations for each time series

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition |
|---|---|---|---|---|---|---|
| [SICKLE](https://arxiv.org/pdf/2312.00069.pdf) | 2024 | Landsat-8 + Sentinel-1 + Sentinel-2 | 30m + 3m + 10m | Bi-monthly + 12d + weekly acquistion | 21 | India (2018-2021) |
| [AgriSen-COG](https://www.mdpi.com/2072-4292/15/12/2980) | 2023 | Sentinel-2 | 10m | Weekly acquisition | 103 | Austria, Belgium, Spain, Denmark, Netherlands (2019-2020) |
| [TimeMatch](https://www.sciencedirect.com/science/article/pii/S0924271622001216) | 2022 | Sentinel-2 | 10m | Weekly acquisition | 16 | Austria, Denmark, mid-west France, southern France (2017) |
| [DENETHOR](https://openreview.net/pdf?id=uUa4jNMLjrL) | 2021 | Cloud-free fusion of images from various satellites | 3m | Daily acquisition | 10 | Germany (2018-2019) |
| [EuroCrops](https://mediatum.ub.tum.de/doc/1616066/3z6cpijmuxa8qnbmyn0kjum6y.Schneider21_EPE.pdf) | 2021 | Sentinel-2 | / | Weekly acquisition | 43 | Europe (2015-2022) |
| [TimeSen2Crop](https://ieeexplore.ieee.org/abstract/document/9408357) | 2021 | Sentinel-2 | 10m | Weekly acquisition | 16 | Austria (2017-2018) |
| [Canadian Cropland](https://openreview.net/pdf/3b9f82b0ce8f1e195c4c20df9637afd8ed9ea339.pdf) | 2021 | Sentinel-2 | 10m | Monthly acquisition | 10 | Canada (2019) |
| [ZueriCrop](https://www.sciencedirect.com/science/article/pii/S0034425721003230) | 2021 | Sentinel-2 | 10m | Weekly acquisition | 48 | Zurich, Switzerland (2019) |
| [Crop type in Western Cap](https://mlhub.earth/data/ref_fusion_competition_south_africa) | 2021 | PlanetScope + Sentinel-1 + Sentinel-2 | 3m + 10m + 10m | Bi-monthly (Planet+S1) + weekly (S2) acquisition | 5 | South Africa (2017) |
| [Spot the crop challenge](https://mlhub.earth/10.34911/rdnt.j0co8q) | 2021 | Sentinel-1 + Sentinel-2 | 5m + 10m | Bi-monthly + weekly acquisition | 10 | South Africa (2016) |
| [BreizhCrops](https://isprs-archives.copernicus.org/articles/XLIII-B2-2020/1545/2020/isprs-archives-XLIII-B2-2020-1545-2020.pdf) | 2020 | Sentinel-2 | 60m | Weekly acquisition | 9 | Brittany, France (2017) |
| [Crop type in Ghana](https://openaccess.thecvf.com/content_CVPRW_2019/html/cv4gc/Rustowicz_Semantic_Segmentation_of_Crop_Type_in_Africa_A_Novel_Dataset_CVPRW_2019_paper.html) | 2020 | PlanetScope + Sentinel-1 + Sentinel-2 | 3m + 10m + 10m | Bi-monthly (Planet+S1) + weekly (S2) acquisition | 4 | Ghana (2017) |
| [Crop type on South Soudan](https://openaccess.thecvf.com/content_CVPRW_2019/html/cv4gc/Rustowicz_Semantic_Segmentation_of_Crop_Type_in_Africa_A_Novel_Dataset_CVPRW_2019_paper.html) | 2020 | PlanetScope + Sentinel-1 + Sentinel-2 | 3m + 10m + 10m | Bi-monthly (Planet+S1) + weekly (S2) acquisition | 4 | South Soudan (2017) |
| [CV4A Kenya](https://arxiv.org/abs/2004.03023) | 2020 | Sentinel-2 | 10m | Bi-monthly acquisition | 7 | Kenya (2019) |
| [Pixel-Set dataset](https://openaccess.thecvf.com/content_CVPR_2020/html/Garnot_Satellite_Image_Time_Series_Classification_With_Pixel-Set_Encoders_and_Temporal_CVPR_2020_paper.html) | 2020 | Sentinel-2 | 10m | Weekly acquisition | 20 | France (2017) |

### Image annotations

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition |
| --- | --- | --- | --- | --- | --- | --- |
| [RapidAI4EO Corpus](https://rapidai4eo.source.coop/) | 2023 | PlanetFusion + Sentinel-2 | 3m + 10m | 5-days + monthly acquisition | 44 (multi-label) | Europe (2018-2019) |
| [SEN12-FLOOD](https://isprs-archives.copernicus.org/articles/XLIII-B2-2020/1343/2020/isprs-archives-XLIII-B2-2020-1343-2020.pdf) | 2020 | Sentinel-1 + Sentinel-2 | 10m + 10m | Bi-monthly + weekly acquisition | 2 | African, Iranian and Australian cities (2018-2019) |

## Regression

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Acquisition |
| --- | --- | --- | --- | --- | --- |
| [CropNet](https://openreview.net/forum?id=lzpHNyhIbr) | 2024 | Sentinel-2 + WRF-HRRR | 9km + 9km | 14d + 1d & Annual annotation | USA (2017-2022) |
| [SICKLE](https://arxiv.org/pdf/2312.00069.pdf) | 2024 | Landsat-8 + Sentinel-1 + Sentinel-2 | 30m + 3m + 10m | Bi-monthly + 12d + weekly acquistion | India (2018-2021) |
| [BioMassters](https://nascetti-a.github.io/BioMasster/) | 2023 | Sentinel-1 + Sentinel-2 | 20m + 10m | Monthly acquisition & Annual annotation | Finland (2016-2021) |

## Forecasting

> [!NOTE]  
> Here we list a few forecasting datasets, particularly for weather forecasting, but this list is by no means exhaustive. More weather forecasting datasets are listed [here](https://mldata.pangeo.io/index.html).

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition |
|---|---|---|---|---|---|---|
| [Digital Typhoon](https://arxiv.org/abs/2311.02665) | 2023 | Himawari | 5km | 60min | / | Western North Pacific basin (1978-2022) |
| [SEN2DWATER](https://arxiv.org/abs/2301.07452) | 2023 | Sentinel-2 | 10m | Every 2 months | / | Italy & Spain (2020-2022) |
| [EarthNet2021](https://openaccess.thecvf.com/content/CVPR2021W/EarthVision/html/Requena-Mesa_EarthNet2021_A_Large-Scale_Dataset_and_Challenge_for_Earth_Surface_Forecasting_CVPRW_2021_paper.html) | 2021 | Sentinel-2 + mesodynamic models | 20m + 1,28km | Weekly (S2) + daily | / | Europe (2016-2020) |
| [CloudCast](https://ieeexplore.ieee.org/abstract/document/9366908) | 2021 | Meteosat Second Generation | 3km | 15min | 11 | Europe (2017-2018) |
| [MeteoNet](https://meteonet.umr-cnrm.fr/) | 2020 | Ground station observations, satellite images, rain radar observations, weather forecasting models and land-sea and relief masks | Variable | Variable | / | France (2016-2018) |
| [SEVIR](https://proceedings.neurips.cc/paper/2020/hash/fa78a16157fed00d7a80515818432169-Abstract.html) | 2020 | GOES-16 + NEXRAD | 2km + 1km | 5min | / | USA (2017-2019)

## Object tracking

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition |
| --- | --- | --- | --- | --- | --- | --- |
| [TMS](https://arxiv.org/abs/2402.00703) | 2024 | Jilin-1 + SkySat + Synthetic | 1m | 1 frame per second | 1 | Cities |
| [AIR-MOT](https://ieeexplore.ieee.org/document/9715124) | 2022 | Jilin-1 | 1m | 5 to 10 frame per second | 2 | Cities |
| [VISO](https://ieeexplore.ieee.org/abstract/document/9625976) | 2021 | Jilin-1 | 1m | 10 frame per second | 4 | Cities |
| [SatSOT](https://ieeexplore.ieee.org/document/9672083) | 2021 | Jilin-1 + SkySat + Carbonite-2 | 1m | 10 to 25 frame per second | 4 | Cities |

## Other tasks

| Dataset name | Year | Task | Image source | Spatial resolution | Temporal resolution | Acquisition |
| --- | --- | --- | --- | --- | --- | --- |
| [SSL4EO-S12](https://ieeexplore.ieee.org/document/10261879) | 2023 | Pre-training task | Sentinel-1 + Sentinel-2 | 5m + 10m | Seasonally acquisition | Global |
| [SAT-MTB](https://ieeexplore.ieee.org/abstract/document/10130311) | 2023 | Detection, segmentation and object tracking | Jilin-1 | 1m | 10 frame per second | Cities |
| [TimeMatch](https://www.sciencedirect.com/science/article/pii/S0924271622001216) | 2022 | Domain adaptation | Sentinel-2 | 10m | Weekly acquisition| Austria, Denmark, mid-west France, southern France (2017) |
| [WorldStrat](https://openreview.net/forum?id=DEigo9L8xZA) | 2022 | Super-resolution | Spot-6 + Spot-7 + Sentinel-2 | 1,5m + 1,5m + 10m | Weekly (S2) acquisition | Global |
| [Jilin-189](https://github.com/XY-boy/MSDTGP) | 2022 | Video super-resolution | Jilin-1 | 1m | 25 frame per second | Cities |
| [SEN12MS-CR-TS](https://ieeexplore.ieee.org/abstract/document/9691348) | 2022 | Cloud removal | Sentinel-1 + Sentinel-2 | 10m + 10m | Bi-monthly (S1) + weekly (S2) acquisition | Global (2018) |
| [NASA Harvest](https://zindi.africa/competitions/nasa-harvest-field-boundary-detection-challenge) | 2022 | Field Boundary Detection | PlanetScope | 3.7m | Monthly acquisition & Time-independant annotation | Rwanda (2021) |
| [AI4Boundaries](https://essd.copernicus.org/preprints/essd-2022-298/essd-2022-298.pdf) | 2022 | Field boundary detection | Sentinel-2 + aerial ortho-photo | 10m + 1m | Monthly acquisition & Yearly annotation | Europe (2019) |
| [Seasonal Contrast](https://openaccess.thecvf.com/content/ICCV2021/html/Manas_Seasonal_Contrast_Unsupervised_Pre-Training_From_Uncurated_Remote_Sensing_Data_ICCV_2021_paper.html) | 2021 | Pre-training task | Sentinel-2 | 10m | Seasonally acquisition | Global |
| [PROBA-V Super-Resolution](https://link.springer.com/article/10.1007/s42064-019-0059-8) | 2019 | Super-resolution | PROBA-V | 300m + 100m | Daily acquisition | Global |

## Citation
The authors thank the French spatial agency (CNES) and the Brittany region for their financial support.
- [Corentin Dufourg](https://www.linkedin.com/in/corentin-dufourg/)<sup>1</sup>
- [Dr. Charlotte Pelletier](https://sites.google.com/site/charpelletier)<sup>1</sup>
- Stéphane May<sup>2</sup>
- [Pr. Sébastien Lefèvre](http://people.irisa.fr/Sebastien.Lefevre/)<sup>1</sup>

<sup>1</sup>Université Bretagne Sud, IRISA, UMR CNRS 6074, Vannes, France  
<sup>2</sup>Centre National d’Études Spatiales (CNES), Toulouse, France

If you use this work, consider citing it as below.

```latex
@misc{dufourg2023sitsdatasets,
 author = {Dufourg, Corentin and Pelletier, Charlotte and May, Stéphane and Lefèvre, Sébastien},
 title = {Satellite Image Time Series Datasets},
 howpublished = {\url{https://github.com/corentin-dfg/Satellite-Image-Time-Series-Datasets}} 
}
```
