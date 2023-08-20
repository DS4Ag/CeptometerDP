[![Wang lab logo](https://static.wixstatic.com/media/c544bf_0e3064b159ae42238c83dca23bc352e8~mv2.png/v1/crop/x_0,y_0,w_1918,h_2080/fill/w_91,h_100,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/lab_icon_3.png)](https://www.dianewanglab.com/)



[![r-project](https://img.shields.io/badge/R-v4.1.3-blue)](https://www.r-project.org/)
[![dplyr](https://img.shields.io/badge/dplyr-1.1.1-success)](https://dplyr.tidyverse.org/)
[![tidyr](https://img.shields.io/badge/tidyr-1.0.3-success)](https://tidyr.tidyverse.org/)
[![lubridate](https://img.shields.io/badge/lubridate-1.9.2-success)](https://lubridate.tidyverse.org/)

[![DOI](https://zenodo.org/badge/680899711.svg)](https://zenodo.org/badge/latestdoi/680899711)

### Ceptometer Data Processing
R script to process data collected using the The AccuPAR LP-80 Ceptometer (r).

### Instructions
##### Data collection
1. Data must have the **Annotation** value following this arrangement:
**ExperimentName_PlotNumber**

E.g. 

|Annotation| 
| ------ |
| RUE_2 |

    Where:
        RUE = Experiment name identifier 

        _ = Required separation symbol

        2 = Plot number 


2. In case of taking more than one measurement per plot, use the following format:
ExperimentName_PlotNumber-MeasurementNumber

E.g. 

|Annotation| 
| ------ |
| RUE_2-1 |

    Where 
    RUE = Experiment name identifier 
    _ = Required separation symbol
    2 = Plot number 
    - = Required separation symbol
    1 = Measurmen 1 of n in the same plot.

3. If you have wrong measurements, only delete the values for columns from **Segment 1 PAR** to **Segment 8 PAR** (do not write 0 or any other character). Leave the rest of the rest of the column's values.  

|Record Type| Date and Time|Annotation| Segment 1 PAR|  Segment 2 PAR|  Segment 3 PAR|  Segment 4 PAR|  Segment 5 PAR|  Segment 6 PAR|  Segment 7 PAR|  Segment 8 PAR|  External Sensor| PAR    Record ID|
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| ABV | 2/3/2023 14:08| |1800.6|    1816.1| 1819.5| 1816.3| 1800.6| 1782.5| |1761|  1757.6| 0|  70658|
|BLW|   2/3/2023 14:08  ||68.4| 73.5|   89.8|   91.2|   86.7|   89| 85.8|   80.1|   0|  70659|
|ABV|   2/3/2023 14:09| |1225.9 |1818.2 |925.2| 1489.8| 1798.7| 1782.8| |1563.9|    1383.9| 0|  70660|
|ABV|   2/3/2023 14:09| |1547.3|    592.7|  536.3|  74.1|   67.2|   104.9|  72.9|   129.2|  0|  70661|
|ABV|   2/3/2023 14:09  ||| |   ||||    ||  0|  70662|
|ABV|   2/3/2023 14:09| |35 |22.3|  8|  6.4 |8.3|   19.1|   41.6|   12.2|   0|  70663|
|SUM|   2/3/2023 14:10|RUE_2-1||||||||||                                        70664|



4. Save your data file in CSV format.

##### Running the R script
 1. Update the values of the following lines according to your files.
```sh
path <- 'C:/Users/Nayeli Quitche/Documents/Ceptometro R studio'
input_file_name <- 'Ceptometro BDP_prueba codigo r studio.csv'
output_file_name <- 'ceptometro_prueba1bdp.csv'
```
 2. Run the R script. 
 3. Your result file will be saved in a folder called **output**.


### Contact
Luis Vargas Rojas - [lvargasr@purdue.edu](lvargasr@purdue.edu)
Purdue University, Wang Lab [dianewanglab.com](https://www.dianewanglab.com/)
