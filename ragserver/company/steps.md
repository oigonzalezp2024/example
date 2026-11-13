# Installation and Execution Guide: RAG Server

## 1. Environment Variables Setup

You must set the following variables directly in your terminal before running the server.

### On Unix/Linux/macOS-based systems:

```bash
export GEMINI_API_KEY="YOUR_GEMINI_API_KEY"
export SERVERPORT="9020"
export WVPORT="9035"

```

### On Windows PowerShell:

```powershell
$env:GEMINI_API_KEY="YOUR_GEMINI_API_KEY"
$env:SERVERPORT="9020"
$env:WVPORT="9035"

```

---

## 2. Infrastructure with Docker

Navigate to the tests folder and spin up the containers:

```bash
cd tests/
docker compose up -d

```

---

## 3. Running the `ragserver`

Once the environment variables and Docker services are configured, open another terminal, navigate to the server directory, and start it with Go:

```bash
cd ragserver
go run .

```

---

## 4. PHP Integration

Open another terminal to run the PHP demo script:

```bash
cd /public/
php ragserver-demo.php

```

### Expected Output Example:

```powershell
PS public> php ragserver-demo.php
Indexing documents...
Array
(
    [status] => ok
    [http_code] => 200
)

Querying Gemini...
Based on the provided information:

*   Technical support hours for industrial maintenance are **Monday to Friday from 7:30 AM to 5:30 PM**.
*   The standard warranty for manufactured equipment lasts **12 months** and covers welding and structural defects.
PS public> 

```

---
