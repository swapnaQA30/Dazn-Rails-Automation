
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
1. Run Collection (Basic Execution)against Prod Environment
newman run Collections/HomePageRails-US-east-1.postman_collection.json
-e Environments/Production.postman_environment.json \

2. Run with HTML Report (Recommended)
mkdir -p Reports

Step 2: Run Newman with report
newman run Collections/HomePageRails-US-east-1.postman_collection.json \
-e Environments/Production.postman_environment.json \
-r cli,htmlextra \
--reporter-htmlextra-export "Reports/HomePageRails-US-east-1-$(date 
+%Y-%m-%d)-report.html" \
--reporter-htmlextra-title "Rails Validations Dashboard by 
swapna.bellamkonda"


Step 3: Open report in browser
open Reports/HomePageRails-US-east-1-$(date +%Y-%m-%d)-report.html



