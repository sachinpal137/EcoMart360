EcoMart360 - A Salesforce CRM for Eco-Friendly E-Commerce
This repository contains the configuration and documentation for EcoMart360, a custom Salesforce CRM application. It's designed to help eco-friendly e-commerce businesses streamline operations, automate order and inventory management, build customer loyalty, and gain sales insights. 




Phase 1: Discovery & Requirements
In this initial phase, we laid the foundation for the project.


Problem Statement: We identified the key challenges faced by eco-friendly startups, including manual order tracking, lack of a customer loyalty system, and poor visibility into sales trends. 


Requirements Gathering: We defined the core requirements for the CRM, such as the need to manage products, orders, and customers in one place, automate stock reduction, and provide sales dashboards. 



Stakeholder Analysis: We identified the primary stakeholders (Business Owners, Sales Team, Customers, Support Team) and mapped their expectations from the system. 


Business Process Mapping: We outlined the customer journey, from browsing products to placing an order and leaving a review. 

Phase 2: Salesforce Org Setup & Configuration
In this phase, we performed the initial technical setup inside a Salesforce Developer org.


Company Profile: We configured the company's information, time zone, currency, business hours, and fiscal year. 




User Setup: We created custom profiles and roles for "Sales Agent" and "Manager" users to ensure proper access and data visibility. 




Security: We established the foundational security model by setting the Org-Wide Defaults (OWD) for our key objects. 

Phase 3: Data Modeling & Relationships
In this phase, we built the complete data structure of the application.

Object Creation: We created the custom EcoProduct object to manage products and a custom Order Line Item junction object. We are using the standard 

Order object to manage sales. 

Fields & Relationships: We added essential fields like Price, Stock Quantity, and Category to our objects. We then established a master-detail relationship between 

Order and Order Line Item, and a lookup relationship between Order Line Item and EcoProduct. 


Phase 4: Process Automation
In this phase, we automated key business processes to improve efficiency.


Validation Rule: We created a rule to prevent users from creating an order for a product with a quantity of zero or less. 


Automated Calculations: We built a Record-Triggered Flow to calculate the subtotal on each Order Line Item and a Roll-Up Summary field to calculate the Total Amount on the Order. 


Approval Process: We set up an approval process to automatically route high-value orders to a manager for review before confirmation. 

Phase 5: Apex Programming
In this phase, we implemented advanced logic for real-time inventory management.


Stock Validation Trigger: We wrote a before insert Apex trigger on the Order Line Item object to check for sufficient stock and prevent the sale of out-of-stock items. 


Stock Reduction Trigger: We wrote an after update Apex trigger on the Order object to automatically reduce the stock quantity of products when an order's status is updated to "Confirmed."


Test Classes: We wrote comprehensive test classes for both triggers to ensure they work as expected and meet Salesforce's code coverage requirements for deployment. 

Phase 6: User Interface Development
In this phase, we focused on making the application user-friendly.


Lightning Record Page: We customized the Order record page using the Lightning App Builder, adding a visual Path component and organizing related lists into tabs for a better user experience. 



Utility Bar: We added a "New Order" quick action to the app's utility bar to allow for efficient record creation from anywhere in the app. 


Lightning Web Component (LWC): We built a custom productSelector LWC to allow users to search for available products and add them to an order with a single click, calling Apex methods to perform the search and create records. 



Phase 7: Integration & External Access
In this phase, we connected our Salesforce application with a mock external system.


Integration Configuration: We configured Remote Site Settings and a Named Credential to establish a secure and authenticated connection point to a mock external shipping API. 



Apex Callout: We wrote an asynchronous @future Apex method to make a REST callout to the external service to fetch mock tracking information. 


UI Action: We built a Screen Flow and a Quick Action button on the Order page to allow users to manually trigger the Apex callout.

Phase 8: Data Management & Deployment
In this phase, we managed the application's data and simulated a deployment.


Data Import: We used the Data Import Wizard to bulk-upload sample EcoProduct records from a CSV file. 


Data Quality: We created a Matching Rule and a Duplicate Rule to prevent users from creating duplicate EcoProduct records. 


Deployment Simulation: We created an Unmanaged Package and added all of the project's components (Objects, Apex Code, LWC, etc.) to simulate packaging our application for deployment. 


Phase 9: Reporting, Dashboards & Security Review
In this final development phase, we built analytics and performed a security review.


Reports: We created custom report types and built key reports, such as "Sales by Product Category" and "Orders by Status". 



Dashboards: We created a "Manager's Revenue Dashboard" with visual components like charts and graphs to provide an at-a-glance view of business performance. 



Security Review: We performed a final security check, verifying our Sharing Settings (OWD), adjusting Field Level Security (FLS) to make fields read-only for certain profiles, and confirming our org's Session Settings. 
