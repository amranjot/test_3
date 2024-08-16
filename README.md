# DPP

This document provides instructions for setting up and running the DPP application.

## Pull the Latest Changes

To ensure you have the latest changes, run:

```sh
git pull

```
## Script Directory: script

### File 1: monitoring.py :- This script monitors a specific directory for changes (modifications and deletions) to PDF files and calls an API with updated file data.
  
#### Variables to be changed in monitoring.py:
  * API_URL: The URL for the API endpoint.
  * DIRECTORY: The directory path to monitor.
  * API_CALL_INTERVAL: Time interval for API calls.
  * BATCH_INTERVAL: Time interval for batching file changes.
  * DEL1ETE_CHECK_DELAY: Delay before checking deleted files.

### File 2: upload_and_delete.py :This script provides an API for uploading and deleting PDF files, using FastAPI.

##### Variables to be changed in upload_and_delete.py:
  * UPLOAD_DIRECTORY: The directory path to save the uploaded files.
  * faiss_index_path: The path to the FAISS index.
  * docstore_path: The path to the docstore.json file.


### Run scripts (monitoring.py and upload_and_delete.py)
* python3 script/monitoring.py
* python3 script/upload_and_delete.py

##### Start the Server
* python3 manage.py runserver



- Commands for migrations
python3 manage.py makemigrations products
python3 manage.py migrate
python3 manage.py runserver


