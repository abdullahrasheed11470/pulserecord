# API Documentation

## Authentication

### Login
```
POST /api/login/
```
Parameters:
- username (string)
- password (string)

### Register
```
POST /api/register/
```
Parameters:
- username (string)
- email (string)
- password (string)
- role (string: "doctor" or "patient")

## Patient Endpoints

### List Patients
```
GET /api/patients/
```

### Create Patient
```
POST /api/patients/
```
Required fields:
- first_name
- last_name
- date_of_birth
- gender
- contact_number

### Update Patient
```
PUT /api/patients/{id}/
```

### Delete Patient
```
DELETE /api/patients/{id}/
```

## Doctor Endpoints

### List Doctors
```
GET /api/doctors/
```

### Create Doctor
```
POST /api/doctors/
```
Required fields:
- first_name
- last_name
- specialization
- license_number

### Update Doctor
```
PUT /api/doctors/{id}/
```

### Delete Doctor
```
DELETE /api/doctors/{id}/
```

## Hospital Endpoints

### List Hospitals
```
GET /api/hospitals/
```

### Create Hospital
```
POST /api/hospitals/
```
Required fields:
- name
- address
- contact_number

### Update Hospital
```
PUT /api/hospitals/{id}/
```

### Delete Hospital
```
DELETE /api/hospitals/{id}/
```

## Appointment Endpoints

### List Appointments
```
GET /api/appointments/
```

### Create Appointment
```
POST /api/appointments/
```
Required fields:
- patient_id
- doctor_id
- appointment_date
- appointment_time

### Update Appointment
```
PUT /api/appointments/{id}/
```

### Delete Appointment
```
DELETE /api/appointments/{id}/
```

## Response Formats

### Success Response
```json
{
    "status": "success",
    "data": {
        // Response data
    }
}
```

### Error Response
```json
{
    "status": "error",
    "message": "Error description"
}
```

## Status Codes
- 200: Success
- 201: Created
- 400: Bad Request
- 401: Unauthorized
- 403: Forbidden
- 404: Not Found
- 500: Server Error
