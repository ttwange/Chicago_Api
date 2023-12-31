# Chicago Crimes API Data Pipeline Documentation

This documentation provides an overview of the Chicago Crimes API data pipeline developed using Mage AI. This pipeline extracts data from the [Chicago Crimes API](https://data.cityofchicago.org/resource/xguy-4ndq.csv), processes it, and exports it to Google Cloud Storage. The pipeline is designed to automate the data retrieval and storage process, making it easier to work with the data for analysis or further processing.

## Pipeline Overview

This data pipeline consists of three main blocks:

1. **crimes_load**: This block is responsible for loading data from the Chicago Crimes API. It uses the `requests` library to fetch data in CSV format and then converts it into a Pandas DataFrame.

2. **crimes_transform**: The transformation block processes the loaded data. While the template code does not specify any transformations, you can customize this block to perform any necessary data cleaning or manipulation.

3. **crimes_export**: This block exports the transformed data to Google Cloud Storage. It uses the Mage AI Google Cloud Storage connector to upload the data to a specified bucket.
## Usage

To use this pipeline, follow these steps:

1. Configure your Mage AI environment and set up the required dependencies.

2. Update the pipeline configuration and specify your Google Cloud Storage settings in the `io_config.yaml` file.

3. Run the pipeline, and it will automatically load data from the Chicago Crimes API, perform transformations (if needed), and export the data to Google Cloud Storage.

## Block Descriptions
### crimes_load

- **Description**: This block loads data from the Chicago Crimes API and converts it into a Pandas DataFrame.
- **Input**: None
- **Output**: Pandas DataFrame containing the raw data from the API.

### crimes_transform

- **Description**: This block can be customized to perform data transformations or preprocessing steps.
- **Input**: Pandas DataFrame (output from crimes_load).
- **Output**: Pandas DataFrame with transformed data (optional).

### crimes_export

- **Description**: This block exports data to Google Cloud Storage.
- **Input**: Pandas DataFrame (output from crimes_transform).
- **Output**: None

## Configuration
Before running the pipeline, you need to configure your environment and update the `io_config.yaml` file with your Google Cloud Storage settings:

- `bucket_name`: Specify the name of your Google Cloud Storage bucket.
- `object_key`: Set the desired object key (file name) for the exported data.
- `format`: Choose the format for exported data (e.g., 'parquet').

## Running the Pipeline

1. Ensure you have set up your Mage AI environment and dependencies.

2. Update the `io_config.yaml` file with your Google Cloud Storage settings.

3. Execute the pipeline, and it will automatically load data from the Chicago Crimes API, perform transformations (if needed), and export the data to Google Cloud Storage.

## Contributing

If you'd like to contribute to this project or improve the pipeline, please follow the Mage AI contribution guidelines and feel free to submit pull requests.

## License

This project is licensed under the [MIT License](LICENSE).
