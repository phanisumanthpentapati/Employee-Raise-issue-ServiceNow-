# Employee Raise Issue Management System

## 📌 Project Overview

The **Employee Raise Issue Management System** is a custom application developed using the ServiceNow platform to help employees report workplace issues and enable the responsible teams to review and resolve them efficiently.

Employees can submit issues related to payroll discrepancies, HR policies, account access, and infrastructure problems through a structured Record Producer form. The submitted information is stored in a custom ServiceNow table for tracking and further processing.

The primary objective of this project is to digitize workplace issue reporting, organize employee requests, and establish a foundation for issue tracking and resolution.

## 🎯 Objectives

- Provide a simple and structured form for reporting workplace issues.
- Collect essential employee and issue details.
- Categorize issues for easier identification and handling.
- Store submitted issues in a custom ServiceNow table.
- Apply validation rules to improve data quality.
- Prepare the application for future automation, notifications, and issue tracking.
- Maintain project configuration and documentation in GitHub.

## 🛠️ Technology Stack

| Technology                  | Purpose                                      |
| --------------------------- | -------------------------------------------- |
| ServiceNow Platform         | Application development and issue management |
| ServiceNow Studio           | Custom application configuration             |
| Custom Tables               | Store employee issue records                 |
| Record Producer             | Provide the issue submission form            |
| Variables and Choice Fields | Collect structured input                     |
| UI Policies                 | Implement conditional form validation        |
| Business Rules              | Configure server-side record behavior        |
| GitHub                      | Source control and project documentation     |

## 🏗️ Application Architecture

The current application follows this basic workflow:

1. **Employee:** Opens the Employee Raise Issue form.
2. **Record Producer:** Collects employee information and issue details.
3. **Validation:** Mandatory fields help ensure required information is supplied.
4. **Custom Table:** The submitted issue is intended to be stored in the Employee Raise Issue table.
5. **Issue Management:** Authorized users can review records and manage their status as the project evolves.

```text
Employee
   |
   v
Employee Raise Issue Form
   |
   v
Record Producer
   |
   v
Field Validation
   |
   v
Employee Raise Issue Table
   |
   v
Review and Resolution
```

## 🗄️ Database Design

**Custom table:** `u_employee_raise_issue`

The table is designed to store workplace issue information.

| Field          | Purpose                                  |
| -------------- | ---------------------------------------- |
| Number         | Unique issue reference number            |
| Employee Name  | Name of the employee reporting the issue |
| Employee Email | Employee's contact email                 |
| Category       | Main type of issue                       |
| Subcategory    | Specific issue classification            |
| Description    | Details of the reported issue            |
| Priority       | Urgency of the issue                     |
| Requester      | User associated with the request         |
| Status         | Current state of the issue               |

The table includes fields for identifying employees, categorizing requests, and supporting issue tracking.

## 📋 Implemented Features

### 1. Custom Application

Created a custom ServiceNow application named **Employee Center** with a description focused on workplace issue reporting.

### 2. Custom Issue Table

Created the **Employee raise issue** table to maintain issue records.

### 3. Issue Categories

Configured categories for classifying employee issues:

- Payroll
- HR Policy
- Access Problem
- Infrastructure

### 4. Subcategories

Configured subcategories to capture more specific issues:

- Salary not credited
- Policy clarification
- Account access
- Laptop issue

### 5. Record Producer

Created a Record Producer named **Employee Raise Issue**, targeting the custom Employee raise issue table.

The form currently displays:

- Employee Name
- Employee Email
- Category
- Subcategory
- Description
- Priority

The form includes mandatory-field indicators for required information.

### 6. UI Policy

Configured a UI Policy to make the Description field mandatory when the issue status is New. This supports conditional form validation.

### 7. Source Control Setup

Connected the ServiceNow application to a GitHub repository through ServiceNow Source Control.

**Repository:** [Employee Raise Issue – ServiceNow](https://github.com/phanisumanthpentapati/Employee-Raise-issue-ServiceNow-)

The repository is intended to maintain project configuration and documentation. The latest configuration changes should be verified in GitHub before claiming they have all been committed.

## 🔄 Issue Submission Workflow

The intended workflow is:

1. Employee opens the Record Producer.
2. Employee enters their name and email.
3. Employee selects a category and subcategory.
4. Employee provides a description and chooses a priority.
5. Employee submits the form.
6. ServiceNow creates a corresponding issue record in the custom table.
7. The responsible team can review and process the issue.

**Note:** The end-to-end record creation and field mapping must be verified after submission to ensure every variable is saved to the intended table field.

## 🚀 Future Enhancements

### 1. Automated Assignment

Automatically route issues to the appropriate team based on category.

### 2. Email Notifications

Notify employees when an issue is submitted, assigned, updated, or resolved.

### 3. Issue Lifecycle Management

Implement a structured lifecycle such as New, In Progress, Resolved, and Closed.

### 4. Employee Portal

Provide an employee-facing interface for submitting issues and viewing their own requests.

### 5. Service Level Agreements

Introduce response and resolution targets based on issue priority.

### 6. Reports and Dashboards

Display issue counts, category-wise distribution, priorities, and resolution performance.

### 7. Access Control

Ensure employees can access only permitted records and authorized support teams can manage assigned issues.

## 💡 Expected Benefits

- Simplifies workplace issue reporting.
- Organizes employee requests in a central location.
- Improves categorization and visibility.
- Provides a foundation for automated routing and notifications.
- Supports future reporting and issue resolution workflows.

## 👨‍💻 Project Information

**Project Name:** Employee Raise Issue Management System
**Platform:** ServiceNow
**Application Name:** Employee Center
**Custom Table:** `u_employee_raise_issue`
**Record Producer:** Employee Raise Issue
**Version:** 1.0.0
**Repository:** [GitHub Repository](https://github.com/phanisumanthpentapati/Employee-Raise-issue-ServiceNow-)

## 📖 Conclusion

The Employee Raise Issue Management System establishes a foundation for handling workplace issues through ServiceNow. It combines a custom application, a dedicated issue table, categorized input fields, a Record Producer, and UI validation.

The next development phase focuses on verifying record creation and field mapping, improving issue lifecycle automation, and building a complete employee-facing portal with notifications, reporting, and access control.
