# Amazon Store Database Design & Deployment

This project implements a relational database system to centralize and manage data for an Amazon rug store. The database integrates sales, returns, and customer reviews, ensuring streamlined access for analysis, reporting, and visualization.


## Project Overview

Database Design: Created normalized schemas to support sales, returns, and review records with referential integrity.

Initialization Script (db_init.qmd):

  Defines table structures and relationships.

  Loads raw datasets into the database.

  Performs initial data cleaning and transformation.

Daily Update Script (db_daily_update.qmd):

  Automates ingestion of new sales, return, and review data.

  Updates tables incrementally without disrupting historical records.

  Applies preprocessing steps (deduplication, type casting, date formatting).
  

## Key Features

Centralized Data Access: All Amazon store data stored in a single relational database.

Automated Pipelines: Daily update workflow ensures database stays fresh with minimal manual effort.

Analytics Ready: Data structures are optimized for queries, supporting business dashboards (R Shiny) and further statistical modeling.

Scalable: Designed to handle growing datasets as product lines and transactions expand.
