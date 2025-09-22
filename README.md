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
