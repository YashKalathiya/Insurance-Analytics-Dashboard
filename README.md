# PRISM Insurance Analytics Dashboard

An interactive **Power BI dashboard** for exploring insurance policies, premiums, claims, and customer feedback. This project brings together a Power BI report, a policy/claims dataset, and a supplementary customer-feedback workbook.

## Project Overview

The dashboard is branded **PRISM INSURANCE PVT. LTD.** and is intended to help users explore insurance portfolio and claims information, including:

- Claim counts by claim status
- Premium amounts by policy type
- Claim amounts across age groups
- Active/inactive policy counts
- Summary metrics and policy-level details
- How results change when report slicers and visual interactions are used

The report currently contains one dashboard page. Open the PBIX file in Power BI Desktop to view the complete report and interact with its visuals.

## Dashboard Preview

Add a screenshot of the report here when publishing the repository. For example, save an image as `images/dashboard-preview.png` and replace the placeholder below:

<!--
![PRISM Insurance Dashboard](images/dashboard-preview.png)
-->

## Files in This Repository

| File | Description |
|---|---|
| `Insurance Dash Board.pbix` | Power BI report containing the dashboard visuals and report configuration |
| `InsuranceData.csv` | Main policy and claims dataset used for insurance analysis |
| `Insurance+Customer+Feedback.xlsx` | Supplementary workbook containing customer names and written feedback |
| `README.md` | Project documentation |

## Dashboard Visuals

The PBIX report includes visuals such as:

- **Number of Claims by Claim Status** — compares claim records by status.
- **Premium Amount by Policy Type** — compares premium totals across policy categories.
- **Claim Amount by Age Group** — explores claim amounts by age group.
- **Count of Active/Inactive Policies** — summarizes policy status.
- **Summary cards and a detail table** — provide headline figures and supporting data.
- **Slicers** — allow users to filter the report. The exact fields and interactions can be explored in Power BI Desktop.

## Dataset Details

### 1. `InsuranceData.csv`

The supplied CSV contains **10,004 rows and 13 columns**.

| Column | Description |
|---|---|
| `PolicyNumber` | Policy identifier |
| `CustomerID` | Customer identifier |
| `Gender` | Customer gender category |
| `Age` | Customer age |
| `PolicyType` | Policy category, such as Auto, Health, Home, Life, or Travel |
| `PolicyStartDate` | Policy start date |
| `PolicyEndDate` | Policy end date |
| `PremiumAmount` | Premium amount recorded for the policy |
| `CoverageAmount` | Coverage amount recorded for the policy |
| `ClaimNumber` | Claim identifier |
| `ClaimDate` | Date associated with the claim, when present |
| `ClaimAmount` | Claim amount recorded in the dataset |
| `ClaimStatus` | Claim status, such as Pending, Settled, or Rejected |

The CSV contains five policy types: Travel, Health, Auto, Life, and Home. Claim statuses in the supplied data include Pending, Settled, and Rejected.

**Data-quality note:** `ClaimDate` is blank for a number of records in the supplied CSV. Check the intended business meaning of these blanks before treating them as missing data or assuming they indicate a particular claim outcome. The dates appear in `DD-MM-YYYY` format in sample rows; verify the locale and data type during import.

### 2. `Insurance+Customer+Feedback.xlsx`

The workbook contains a sheet with two columns:

- `Customer Name`
- `Feedback`

It contains **97 feedback records** in the supplied file. This workbook is a supplementary qualitative data source; confirm whether and how it is connected to the Power BI model before assuming that it affects the dashboard visuals.

## Tools and Technologies

- **Microsoft Power BI Desktop** — dashboard creation and interactive reporting
- **CSV** — structured policy and claims data
- **Microsoft Excel (`.xlsx`)** — customer feedback data

## Getting Started

1. Clone or download this repository.
2. Install or open **Microsoft Power BI Desktop**.
3. Open `Insurance Dash Board.pbix`.
4. If Power BI reports that a data source cannot be found, update the source path to the local `InsuranceData.csv` file (and to the feedback workbook if it is used by the model).
5. In Power BI Desktop, use **Transform data** or **Data source settings** to review the file paths and data types.
6. Apply any changes, refresh the report, and explore the slicers, charts, summary cards, and detail table.

Power BI menu names may differ slightly by version. If you move the project to another computer, you may need to update file paths and refresh the data.

## Suggested Repository Structure

```text
.
├── Insurance Dash Board.pbix
├── InsuranceData.csv
├── Insurance+Customer+Feedback.xlsx
├── README.md
└── images/
    └── dashboard-preview.png
```

The `images/` folder and preview image are optional; add them if you want the dashboard to appear directly on the GitHub repository page.

## Notes and Limitations

- Dashboard values depend on the data model, transformations, measures, and filters configured in the PBIX file.
- Confirm the definition used for active/inactive policies and any calculated age groups before interpreting those visuals.
- Blank claim dates and claim statuses should be validated against the data owner's definitions.
- The dashboard supports descriptive analysis; observed patterns do not establish causation or guarantee future outcomes.
- The feedback workbook contains customer names and written feedback. **Review privacy, consent, and data-sharing permissions before publishing it publicly.** Consider removing or anonymizing personally identifiable information before uploading the repository.

## Potential Enhancements

- Add a dashboard screenshot or GIF.
- Document key DAX measures and Power Query transformations.
- Add a data dictionary explaining business definitions and KPI calculations.
- Document how policy status and age groups are calculated.
- Add a short methodology section describing data cleaning, missing-value handling, and date parsing.
