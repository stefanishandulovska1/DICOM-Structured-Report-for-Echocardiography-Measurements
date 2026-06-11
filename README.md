# DICOM Structured Report for Echocardiography Measurements

A medical digitization project focused on generating a DICOM Structured Report (SR) for echocardiography measurements extracted from an Excel file. The application creates a standard-compliant measurement report containing 70-80 echo-related values and provides an interactive **Show the Image** link for each measurement, allowing direct navigation to the corresponding medical image.

## Overview

This project was developed as part of the **Digitization** course and addresses the digitization of DICOM tags through automated insertion of measurement codes. Its main goal is to transform structured measurement data from Excel into a DICOM SR document that can be viewed alongside the original image in compatible medical imaging software such as Weasis.

## Key Features

- Supports **70-80 echocardiography measurements**
- Handles values such as gradient, velocity, and volume
- Includes measurement units such as mmHg, m/s, cm, and ml
- Provides a **Show the Image** link under each measurement
- Opens the corresponding image when the link is clicked
- Automatically integrates **Study UID** and **Series UID** from the source DICOM image
- Uses **TID 1500** to produce a standard DICOM Measurement Report

## Technologies Used

- Python
- pydicom
- pandas
- openpyxl
- DICOM Structured Reporting
- Excel-based data processing

## Project Goal

The purpose of this project is to simplify the conversion of echocardiography measurements into a structured and standardized DICOM report. By linking each measurement to its related medical image, the system improves traceability, interpretability, and usability in clinical or academic workflows.

## Installation

Install the required dependencies with:

```bash
pip install pydicom pandas openpyxl
```

## Quick Start

1. Prepare the `measurements_nashi.xlsx` file containing 70-80 echocardiography measurements.
2. Place the source DICOM image file as `echo_output.dcm`.
3. Run the script:

```bash
python script.py
```

4. Open Weasis and import both the generated Structured Report and the related DICOM image.
5. Click **Show the Image** under a measurement to navigate to the corresponding image.

## Expected Input Files

| File | Description |
|------|-------------|
| `measurements_nashi.xlsx` | Excel file containing coded echocardiography measurements |
| `echo_output.dcm` | Source DICOM image used for Study/Series integration |
| `script.py` | Python script that generates the DICOM Structured Report |

## Use Case

This project is suitable for medical imaging digitization tasks where structured measurement data must be linked with diagnostic images. It demonstrates how DICOM SR can be used to create interactive and standardized reports for echocardiography analysis.
