# Online Aadhaar System

This project implements a **Database Management System (DBMS)** for managing Aadhaar services, appointments, enrolments, and related entities. It includes the **ER diagram, relational schema, functional dependencies, normalization up to BCNF and 4NF**, and detailed decomposition.

---

## 📌 **Project Overview**

✅ **Designed an efficient database of Online Aadhaar Card System in PostgreSQL inspired from the [UIDAI government website](https://uidai.gov.in/).**

✅ The concepts used were **Enhanced Entity Relationship (EER) Diagram, Relational Schema, Functional Dependency Closure, BCNF and 4NF decomposition** to make this project robust and well-structured.

✅ It was **implemented on pgAdmin** using **PostgreSQL** as the database management system.

---

## 🗃️ **Database Design Highlights**

* **Entities Designed**

  * **Citizen** (Personal details and EC mapping)
  * **Enrollment Centre** (EC details and types)
  * **Employee** (Works in Enrollment Centres)
  * **Appointment & Appointment For** (Booking and status tracking)
  * **Registered User** (Aadhaar to Citizen mapping)
  * **Documents** (Documents submitted per user)
  * **Aadhar Services** (Lock status, EKYC, Fetch & Payment history)
  * **Bank Account** (Account and IFSC mapping)
  * **Online Check Status** (Status of Aadhaar services)
  * **Update Requirement & Update Document** (Fee and document required per update type)
  * **All Status** (Status types)
  * **Avail Services** (VirtualID to Aadhaar linkage)

* **Normalization:**

  * All relations decomposed to **BCNF** or **4NF** to remove partial, transitive, and multivalued dependencies.
  * For example:

    * *Citizen* decomposed to handle locality, pincode, and state dependencies.
    * *Aadhar Services* decomposed to separate multivalued dependencies for **FetchHistory** and **PaymentHistory**.

---

## 📄 **Normalization Example (Citizen Table)**

| Attribute | Functional Dependency                                                |
| --------- | -------------------------------------------------------------------- |
| CitizenNo | → Fname, Gender, Mname, Lname, Locality, State, Pincode, DOB, EC\_ID |
| Pincode   | → State                                                              |
| Locality  | → Pincode, State                                                     |

**Decomposition:**

* R1(CitizenNo, Fname, Gender, Mname, Lname, DOB, EC\_ID)
* R2(Pincode, State)
* R3(Locality, Pincode, State)

---

## 🛠️ **Tools & Technologies Used**

* **Database Concepts:** EER Modelling, Relational Mapping, FD closure, BCNF/4NF decomposition
* **RDBMS:** **PostgreSQL**
* **Database IDE:** **pgAdmin**
* **Diagramming Software:** Draw\.io / MySQL Workbench for ER and relational diagrams
* **Documentation:** Structured derivation of dependencies and normal forms

---

## 💡 **Learning Outcomes**

* Designed normalized relational schemas from a real-world identity management use case
* Applied **functional dependency analysis and decomposition** systematically
* Understood multivalued dependencies and their implications in design
* Gained practical experience in **PostgreSQL database implementation using pgAdmin**

---

## 📁 **Project Structure**

* **ER & Relational Diagram:** Entity definitions with relationships
* **Functional Dependencies & Closure:** For each entity
* **Normalization:** Up to BCNF and 4NF wherever required

---

## ✍️ **Author**

* **Name:** Utsav Pansuriya
* **GitHub:** [UtsavPansuriya](https://github.com/UtsavPansuriya)

---

## 🚀 **How to Use**

1. Review the ER and relational diagrams to understand entity relationships.
2. Refer to **Functional Dependencies and Normalization** section for schema decomposition logic.
3. Implement schemas directly into **PostgreSQL using pgAdmin** using the normalized table structures.

---
