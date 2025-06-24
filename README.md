# 🤖 UiPath_CalculateClientSecurityHash_Dispatcher
This is a UiPath automation project that logs into **ACME System 1**, scrapes all `Work Items`, filters them by **Description = "Calculate Client Security Hash	"**, and prepares them for processing by uploading them to an Orchestrator Queue.
## 📌 Project Purpose
Automate the extraction of specific transaction data from ACME System 1 based on business criteria and send the results to Orchestrator for further processing.
## 🔍 What It Does
- Logs into [ACME System 1](https://acme-test.uipath.com)
- Navigates to the **Work Items** page
- Extracts all available items using **Data Scraping**
- Filters items where:
  - `Type = WI5`
- Adds filtered items to the queue: **CalculateClientSecurityHash_Dispatcher**
## 🧰 Technologies Used
- UiPath Studio
- Data Scraping Wizard
- Orchestrator Queues
- Excel / Config file for **Settings & Assets & Exception Errors**
## 🚀 How to Run
1. Open `Config.xlsx` and verify:
   - ACMEURL
   - QueueName
   - Credentials (via Orchestrator Assets or Windows Vault)
3. Open **Main.xaml**
4. Run the Dispatcher process from UiPath Studio or Orchestrator
