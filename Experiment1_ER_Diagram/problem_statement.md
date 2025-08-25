# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - GEETHU R

## Scenario Chosen:
 Hospital 

## ER Diagram:
<img width="817" height="487" alt="Hospital Building" src="https://github.com/user-attachments/assets/561e306f-6fa1-49a2-8372-4b4070127a92" />

## Entities and Attributes:
 - Patient: PatientID, Name, Age, Gender

 - Doctor: DoctorID, Name, Specialization

 - Ward: WardID, Capacity

 - Treatment: TreatmentID, Description

 - Appointment: AppointmentID, Date, Time

## Relationships and Constraints:
1.Contains (Ward – Patient)

 - A ward contains many patients.

 - (1:N relationship → One ward can contain many patients, but each patient is assigned to one ward).

2.Consults (Patient – Doctor)

 - A patient consults a doctor.

 - (M:N relationship → One patient can consult multiple doctors, and one doctor can consult multiple patients).

3.Assigned (Patient – Treatment)

 - A treatment is assigned to a patient.

 - (1:N relationship → One patient can have multiple treatments, but each treatment belongs to one patient).

4.Schedules (Doctor – Appointment)

 - A doctor schedules appointments.

 - (1:N relationship → One doctor can schedule multiple appointments, but each appointment is with one doctor).


## Extension (Prerequisite / Billing):
Billing can be an extra entity with BillID, Amount, PaymentMode linked to Patient & Treatment.

## Design Choices:
 - Primary Keys (like Patient ID, Doctor ID, Appointment ID, etc.) ensure unique identification.

 - Ward–Patient relation chosen as 1:N since wards have multiple patients but each patient belongs to one ward.

 - Patient–Doctor relation chosen as M:N because patients may consult multiple doctors and doctors handle multiple patients.

 - Separate Appointment entity was created to clearly store scheduling details instead of keeping them inside Doctor or Patient.

 - Treatment entity was introduced to record specific procedures/medications linked to a patient.

## RESULT
The ER diagram models hospital data with patients, doctors, wards, treatments, and appointments effectively.
