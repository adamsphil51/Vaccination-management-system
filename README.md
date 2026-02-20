# Vaccine Management System – Kenya

This project simulates a **Vaccine Management System** database, designed for tracking vaccine administration, stock levels, and reporting KPIs in a public health setting in Kenya.

---

## **Purpose**
The system supports:

- Tracking of patients and their vaccinations
- Vaccine stock management across facilities
- Monitoring immunization coverage and gaps
- Analytics for public health decision-making

---

## **Database Structure**
The project includes the following tables:

- **patients** – Stores patient details (names, age, gender, city)  
- **vaccines** – Stores vaccine types, manufacturers, and expiry dates  
- **vaccinations** – Tracks which patient received which vaccine, when, and by which health worker  
- **health_workers** – Staff administering vaccines across facilities  
- **facilities** – Clinics and vaccination centers  

**Relationships:**  
- `vaccinations` references `patients`, `vaccines`, and `health_workers`  
- `health_workers` belong to a `facility`  
- Data integrity enforced with primary/foreign keys, constraints, and realistic sample data  

---

## **Features**
- Maintains accurate vaccination records per patient  
- Tracks vaccine stock by batch, manufacturer, and expiry  
- Supports queries for immunization coverage by facility or region  
- Generates KPI reports for health ministry dashboards  

---

## **Sample Data**
- 8–10 sample patients across multiple cities  
- 5 health workers in different facilities  
- 3–5 vaccine types (e.g., AstraZeneca, Pfizer, Moderna)  
- Vaccinations recorded with dates and doses  

---

## **Analytics / KPIs**
See `analytics_queries.sql` for:

- Total vaccinations administered  
- Vaccinations per vaccine type  
- Health worker performance (vaccines administered)  
- Facility-level vaccination counts  
- Patient vaccination coverage  

---

## **Technologies**
- **SQL (PostgreSQL)** – Database design, sample data, queries  
- **Analytics-ready** – Prepares dataset for dashboards and BI analysis  

--

## **Usage**
1. Clone this repo  
2. Run `schema_and_data.sql` to create tables and load sample data  
3. Run `analytics_queries.sql` to generate KPIs and reports  
