# Truck Shipment Efficiency Dashboard – Glovis (Summer 2025)

This Power BI dashboard was built during my internship at Hyundai Glovis to monitor and improve weekly outbound/inbound efficiency of truck shipments by port.

---

## 🚚 Project Overview

Aimed at reducing dwell times and improving outbound flow, this dashboard highlights shipment inefficiencies across U.S. ports by tracking VIN-level vehicle movements, summarized weekly.

---

## 🧠 Business Logic

- **Inbound Event:** `TENDER_DATE` (unit released for shipment)
- **Outbound Event:** `SHIPMENT_DATE` (unit shipped)
- **Filter:** Only `TRANS_TYPE = 'Truck'` vehicles
- **Group By:** WeekStart × Port × Carrier × Customer
- **Ratio:** `Total Outbound Units / Total Inbound Units`

---

## 📊 Key Features

- **Outflow:Inflow Ratio Trendline**
- **VIN-level Drilldown Table**
- **Carrier & Customer Slicers**
- **Alert Flags:** Ratio drops, 3-week performance dips
- **Sparkline & Bar Charts** for past 12 weeks

---

## 🧱 Data Modeling

- Power Query used to create `InEvents`, `OutEvents`, `MasterEvents`
- Weekly aggregation logic using `WeekStart`
- Separate summary table `WeeklyRatios_Truck`
- Clean column naming, outlier detection, and scalable structure

---

## 🔄 Tools Used

- Power BI (Data modeling, DAX, visualization)
- MongoDB via ODBC (VIN-level raw data)
- Excel & Python (future automation and forecasting integrations)

---

## 📄 PDF Summary

[📎 Click to view the 1-page project summary (PDF)](./Truck_Shipment_Dashboard_Summary_Jacob_Lee.pdf)

> _Note: All data used in this project is either anonymized or generated for demonstration purposes only._

---

Feel free to connect with me on [LinkedIn](https://linkedin.com/in/jacob-lee-) or check out more projects at [github.com/jacobmlee29](https://github.com/jacobmlee29)
