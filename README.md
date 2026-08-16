# Employee Data Synchronization (SF to S/4HANA) using SAP Cloud Integration

## Project Overview

This project implements an employee data integration scenario using SAP BTP Integration Suite – Cloud Integration.

The integration flow retrieves employee data from SAP SuccessFactors, processes and transforms the data using message mapping, sends the transformed data to S/4HANA, and uploads the processed data to an SFTP server.

The project also includes exception handling with email notification for integration failures.

## Integration Flow

SuccessFactors
      ↓
Request Reply
      ↓
Message Mapping
      ↓
Request Reply
      ↓
S/4HANA
      ↓
XML to CSV Converter
      ↓
SFTP

Exception Handling:
Integration Error
      ↓
Exception Subprocess
      ↓
Content Modifier
      ↓
Mail Notification

## Technologies Used

- SAP BTP
- SAP Integration Suite – Cloud Integration
- SAP SuccessFactors
- SAP S/4HANA
- SFTP
- Message Mapping
- XML to CSV Converter
- Content Modifier
- Request Reply
- Mail Adapter
- Exception Subprocess

## Key Features

- Employee data retrieval from SuccessFactors
- Message transformation using Message Mapping
- Employee data processing in S/4HANA
- XML to CSV conversion
- SFTP file upload
- Exception handling
- Error email notification
- Successful processing email notification
- Integration monitoring and testing

## Testing

The integration was tested using both positive and negative scenarios.

### Successful Scenario

Employee data is retrieved from SuccessFactors, transformed and successfully processed in S/4HANA. The processed data is also uploaded to the configured SFTP server.

### Error Scenario

An invalid SFTP configuration was used to verify exception handling and failure notification.

### Duplicate Participant ID Scenario

A duplicate Participant ID was used to verify the handling of duplicate employee records.

## Documentation

Detailed project documentation is available in the `Documentation` folder.

- Technical Design & Test Documentation
- Agile Project Artifacts

## Project Evidence

Screenshots and monitoring evidence are available in the `Screenshots` folder.

## Author

**Krishnakant Pal**

PID: P2012786192
