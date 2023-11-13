
## Miniproject11: Data Pipeline with Databricks
### Purpose:
* The purpose of this mini-project is to build and deploy an end-to-end data processing pipeline using Databricks, focusing on ingesting, transforming, and analyzing data within a practical framework. Utilizing the Million Song dataset, the project aims to provide hands-on experience with Databricks features for ETL (Extract, Transform, Load) workflows, from data ingestion to querying transformed data.
* A comprehensive guide on how to build a pipeline can be found at: https://docs.databricks.com/en/getting-started/data-pipeline-get-started.html
### Analyze the data:
The results query are shown below:
This SQL query is designed to find which artists released the most songs each year from the 'prepared_song_data' table. It selects the name of each artist (`artist_name`), counts the number of songs by each artist (`num_songs`), and includes the year of release (`year`). The query focuses only on records where the `year` is greater than 0, thus excluding entries without a valid year. It then groups the results by `artist_name` and `year`, ensuring that the count of songs is organized by both artist and release year. Finally, the results are ordered first by the number of songs in descending order (to show the most prolific artists first) and then by year in descending order (to show the more recent years first).
<img width="882" alt="Screen Shot 2023-11-12 at 23 54 44" src="https://github.com/nogibjj/IDS706_miniproject11_xk10/assets/143849077/477fbeda-299e-4f17-a3b5-6eb063a46a51">

This SQL query is designed to curate a selection of songs ideal for a DJ list from the prepared_song_data database. It retrieves the artist's name, song title, and tempo of each track, filtering for those with a 4/4 time signature and a tempo ranging between 100 and 140 beats per minute. These criteria are chosen to identify songs with a steady, danceable rhythm, making them suitable for a DJ's playlist in settings like parties or dance events.
<img width="875" alt="Screen Shot 2023-11-12 at 23 55 02" src="https://github.com/nogibjj/IDS706_miniproject11_xk10/assets/143849077/322870ed-cca8-4b52-a4be-2182aa1f25e0">


### Steps:
1. Create a Cluster: First, create a compute cluster in Databricks, choosing 'Single User' access mode for full DBFS access and Unity Catalog compatibility.

2. Create 3 notebooks in Workspace:
* Ingest Raw Data: Use a Databricks notebook to load the raw data into a table, ideally utilizing Auto Loader for efficient and automatic data ingestion. Define the data schema explicitly due to the absence of header information in the dataset.
* Prepare Raw Data: Create another notebook to transform the raw data. This involves filtering out unnecessary columns, adding new fields, and storing the processed data in a new table.
* Query Transformed Data: Extend the pipeline with a notebook dedicated to querying the transformed data. This step is crucial for extracting meaningful insights from the processed data.
<img width="931" alt="Screen Shot 2023-11-12 at 23 52 53" src="https://github.com/nogibjj/IDS706_miniproject11_xk10/assets/143849077/c4c2ea14-b9af-4e29-9936-15a831baf1fa">

Make sure that raw data is loaded into the notebook and the data is transformed into database format and prepared for query
<img width="1491" alt="Screen Shot 2023-11-12 at 23 53 37" src="https://github.com/nogibjj/IDS706_miniproject11_xk10/assets/143849077/392a5be8-d4b1-421a-a403-2b572a054dc7">

3. Automate with a Databricks Job: Finally, automate the entire pipeline by creating a Databricks job. This job should sequentially run the data ingestion, processing, and analysis notebooks, ensuring a smooth and automated workflow.
<img width="838" alt="Screen Shot 2023-11-12 at 23 55 27" src="https://github.com/nogibjj/IDS706_miniproject11_xk10/assets/143849077/8202125b-45cb-4111-a2e5-84d5303147b8">
<img width="770" alt="Screen Shot 2023-11-12 at 23 55 46" src="https://github.com/nogibjj/IDS706_miniproject11_xk10/assets/143849077/7ce58168-58b4-4534-ad4e-38a4031f06b7">


