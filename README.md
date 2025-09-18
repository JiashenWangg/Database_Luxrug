# Amazon Store Database Design & Deployment

This project implements a full pipeline for managing, cleaning, analyzing, and visualizing data for an Amazon rug store. It integrates sales, returns, and customer reviews into a relational database, applies structured preprocessing, and produces business insights through statistical analysis and visualizations.

## Project Workflow

**1. Database Initialization – db_init.qmd**

	Designs and deploys normalized relational schemas for sales, returns, and reviews.

	Loads historical raw datasets into the database.

	Cleans and formats data types (dates, currencies, categorical values) to ensure integrity.

**2. Daily Updates – db_daily_update.qmd**

	Automates ingestion of new sales, returns, and reviews data.

	Deduplicates records and appends updates without overwriting historical data.

	Keeps the database synchronized with Amazon Seller Central exports.

**3. Data Preprocessing – data_prep.qmd**

	Consolidates sales, returns, and review data into unified, analysis-ready tables.

	Applies transformations such as:

		Standardizing product identifiers (SKU, pattern, size).

		Generating derived metrics (return rates, review scores, revenue per listing).

		Handling missing values and outliers.

		Outputs cleaned datasets used for statistical modeling and visualization.

**4. Data Analysis – data_analysis.qmd**

	Performs exploratory and statistical analysis on cleaned data.

	Investigates:

		Revenue trends by time, product pattern, and size.

		Return rate distributions and their drivers.

		Customer review sentiment and average star ratings.

		Uses regression and time-series techniques to identify patterns and causal relationships.

**5. Visualization & Insights**

	Built interactive R Shiny dashboards connected to the processed database.

	Key visualizations include:

		Time series plots of revenue, returns, and review counts.

		Faceted bar plots comparing product categories and sizes.

		Geographic maps of customer demand and return rates.

		Correlation plots linking reviews, returns, and sales performance.

	These visualizations support product strategy (pattern/size prioritization), ad targeting, and return mitigation.
