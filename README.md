# Azure DevOps Work Item Data Extraction

This project provides a Jupyter notebook for extracting, transforming, and exporting work item data from Azure DevOps using the REST API. The notebook fetches work item revisions, processes date fields, calculates work hours, and exports the results to a CSV file.

## Features

- Fetches all work item revisions from Azure DevOps for a specified project and date range.
- Handles API authentication using a Personal Access Token (PAT) stored in environment variables.
- Processes and normalizes date fields to Indian Standard Time (IST).
- Calculates daily work hours based on completed work.
- Aggregates and exports the processed data to `output_file.csv`.

## Setup

1. **Clone or Download the Repository**

2. **Install Required Packages**

   Run the following command in a notebook cell:
   ```python
   !pip install python-dotenv pandas numpy pytz requests
   ```

3. **Configure Environment Variables**

   Create a `.env` file in the project directory with the following content:
   ```
   ORGANIZATION=your_organization_name
   PROJECT=your_project_name
   AZURE_PAT=your_azure_devops_pat
   ```

## Usage

1. Open the notebook `main 3 1 2.ipynb` in VS Code or Jupyter.
2. Run all cells sequentially.
3. The processed data will be saved as `output_file.csv` in the project directory.
4. Refresh the Power BI Output

## Notes

- Ensure your Azure DevOps PAT has sufficient permissions to read work items.
- Adjust the `startDateTime` parameter in the API URL as needed for your reporting period.

## License

This project is for internal use. Please ensure compliance with your organization's data policies.
