# Optimizing Global Sales Reporting with SAP BW/4HANA for Faster Decision-Making

**Candidate:** Samantha Yoong 
**Role Applied:** Junior Business Intelligence Analyst – BW  
**Industry:** Global B2B manufacturing & construction supply  
**Duration:** 3 months  
**Tech & Skills:** SAP BW/4HANA, Data Modelling, ETL, ABAP (basics), SQL, Tableau, Stakeholder Collaboration

---

## TL;DR (Why this matters)
- **Problem:** Large volumes + fragmented models slowed reports → decisions lagged by **4–5 business days**.  
- **Goal:** **Speed + timeliness** — optimize BW models for **faster queries** and enable **near real-time** updates for critical KPIs.  
- **Outcome:** <24h monthly close reporting, **2-hour** refresh for critical KPIs, **65%** runtime reduction, **0** Excel stitching.

---

## Background

In a global manufacturing company operating across 80+ countries, sales leaders struggled with **inconsistent** and **delayed** performance reporting.

The SAP BW landscape consumed data from multiple regional ERPs, but:
- Data models were **not standardized** across regions.  
- Sales KPIs required **manual Excel consolidation**.  
- **Large data volumes slowed report generation**, causing monthly reporting to take **4–5 business days**, delaying strategic decisions.

**My mandate:** review the existing reporting process, identify bottlenecks, and deliver a **faster, scalable, standardized** solution in **SAP BW/4HANA**.

---

## Objectives

1. Reduce monthly sales reporting time from **4–5 days** to **< 24 hours**.  
2. **Standardize KPI definitions** for global alignment.  
3. Enable **self-service reporting** for regional managers.  
4. **Optimize BW data models** for faster query performance and introduce **near real-time** reporting for business-critical KPIs.

---

## Architecture (High-Level)

```mermaid
flowchart LR
  A[Regional ERPs / S/4HANA] -->|ODP/Extractors| B[Staging (BW ADSOs)]
  B --> C[Transformations (ETL)]
  C --> D[Consolidated ADSO]
  D --> E[CompositeProvider (Global)]
  E --> F[BEx Queries / BW Queries]
  F --> G[(SAP Analytics Cloud / Tableau)]
  E --> H[Open ODS Views (Near Real-Time KPIs)]
  H --> F


