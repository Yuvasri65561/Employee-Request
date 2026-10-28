# Employee Requests Installation of Licensed Software through the Service Catalog (ServiceNow)

## 📌 Overview
This project manages employee requests for installing licensed software through the ServiceNow Service Catalog. Employees submit a structured request, the request goes through a manager approval workflow, and a fulfillment task is created for the Software team.

The project manages the request process within ServiceNow. It does not automatically install software on an employee's computer.

## 🎯 Problem Statement
Without a structured request process, software installation requests may be:

* Submitted inconsistently
* Difficult to approve and track
* Missing a clear record of the work required by the IT team

## 💡 Solution
This project uses a ServiceNow Service Catalog item and a workflow to:

* Collect request details through catalog variables
* Create Request (REQ) and Requested Item (RITM) records
* Route the request for Manager Approval
* Create a catalog task (Software Fulfillment Task) after approval
* Assign the task to the Software assignment group

**Process flow:**
Employee → Service Catalog → REQ/RITM → Manager Approval → Catalog Task → Software Support Team → Task Processing → Status Tracking

## 🛠 Tech Stack

* Platform: ServiceNow
* Interface: Service Portal / Service Catalog
* Components: Catalog Item, Catalog Variables, Workflow Studio, Approval, Catalog Tasks, Assignment Groups
* Data: Request (`sc_request`), Requested Item (`sc_req_item`), Catalog Task (`sc_task`)
* Deployment: Update Sets
* Version Control: Git & GitHub

## 🧾 Catalog Item and Variables
**Catalog item:** Software Installation Request (Software category)

| Variable | Purpose |
|---|---|
| Software Name | Name of the software requested |
| Version Required | Required software version |
| License Justification | Reason the employee needs the software |
| Urgency | Normal, High or Critical |

## ⚙️ Workflow
**Software Request Workflow** (on the Requested Item table):
Ask For Approval (Manager Approval) → If Approval Approved → Create Catalog Task → assigned to the **Software** group

**Update Set:** Licensed Software Installation - Capstone (exported, imported, previewed and committed in the target instance)

## 🚀 Key Features

* Structured Service Catalog request form
* Automatic REQ and RITM creation
* Manager approval before fulfillment
* Automatic fulfillment task creation and assignment
* Request traceability through REQ, RITM and SCTASK records
* Configuration packaged in an Update Set

## 🎥 Project Demo Video
The demo video is available in the **Demo Video** folder of this repository.

## 📈 Future Enhancements

* Automatic license availability checking and inventory validation
* SLA tracking
* Additional approval routing
* Integration with a software deployment tool
* Catalog UI Policies, email notifications, and reports and dashboards

## 📄 Documentation
The repository contains folders for each project phase:

* Ideation Phase
* Requirement Analysis Phase
* Project Planning Phase
* Project Design Phase
* Project Development Phase
* Project Documentation
* Project Demonstration

## 👩‍💻 Author
Developed by Malla Yuvasri (Student ID: 23NU1A4227)

📧 Contact via GitHub profile for collaboration or queries.
