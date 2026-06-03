# Hospitality Dashboard Project

## Overview
This repository contains dashboards and analysis artifacts for a hospitality dataset (dashboards, visualizations, and SQL scripts used to prepare and summarize the data).

## Files in this folder
- Hospitality Dashboard Excel.xlsm — Macro-enabled Excel workbook with dashboards and analyses (Excel, macros/VBA).  
- Hospitality Dashboard PDF.pdf — Exported PDF of the dashboard/report.  
- Hospitality Dashboard Power BI.pbix — Power BI Desktop report (open with Power BI Desktop).  
- Hospitality Dashboard Tableau 2.twbx — Packaged Tableau workbook (open with Tableau Desktop).  
- Hospitality Dashboard Tableau.twbx — Packaged Tableau workbook (alternate or original workbook).  
- Hospitality Data Analysis SQL.sql — SQL script containing aggregated queries used for the analyses and dashboards.

## SQL script summary
The `Hospitality Data Analysis SQL.sql` file contains the primary queries used to generate metrics for the dashboards. Key queries include:

- Total revenue (sum of `revenue_realized` from `fact_bookings`).
- Occupancy and utilization calculations (using `fact_aggregated_bookings` and `capacity`).
- Cancellation rate (percentage of bookings with `booking_status = 'Cancelled'`).
- Total bookings (distinct `booking_id`).
- Daily and weekly trend analyses (revenue and bookings grouped by `check_in_date` and `week_no`).
- Weekday vs weekend revenue and bookings (joined with `dim_date`).
- Revenue by city/property (joined with `dim_hotels`).
- Room-class level revenue (joined with `dim_rooms`).
- Booking status summary (counts by `booking_status`).

Run these queries against the `hospitality` database (or the schema containing the listed dimension and fact tables) to reproduce the summary tables used by the dashboards.

## How to open / run

- Excel: open with Microsoft Excel and enable macros to view interactive dashboard elements.  
- Tableau: open the `.twbx` files with Tableau Desktop.  
- Power BI: open the `.pbix` file with Power BI Desktop.  
- SQL: run `Hospitality Data Analysis SQL.sql` in your SQL client connected to the hospitality database.

## Notes & suggestions
- Keep a copy of the raw data source used to build the dashboards.  
- If sharing on GitHub, consider exporting non-binary extracts (CSV sample of the data or documentation) and including a brief data dictionary.  

## License & Contact
This repository does not include an explicit license. If you want one, add a `LICENSE` file (for example, MIT).  

If you want, I can:  
- add this `README.md` to the repo,  
- create a short `LICENSE` file, or  
- commit these files to a GitHub repo and push (if you provide repo access or remote URL).
