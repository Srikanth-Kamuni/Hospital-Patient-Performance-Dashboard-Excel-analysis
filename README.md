# Hospital Patient Performance Dashboard | Excel

## Project description
Excel-based hospital operations dashboard examining reported patient volume, ICU activity, readmissions, discharge outcomes and service performance across hospitals and clinical divisions.

## Problem statement
Hospital operations teams need consistent visibility into reported patient volumes, ICU activity, readmissions, discharge outcomes and waiting times across hospitals and clinical divisions. This Excel project consolidates the workbook’s aggregated patient-count fields into a dashboard for descriptive operational reporting. Because patient IDs repeat and several measures are counts within rows, the dashboard must not be interpreted as a unique-patient cohort or a validated clinical outcome study.

## Objectives
- Monitor patient-volume, ICU, death and readmission totals as reported in the workbook.
- Compare hospital, division, specialty, gender, city and discharge groupings.
- Examine waiting-time and discharge-day measures.
- Flag source-data quality and privacy issues before publication.

## Workbook structure
| Sheet | Purpose |
|---|---|
| Data | 136 source rows and 25 columns |
| Pivot | Aggregated KPI tables and category summaries |
| Dashboard | Visual reporting and filters |

## Headline metrics
| Metric | Value |
|---|---:|
| Source rows | 136 |
| Distinct patient IDs | 50 |
| Sum of Total Patients | 1,219 |
| Sum of Patients in ICU | 601 |
| Sum of Total Died | 144 |
| Sum of Re-admit Patients | 474 |
| Mean Avg Days of Discharge | 2.69 |
| Discharge dates before admission | 48 |
| Repeated patient ID rows | 86 |

**Note:** Patient-count measures are row-level numeric totals, not counts of unique individuals. The workbook contains 50 distinct Patient IDs.

## Data dictionary
| Field | Definition / caution |
|---|---|
| Admission Date | Recorded admission date; compare with discharge date for chronology. |
| Discharge Date | Recorded discharge date; some dates precede admission. |
| Hospital Name | Name of reporting hospital. |
| Hospital Country | Country recorded for the hospital. |
| Hospital State | State recorded for the hospital. |
| Patient ID | Patient identifier; repeats across source rows and must be anonymized. |
| Patient Name | Direct identifier; exclude from public datasets. |
| Gender | Recorded gender category. |
| Age | Recorded patient age. |
| Age Group | Source-provided age band; verify against age. |
| City | City recorded on the source row. |
| Division | Clinical or service division. |
| Department | Inpatient/outpatient service classification in this workbook. |
| Surgical Specialty | Clinical specialty grouping; not proof a procedure occurred. |
| Physicians | Recorded physician name; potentially identifying. |
| LOS Bucket (Length of Stay) | Source-provided length-of-stay band; verify against dates. |
| Patients in ICU | Numeric ICU patient count reported per row, not necessarily unique individuals. |
| Total Died | Numeric death count reported per row; cannot infer individual mortality. |
| Re-admit Patients | Numeric readmission count reported per row; not a patient-level readmission flag. |
| Discharge Type | Recorded discharge disposition. |
| Avg Waiting Time by Division (hrs) | Reported average waiting time in hours, row-level. |
| Avg Days of Discharge | Reported average days metric; source meaning requires confirmation. |
| Total Patients | Patient count associated with each row, summed for the dashboard. |
| Year | Reporting year supplied in workbook. |
| Month | Reporting month label supplied in workbook. |

## KPI calculations
- **Reported patients:** `SUM(Total Patients)`
- **ICU count:** `SUM(Patients in ICU)`
- **Reported deaths:** `SUM(Total Died)`
- **Readmissions:** `SUM(Re-admit Patients)`
- **Average discharge-day metric:** `AVERAGE(Avg Days of Discharge)` (unweighted)
- **Segment total:** `SUM(Total Patients)` grouped by a dimension.

## Data quality and limitations
- 86 repeated patient-ID rows beyond first occurrence.
- 48 discharge dates precede admission dates.
- Patient names, IDs and physician names must be removed or replaced before sharing source data publicly.
- Confirm the clinical definitions and reporting period before drawing operational conclusions.
- This is descriptive reporting, not validated clinical evidence or a patient-level risk model.

## Tools
Microsoft Excel (.xlsm), PivotTables, calculated KPI summaries and dashboard visualizations.

## Repository files
- `Hospital_Patient_Performance_dashboard.xlsm` (publish only after privacy review)
- `Hospital_Patient_Project_Documentation.pdf`
- `README.md`
## Hospital and Patient Performance Dashboard
<img width="1748" height="908" alt="Screenshot 2026-10-24 170551" src="https://github.com/user-attachments/assets/dfc90666-ce95-4e2d-983a-87d0affa26ff" />

## Portfolio summary
Built an Excel hospital performance dashboard from 136 reporting rows, using Pivot-based summaries to explore patient volumes, ICU counts, readmissions, discharge outcomes and operational waiting-time measures across hospitals and clinical divisions. Documented data quality and privacy limitations.
