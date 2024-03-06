# Hospital API for COVID-19 Testing and Quarantine Management

This API is designed to facilitate the testing, quarantine, and well-being management of COVID-19 patients by doctors in a hospital setting. The API supports two types of users: doctors and patients.

## User Types

### 1. Doctors
- Doctors can log in using their credentials.
- They can register patients upon their visit to the hospital.
- After the checkup, doctors can create a report for each patient.

### 2. Patients
- Patients can be registered by doctors upon their visit to the hospital.

## API Endpoints

### Authentication
- `/doctors/register` - Register a doctor with username and password.
- `/doctors/login` - Log in for doctors and receive a JWT (JSON Web Token) to be used for authentication.

### Patients
- `/patients/register` - Register a new patient.
- `/patients/:id/all_reports` - Retrieve all reports of a patient, sorted from oldest to latest.

### Reports
- `/patients/:id/create_report` - Create a report for a patient.
- `/reports/:status` - List all reports of all patients filtered by a specific status.

## Report Fields

Each patient report includes the following fields:
- Created by doctor
- Status (Enums: Negative, Travelled-Quarantine, Symptoms-Quarantine, Positive-Admit)
- Date
- Required Routes

## Authentication and Authorization

- Routes for doctors' registration and login are protected by authentication.
- All routes related to patients' information and reports are accessible only after successful authentication.

## Security

- JWT is utilized for authentication to ensure secure access to the API.
- Proper error handling and validation mechanisms are implemented to prevent unauthorized access and ensure data integrity.

## Note

- Further improvements and optimizations can be made based on specific hospital requirements and security considerations.

---
This README provides an overview of the Hospital API for COVID-19 Testing and Quarantine Management. For detailed information on API endpoints, request and response formats, refer to the API documentation. For any queries or assistance, contact the development team.
