# IGS GNSS Data Download

This Python module provides utilities for working with GNSS data. It includes functionality to calculate GPS week and download IGS station observation and navigation files from the ESA FTP server.

## Features

- **GPS Week Calculation**: Convert a given day of year and year to its corresponding GPS week.
- **IGS Station Data Downloader**: Download observation and navigation files for a specific GNSS station over a specified date range.

## Installation

This module does not require any external dependencies beyond Python's standard library. Simply clone this repository and use the provided Python file.

```bash
# Clone the repository
$ git clone https://github.com/](https://github.com/anwar1406/IGS-Data-Download.git

# Navigate into the directory
$ cd gnss-data-downloader
```

## Usage

### Import the Module

You can import the module into your Python script:

```python
from gnss_data_downloader import gps_week, igs_station_data
```

### Functions

#### `gps_week(day_of_year, year)`
Converts a given day of year and year to its corresponding GPS week.

- **Parameters**:
  - `day_of_year` (int): Day of the year (1-365 or 1-366 for leap years).
  - `year` (int): The year (e.g., 2023).
- **Returns**:
  - `int`: The GPS week number.

#### Example
```python
week = gps_week(152, 2023)
print(f"GPS Week: {week}")
```

#### `igs_station_data(station_name, doy_i, doy_f, year, country_name="IND", file_path="")`
Downloads IGS station data (observation and navigation files) for a specified station and date range.

- **Parameters**:
  - `station_name` (str): Name of the GNSS station (e.g., "IISC").
  - `doy_i` (int): Start day of the year (DOY).
  - `doy_f` (int): End day of the year (DOY).
  - `year` (int): Year of the data.
  - `country_name` (str, optional): Country code (default: "IND").
  - `file_path` (str, optional): Directory to save the downloaded files (default: current directory).

#### Example
```python
igs_station_data(
    station_name="IISC",
    doy_i=152,
    doy_f=156,
    year=2023,
    country_name="IND",
    file_path="./data"
)
```

### Running the Module

To run the module as a standalone script:

1. Modify the parameters in the `if __name__ == "__main__"` section.
2. Execute the script:

```bash
$ python gnss_data_downloader.py
```

## Directory Structure

```
.
├── gnss_data_downloader.py  # Main Python module
├── README.md                # Documentation
└── data/                    # Directory for downloaded files (created dynamically)
```

## Contributions

Contributions are welcome! If you encounter a bug or have a feature request, please open an issue or submit a pull request.

## License

This project is licensed under CC0 licence. See the LICENSE file for details.

## Acknowledgments

This module was developed by **Ibaad Anwar** as part of Ph.D.= Thesis on GNSS.

