The dataset we chose was the [resale flat prices dataset](https://data.gov.sg/dataset/resale-flat-prices). This dataset contains the historical transactions of resale [Housing Development Board (HDB)](https://www.hdb.gov.sg/cs/infoweb/homepage) flats from 1990 to present, detailing these columns:

| Column name    | Description |
|----------------|-------------|
| `month`        | Sale month of the resale flat |
| `town`         | HDB towns; list available [here](https://www.hdb.gov.sg/about-us/history/hdb-towns-your-home)|
| `flat_type`      | HDB flat types; list available [here](https://www.hdb.gov.sg/residential/buying-a-flat/finding-a-flat/types-of-flats)|
| `block`         | Block number of the resale flat |
| `street_name`    | Street name of HDB flat |
| `storey_range`   | Range of storeys for HDB flat |
| `floor_area_sqm` | Area of the flat (in square metres) |
| `flat_model`     | HDB flat model |
| `lease_commencement_date` | Lease commencement date (YYYY format) |
| `remaining_lease` | Remaining lease length (in years) |
| `resale_price` | Transacted price (in S$) |

That being said, some of the files do not have the "remaining lease period" column, for which we can impute using the assumption that HDB flats have a 99-year lease starting from the lease commencement date, which is provided in all the data files.

We believe that the dataset is reliable given that it is provided by the Housing and Development Board and available for public download via the first link above. Furthermore, we can be confident that the data is updated, as is indicated from its metadata given in the same link.