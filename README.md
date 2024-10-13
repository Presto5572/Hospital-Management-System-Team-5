# Hospital-Management-System-Team-5

## Team Members
- Cole Keim
- Justin Cushing
- James Rogers
- Camden Myers
- Wil Cunningham

## Problem Description
The task at hand is to model and build a relational database for the general workings of a hospital. The central entity in the model is the Patient entity—representing each individual receiving care in the hospital. The hospital operates with various departments, wards, and staff, including Nurses and Doctors, who provide care through Appointments and Treatments.

The hospital also manages financial aspects, such as patient Billing and Insurance. All of these components work together to support the care provided to patients. We are interested in accurately modeling these relationships, generating sample data, and populating the entities with this data. Furthermore, we aim to perform functioning queries on this data to provide valuable business insights about the hospital and its operations.


## Data Model
Our hospital management system is structured to streamline hospital operations and ensure the efficient delivery of patient care. The model focuses on managing staff, patient records, departments, appointments, and billing.

The Nurse entity represents all nurses in the hospital. Nurses can work under a Head Nurse, which is why we established a recursive one-to-many relationship within the Nurse table, where each nurse may have a supervising head nurse. In addition, we created an associative entity called NurseWardAssignment, representing the assignment of nurses to various wards. This entity captures the many-to-many relationship between Nurses and Wards, as each nurse can be assigned to multiple wards, and each ward can have several nurses working in it.

The Ward entity represents different wards or sections within the hospital, such as ICU, Pediatrics, or General Surgery. Each ward has a Head Nurse who oversees the operations, and this is reflected in the one-to-one relationship between Ward and Nurse for the head nurse role.

Patients are a core focus of the system. The Patient entity stores the basic information of individuals receiving care, including emergency contact details. Each patient is assigned to a Ward, establishing a one-to-many relationship between Ward and Patient because multiple patients can occupy a ward at any given time. Patients also have many Appointments with doctors, represented by a one-to-many relationship between the Patient and Appointment entities. Each appointment record stores information about the doctor, date, and time of the consultation.

Doctors play a central role in patient care. The Doctor entity includes basic information about the doctors in the hospital. Each doctor may work under a Senior Doctor, creating a recursive one-to-many relationship within the Doctor table. Additionally, each doctor is assigned to a Department, such as cardiology, surgery, or pediatrics, creating a one-to-many relationship between Department and Doctor. This captures the structure of the medical staff in the hospital.

Doctors also have appointments with multiple patients, represented by the one-to-many relationship between Doctor and Appointment. During these appointments, doctors may prescribe treatments or medications, which are stored in the Prescription entity. A one-to-many relationship exists between Doctor and Prescription as a doctor can issue many prescriptions, and similarly between Patient and Prescription, as a patient can receive multiple prescriptions over time. Each prescription includes the medication name, dosage, and specific instructions for use.

The hospital’s Medical Record entity captures the complete history of each patient’s visits and treatments. Since patients can have multiple records for different visits, we established a one-to-many relationship between Patient and Medical_Record. Each medical record includes information on the diagnosis, treatment provided, and the date of the visit.

In addition to medical care, the hospital management system also tracks financial data through the Billing entity. Each Billing record is linked to a Patient and an Insurance provider. The Billing table records the total amount, the amount covered by insurance, and payment details, ensuring a complete record of the patient’s financial obligations. There is a one-to-one relationship between Billing and Insurance, as each billing record is associated with a specific insurance policy.

Finally, the Insurance entity captures details about the insurance providers, policies, and coverage periods. This entityhelps the hospital manage insurance-related claims and coverage for patients’ medical expenses.

<img width="493" alt="Screenshot 2024-10-12 at 11 03 46 AM" src="https://github.com/user-attachments/assets/590a15e7-c5e6-4211-97a5-412c754ca544">


## Data Dictionary

<img width="732" alt="Screenshot 2024-10-12 at 9 26 47 PM" src="https://github.com/user-attachments/assets/6187db65-15dd-4ca1-9fb3-285c3d3dfb4c">

<img width="639" alt="Screenshot 2024-10-12 at 9 27 25 PM" src="https://github.com/user-attachments/assets/3cce9f94-4465-4f60-a18c-959e16906a00">

<img width="651" alt="Screenshot 2024-10-12 at 9 27 50 PM" src="https://github.com/user-attachments/assets/35935330-dda5-428b-bcc3-7c70b6f06e04">

<img width="659" alt="Screenshot 2024-10-12 at 9 28 15 PM" src="https://github.com/user-attachments/assets/1a5d3680-6c2f-4815-bdce-becc2e5d31d9">

<img width="742" alt="Screenshot 2024-10-12 at 9 28 32 PM" src="https://github.com/user-attachments/assets/b0e06843-9612-4c19-b714-28dea9644cf9">

<img width="524" alt="Screenshot 2024-10-12 at 9 28 53 PM" src="https://github.com/user-attachments/assets/8cb843e5-2db3-43fb-8a80-7135175792ca">

<img width="629" alt="Screenshot 2024-10-12 at 9 29 24 PM" src="https://github.com/user-attachments/assets/db02a6a7-d573-45f1-bda5-d7ab64fe9e05">

<img width="478" alt="Screenshot 2024-10-12 at 9 29 41 PM" src="https://github.com/user-attachments/assets/b09c55ca-5840-4c60-9495-6b376d372ca9">

<img width="662" alt="Screenshot 2024-10-12 at 9 30 04 PM" src="https://github.com/user-attachments/assets/41c51349-1f0a-4b7f-875e-2d639019a40e">

<img width="507" alt="Screenshot 2024-10-12 at 9 30 25 PM" src="https://github.com/user-attachments/assets/aef7b572-3070-40e9-b42f-c487d5c7dff1">

<img width="570" alt="Screenshot 2024-10-12 at 9 30 41 PM" src="https://github.com/user-attachments/assets/41e1bf8d-861b-46ec-945e-cdd8e3c18d8c">

## Query Descriptions:

Query 1:


Query 2:


Query 3:


Query 4:


Query 5:


Query 6:


Query 7:


Query 8:


Query 9:


Query 10:


## Database Info
