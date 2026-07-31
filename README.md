
# DAZN Rails Automation

## Project Type
Postman + Newman API Automation Framework

---

## 📌 Prerequisites (IMPORTANT)

Before running this project, install the following:

### 1. Install Node.js (includes npm)
Download and install:
https://nodejs.org/

Verify:
```bash
node -v
npm -v

2. Install Newman globally
npm install -g newman

Verify:
newman -v

3. Install HTML Extra Reporter
npm install -g newman-reporter-htmlextra

🚀 How to Run
1. Run Collection (Basic Execution)against Prod Environment with report
newman run Collections/HomePageRails-US-east.postman_collection.json \
-e Environments/Production.postman_environment.json \
-r cli,htmlextra \
--reporter-htmlextra-export "Reports/HomePageRails-US-east-Prod-$(date +%Y-%m-%d)-report.html" \
--reporter-htmlextra-title "Rails Validations Dashboard by swapna.bellamkonda"

After the run completes:To open the report
open Reports/HomePageRails-US-east-Prod-$(date +%Y-%m-%d)-report.html



2.Run Collection (Basic Execution)against Stage Environment with report
newman run Collections/HomePageRails-US-east.postman_collection.json \
-e Environments/Stage.postman_environment.json \
-r cli,htmlextra \
--reporter-htmlextra-export "Reports/HomePageRails-US-east-Stage-$(date +%Y-%m-%d)-report.html" \
--reporter-htmlextra-title "Rails Validations Dashboard by swapna.bellamkonda"

After the run completes:To open the report
open Reports/HomePageRails-US-east-Stage-$(date +%Y-%m-%d)-report.html




