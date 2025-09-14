EcoMart360 - A Salesforce CRM for Eco-Friendly E-Commerce
This repository contains the configuration and documentation for 

EcoMart360, a custom Salesforce CRM application. It's designed to help eco-friendly e-commerce businesses streamline operations, automate order and inventory management, build customer loyalty, and gain sales insights.

Phase 1: Discovery & Requirements
In this initial phase, we laid the foundation for the project.

Problem Statement: We identified the key challenges faced by eco-friendly startups, including manual order tracking, lack of a customer loyalty system, and poor visibility into sales trends.

Requirements Gathering: We defined the core requirements for the CRM, such as the need to manage products, orders, and customers in one place, automate stock reduction, and provide sales dashboards.

Stakeholder Analysis: We identified the primary stakeholders (Business Owners, Sales Team, Customers, Support Team) and mapped their expectations from the system.

Business Process Mapping: We outlined the customer journey, from browsing products to placing an order and leaving a review.

Phase 2: Salesforce Org Setup & Configuration
In this phase, we performed the initial technical setup inside a Salesforce Developer org.

App Creation: We created a new Lightning App named "EcoMart360" to serve as the main workspace for users.

Custom Object: We built a custom object named EcoProduct to store all information related to the eco-friendly products.

Custom Fields: We added several custom fields to the EcoProduct object to store key information, including:

Price__c (Currency)
Category__c (Picklist)
Stock_Quantity__c (Number) 

Tabs & Navigation: We created a custom tab for the "EcoProducts" object to make it accessible and configured the app's main navigation bar.

Documentation: We took screenshots of all key setup steps and uploaded them to the repository for documentation purposes.
