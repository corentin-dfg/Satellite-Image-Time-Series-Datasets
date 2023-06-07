<!-- omit in toc -->
# Satellite Image Time Series Datasets
This page presents a list of satellite imagery datasets with a temporal dimension, mainly satellite image time series (SITS) and satellite videos, for various computer vision and deep learning tasks. It covers multi-temporal datasets with more than two acquisitions but not bi-temporal datasets.

<!-- omit in toc -->
## Table of Contents
- [Semantic and Instance Segmentation](#semantic-and-instance-segmentation)
  - [Pixel annotations for each image](#pixel-annotations-for-each-image)
  - [Pixel annotations for each time series](#pixel-annotations-for-each-time-series)
  - [Polygon annotations for each image](#polygon-annotations-for-each-image)
  - [Polygon annotations for each time series](#polygon-annotations-for-each-time-series)
  - [Image annotations](#image-annotations)
- [Forecasting](#forecasting)
- [Object tracking](#object-tracking)
- [Other tasks](#other-tasks)
- [Authors](#authors)

## Semantic and Instance Segmentation
Datasets are sorted by annotation granularity. We note that polygons annotations are reserved for crop-type identification tasks, while pixel annotations might be considered in more general tasks such as land cover mapping.

### Pixel annotations for each image

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition area |
| --- | --- | --- | --- | --- | --- | --- |
| [MultiEarth 2022](https://arxiv.org/abs/2204.07649) | 2022 | Sentinel-1 + Sentinel-2 + Landsat-5 + Landsat-8 | 10m + 10m + 30m + 30m | Daily + weekly acquisitions depending on the source & Monthly annotation | 2 | Amazon |
| [Dynamic World](https://www.nature.com/articles/s41597-022-01307-4) | 2022 | Sentinel-2 | 10m | Weekly acquisition and weekly automatic annotation without human verification | 9 | Global |
| [DynamicEarthNet](https://openaccess.thecvf.com/content/CVPR2022/html/Toker_DynamicEarthNet_Daily_Multi-Spectral_Satellite_Dataset_for_Semantic_Change_Segmentation_CVPR_2022_paper.html) | 2021 | PlanetFusion | 3m | Daily acquisition & Monthly annotation | 7 | Global |
| [SpaceNet 7](https://openaccess.thecvf.com/content/CVPR2021/html/Van_Etten_The_Multi-Temporal_Urban_Development_SpaceNet_Dataset_CVPR_2021_paper.html) | 2020 | PlanetScope | 4m | Monthly acquisition & annotation | 2 | Global |


### Pixel annotations for each time series

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition area |
| --- | --- | --- | --- | --- | --- | --- |
| [MultiSenGE](https://germain-forestier.info/publis/isprs2022.pdf) | 2022 | Sentinel-1 + Sentinel-2 | 5m + 10m | Daily + weekly acquisition | 14 | Eastern France |
| [PASTIS](https://openaccess.thecvf.com/content/ICCV2021/html/Garnot_Panoptic_Segmentation_of_Satellite_Image_Time_Series_With_Convolutional_Temporal_ICCV_2021_paper.html) | 2021 | Sentinel-2 | 10m | Weekly acquisition | 18 | France |
| [PASTIS-R](https://www.sciencedirect.com/science/article/pii/S0924271622000855) | 2021 | Sentinel-1 + Sentinel-2 | 5m + 10m | Daily + weekly acquisition | 18 | France |
| [UTRNet](https://ieeexplore.ieee.org/document/9771449) | 2021 | Landsat-8 | 30m | Irregular acquisition | 2 | China |
| [MTLCC](https://www.mdpi.com/2220-9964/7/4/129) | 2018 | Sentinel-2 | 10m | Weekly acquisition & Annual annotation for 2016 and 2017 | 17 | Munich, Germany |
| [TiSeLaC](https://sites.google.com/site/dinoienco/tiselac-time-series-land-cover-classification-challenge) | 2017 | Landsat-8 | 30m | Bi-monthly acquisition | 9 | Reunion Island |

### Polygon annotations for each image

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition area |
| --- | --- | --- | --- | --- | --- | --- |
| [Sen4AgriNet](https://ieeexplore.ieee.org/abstract/document/9749916) | 2022 | Sentinel-2 | 10m to 60m | Weekly acquisition & Annual annotation | 168 | Catalonia & France |
| [Campo Verde](https://ieeexplore.ieee.org/document/8263605) | 2018 | Landsat-8 + Sentinel-1 | 30m + 10m | Bi-monthly acquisition & annotation | 14 | Brazil |
| [LEM](https://isprs-archives.copernicus.org/articles/XLII-1/387/2018/isprs-archives-XLII-1-387-2018.pdf) | 2018 | Landsat-8 + Sentinel-1 + Sentinel-2 | 30m + 10m + 10m | Bi-monthly (L8+S1) + weekly (S2) acquisition & Monthly annotation | 14 | Brazil |

### Polygon annotations for each time series

| Dataset name     | Year | Image source                                      | Spatial resolution | Temporal resolution               | Number of classes | Acquisition area           |
|------------------|------|---------------------------------------------------|--------------------|-----------------------------------|-------------------|-----------------------------|
| [DENETHOR](https://openreview.net/pdf?id=uUa4jNMLjrL)          | 2021 | Cloud-free fusion of images from various satellites | 3m                 | Daily acquisition                 | 10                | Germany                     |
| [EuroCrops (demo)](https://mediatum.ub.tum.de/doc/1616066/3z6cpijmuxa8qnbmyn0kjum6y.Schneider21_EPE.pdf)  | 2021 | Sentinel-2                                        | /                  | Weekly acquisition                | 43                | Austria & Denmark & Slovenia |
| [TimeSen2Crop](https://ieeexplore.ieee.org/abstract/document/9408357)      | 2021 | Sentinel-2                                        | 10m                | Weekly acquisition                | 16                | Austria                     |
| [Canadian Cropland](https://openreview.net/pdf/3b9f82b0ce8f1e195c4c20df9637afd8ed9ea339.pdf) | 2021 | Sentinel-2                                        | 10m                | Monthly acquisition               | 10                | Canada                      |
| [ZueriCrop](https://www.sciencedirect.com/science/article/pii/S0034425721003230)         | 2021 | Sentinel-2                                        | 10m                | Weekly acquisition                | 48                | Zurich, Swiss               |
| [Crop type in Western Cap](https://mlhub.earth/data/ref_fusion_competition_south_africa) | 2021 | PlanetScope + Sentinel-1 + Sentinel-2 | 3m + 10m + 10m     | Bi-monthly (Planet+S1) + weekly (S2) acquisition | 5  | South Africa |
| [Spot the crop challenge](https://mlhub.earth/10.34911/rdnt.j0co8q)   | 2021 | Sentinel-1 + Sentinel-2                        | 5m + 10m           | Bi-monthly + weekly acquisition   | 10                | South Africa                |
| [BreizhCrops](https://isprs-archives.copernicus.org/articles/XLIII-B2-2020/1545/2020/isprs-archives-XLIII-B2-2020-1545-2020.pdf)       | 2020 | Sentinel-2                                        | 60m                | Weekly acquisition                | 9                 | Brittany, France            |
| [Crop type in Ghana](https://openaccess.thecvf.com/content_CVPRW_2019/html/cv4gc/Rustowicz_Semantic_Segmentation_of_Crop_Type_in_Africa_A_Novel_Dataset_CVPRW_2019_paper.html)         | 2020 | PlanetScope + Sentinel-1 + Sentinel-2 | 3m + 10m + 10m     | Bi-monthly (Planet+S1) + weekly (S2) acquisition | 4  | Ghana |
| [Crop type on South Soudan](https://openaccess.thecvf.com/content_CVPRW_2019/html/cv4gc/Rustowicz_Semantic_Segmentation_of_Crop_Type_in_Africa_A_Novel_Dataset_CVPRW_2019_paper.html)  | 2020 | PlanetScope + Sentinel-1 + Sentinel-2 | 3m + 10m + 10m     | Bi-monthly (Planet+S1) + weekly (S2) acquisition | 4  | South Soudan |
| [CV4A Kenya](https://arxiv.org/abs/2004.03023)        | 2020 | Sentinel-2                                        | 10m                | Bi-monthly acquisition            | 7                 | Kenya                       |
| [Pixel-Set dataset](https://openaccess.thecvf.com/content_CVPR_2020/html/Garnot_Satellite_Image_Time_Series_Classification_With_Pixel-Set_Encoders_and_Temporal_CVPR_2020_paper.html) | 2020 | Sentinel-2                                        | 10m                | Weekly acquisition                | 20                | France                      |

### Image annotations

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition area |
| --- | --- | --- | --- | --- | --- | --- |
| [RapidAI4EO Corpus](https://rapidai4eo.source.coop/) | 2023 | PlanetFusion + Sentinel-2 | 3m + 10m | 5-days + monthly acquisition | 44 (multi-label) | Europe |
| [SEN12-FLOOD](https://isprs-archives.copernicus.org/articles/XLIII-B2-2020/1343/2020/isprs-archives-XLIII-B2-2020-1343-2020.pdf) | 2020 | Sentinel-1 + Sentinel-2 | 10m + 10m | Bi-monthly + weekly acquisition | 2 | African, Iranian and Australian cities |

## Forecasting

| Dataset name | Year | Image source                   | Spatial resolution | Temporal resolution | Number of classes | Acquisition area           |
|--------------|------|--------------------------------|--------------------|---------------------|-------------------|----------------------------|
| [SEN2DWATER](https://arxiv.org/abs/2301.07452) | 2023 | Sentinel-2 | 10m | Every 2 months | / | Italy & Spain |
| [EarthNet2021](http://www.classic.grss-ieee.org/earthvision2021/papers/Requena-Mesa_EarthNet2021_A_Large-Scale_Dataset_and_Challenge_for_Earth_Surface_Forecasting_CVPRW_2021_paper.pdf) | 2021 | Sentinel-2 + mesodynamic models | 20m + 1,28km       | Weekly (S2) + daily | /                 | Europe                     |
| [CloudCast](https://ieeexplore.ieee.org/abstract/document/9366908)     | 2021 | Meteosat Second Generation     | 3km                | 15min               | 11                | Europe                     |

## Object tracking

| Dataset name | Year | Image source | Spatial resolution | Temporal resolution | Number of classes | Acquisition area |
| --- | --- | --- | --- | --- | --- | --- |
| [AIR-MOT](https://ieeexplore.ieee.org/document/9715124) | 2022 | Jilin-1 | 1m | 5 to 10 frame per second | 2 | Cities |
| [VISO](https://ieeexplore.ieee.org/abstract/document/9625976) | 2021 | Jilin-1 | 1m | 10 frame per second | 4 | Cities |
| [SatSOT](https://ieeexplore.ieee.org/document/9672083) | 2021 | Jilin-1 + SkySat + Carbonite-2 | 1m | 10 to 25 frame per second | 4 | Cities |

## Other tasks

| Dataset name | Year | Task | Image source | Spatial resolution | Temporal resolution | Acquisition area |
| --- | --- | --- | --- | --- | --- | --- |
| [WorldStrat](https://openreview.net/forum?id=DEigo9L8xZA) | 2022 | Super-resolution | Spot-6 + Spot-7 + Sentinel-2 | 1,5m + 1,5m + 10m | Weekly (S2) acquisition | Global |
| [SEN12MS-CR-TS](https://ieeexplore.ieee.org/abstract/document/9691348) | 2022 | Cloud removal | Sentinel-1 + Sentinel-2 | 10m + 10m | Bi-monthly (S1) + weekly (S2) acquisition | Global |
| [AI4Boundaries](https://essd.copernicus.org/preprints/essd-2022-298/essd-2022-298.pdf) | 2022 | Field boundary detection | Sentinel-2 + aerial ortho-photo | 10m + 1m | Monthly acquisition & Yearly annotation | Europe |
| [Seasonal Contrast](https://openaccess.thecvf.com/content/ICCV2021/html/Manas_Seasonal_Contrast_Unsupervised_Pre-Training_From_Uncurated_Remote_Sensing_Data_ICCV_2021_paper.html) | 2021 | Pre-training task | Sentinel-2 | 10m | Seasonally acquisition | Global |

## Authors
The authors thank the French spatial agency (CNES) and the Brittany region / BreTel SIG for their financial support.
- [Corentin Dufourg](https://www.linkedin.com/in/corentin-dufourg/)<sup>1</sup>
- [Dr. Charlotte Pelletier](https://sites.google.com/site/charpelletier)<sup>1</sup>
- Stéphane May<sup>2</sup>
- [Pr. Sébastien Lefèvre](http://people.irisa.fr/Sebastien.Lefevre/)<sup>1</sup>

<sup>1</sup>Université Bretagne Sud, IRISA, UMR CNRS 6074, Vannes, France  
<sup>2</sup>Centre National d’Études Spatiales (CNES), Toulouse, France
