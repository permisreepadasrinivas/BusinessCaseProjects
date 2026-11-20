# UrbanCart Retail – Raw Source Data (Landing Zone)



UrbanCart is a retailer with 12 stores (US, UK, India, UAE), an online store and a distributor in the UAE. These files are what the source systems "dropped" on the night of 16-Nov-2026. They are very messy.



|Folder|Source system|Format|How it arrives in real life|
|-|-|-|-|
|pos/|Store tills (POS)|CSV, one file per day|Nightly SFTP / blob drop|
|ecommerce/|Online store REST API|Paginated JSON|API call by pipeline|
|erp/|SAP ERP material master|Excel export|Scheduled report / gateway|
|crm/|CRM customers|CSV full export|Nightly full extract|
|distributors/|Gulf Distribution LLC|CSV (wk45), Excel (wk46)|Email / SFTP from partner|
|reference/|Stores, FX rates, distributor SKU mapping|CSV|Maintained by business teams|



Your job: land these in Bronze untouched, then build Silver (clean) and Gold (star schema) layers and a sales dashboard in USD across all channels.



Try to find the data problems yourself first. Then check ISSUES\_ANSWER\_KEY.md-

