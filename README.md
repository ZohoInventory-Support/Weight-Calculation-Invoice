
	
# Weight-Calculation-Invoice
Calculates both the line item level weight and total weight of Items in an Invoice.

# Steps
# 1. Create 2 custom fields in the item module :

Settings > Preferences > Invoices > Field Customization > New Custom Field

1.Weight Per Item( API Field Name: cf_weight_per_item) 
	- Weight of the Item - To be filled during Item creation.
2.Overall Weight( API Field Name: cf_overall_weight) 
	- Script will calculate and update the line item weight. 
( Weight per item * quantity) 

# 2. Create 1 custom field in the invoice module:

1.Total Weight( API Field Name: cf_total) 
- To calculate and update the Total weight in Invoice.

# 3. Create Custom function

Settings > Automations > Custom Functions > New Custom Function 
Module: Invoice
Copy and paste the Weight Calculation Script.

Create connection for Zoho Inventory - zilink

# 4. Create workflow

Settings > Automations > Workflow Rules > New Workflow Rule

Module : Invoice
Workflow Type : Event Based
When an Invoice is: Created

Choose the appropriate custom function in the Action.
Save the workflow. On each invoice creation workflow automatically calculates the line item level weight and total weight of Items in an Invoice.
