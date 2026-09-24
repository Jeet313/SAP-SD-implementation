# SAP-SD-implementation Project
SAP S/4HANA SD – End-to-End Order-to-Cash (O2C) Greenfield Implementation 

Client Information 

• Client: Aztech Solutions Pvt. Ltd. 

• Implementation Type: Greenfield Implementation 

• Module: SAP S/4HANA Sales and Distribution (SD) 

• Environment: SAP S/4HANA 

• Duration: 5 Days 

• Prepared by: Gourab Karmakar


Aztech Solutions Pvt. Ltd. is a retail trading organization specializing in garment distribution through multiple sales channels. The company previously managed sales orders, pricing, inventory, deliveries, and invoicing using manual spreadsheets, resulting in pricing inconsistencies, delayed order fulfilment, and poor inventory visibility.To modernize its sales operations, the company decided to implement SAP S/4HANA Sales & Distribution through a Greenfield Implementation, where the complete SD organizational structure and business process were designed from scratch.
The objective of this project was to automate the complete Order-to-Cash (O2C) lifecycle while integrating pricing, logistics, inventory, billing, revenue accounting, consignment, and advanced returns


The implementation was designed to achieve the following business goals:

Enterprise Structure
Configured the SAP SD organizational structure including:
- Company Code - 1000
- Plant - 1200
- Sales Organization – MNX1
- Distribution Channel – 4J
- Division – HJ, HK
- Sales Office – AFS9
- Sales Group – 4Q, 4B
- Shipping Point – FXL9

👉 [Screenshot: - Sales area data customer]

2️⃣ Business Partner & Master Data
- BP Group – GMCS, Number Range – 14
- Account Group – GSX9, Number Range – 03
- Partner group - JXCX
- Business Partners – SP, SH, BP, PY
- Customer Company Code Data - 1000
- Business Partner Number – 9900000520
- Customer Number - 1000000115 

👉 [Screenshot - Sales area data customer]

 4️⃣ Pricing & Condition Technique

- Condition Tables - 547
- Access Sequences – ASD9
- Condition Types – XRK0
- Pricing Procedure – RVAA01
- Pricing Procedure Determination - MNX1,4J, HJ, A, 1, RVNN01, XRK0
- Customer pricing procedure – 1
- Document pricing procedure - A


👉 [Screenshots - VK11, OVKK]

 5️⃣ Shipping & Logistics
- Shipping Point Determination -  02, 0001, 1200
- Shipping Conditions – 02 
- Loading Group - 0001
- Plant – 1200
- Shipping Point – FXL9
Inventory verification was performed using:
MIGO 
- Material – 3812
- Quantity – 1000 (PC)
- Storage location – 0001
- Plant - 1200
MMBE
- Batch Number -  0000000461

👉 [Screenshots: - Shipping Point determination, MMBE stock overview post]

 6️⃣ Credit Management
- Credit Control Area – HJ09
- Risk Category – D01 (High Risk Customer), D02 (Medium Risk Customer), D03 (low Risk Customer)
- Credit Limit – 10000/-
- Credit groups – Z1 (Block at sales order level), z2 (Block at delivery level), z3 (Block at PGI level)

👉 [Screenshots:- Automatic credit control, Maintain credit limit in FD32]

 7️⃣ Text Determination (VOTXN)

- Customer - 1000000115
- Text Type - TC01
- Text Procedure - C1
- Account Group - Gsx9+C1
- Text Added - No Guaranteed Replacement After 10 Business Days

Sales Order - 
- Text Type - TC02
- Text Procedure - C2
- Acc Seq - 26

Delivery - 
- Text Type - TC03
- Text Procedure - C3
- Acc Seq - 27

Invoice - 
- Text Type - TC04
- Text Procedure - C4
- Acc Seq - 28


👉 [Screenshots:- Text ID in customer, Text procedure with account group, Customer text procedure, sales order header text tab, delivery header text, invoice header text]

 8️⃣ Revenue Account Determination & SD–FI Integration

Configured revenue account determination to integrate SD billing with Financial Accounting.
- Table – 514
- Access Sequence – HH9
- Condition type – NEX7
- Account Determination procedure – KL07
- G/L Account - 175000

👉 [Screenshots:- Revenue account with G/l account, Vf03 Environment Revenue Account]

9 Tax Determination

- Condition Table - 554
- Access Sequence - JXTX
- Condition Type – 
 - JXSG (SGST @5%)
 - JXCG (CGST @5%)
 - JXIG (IGST @10%)
 - JXUG (UGST @10%)
Pricing procedure – RVNN01

👉 [Screenshots:- Tax category for country, Customer tax maintain, Material tax maintain, Sales order billing tax applied]

Note - I upload all releveant screenshots for each section and also upload a Presentation in PDF format you can easily view it by this name "My_SAP_SD_project". Also i uploaded Root Cause Analysis(RCA) register in Excel format the issues i've faced and solved during Unit testing.
