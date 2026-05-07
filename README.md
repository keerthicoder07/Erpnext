### Sample Erp

Erpnext sample

### Installation

You can install this app using the [bench](https://github.com/frappe/bench) CLI:

```bash
cd $PATH_TO_YOUR_BENCH
bench get-app $URL_OF_THIS_REPO --branch develop
bench install-app sample_erp
```

### Contributing

This app uses `pre-commit` for code formatting and linting. Please [install pre-commit](https://pre-commit.com/#installation) and enable it for this repository:

```bash
cd apps/sample_erp
pre-commit install
```

Pre-commit is configured to use the following tools for checking and formatting your code:

- ruff
- eslint
- prettier
- pyupgrade

### CI

This app can use GitHub Actions for CI. The following workflows are configured:

- CI: Installs this app and runs unit tests on every push to `develop` branch.
- Linters: Runs [Frappe Semgrep Rules](https://github.com/frappe/semgrep-rules) and [pip-audit](https://pypi.org/project/pip-audit/) on every pull request.


### License

mit


%Introduction%
    The ERP next is a open source which used to build app for all the comapnies form small scale to large scale for their enterprise maitainance including accouting,crm etc and since it is the open source where any one can use to build their app and can deploy in the frappe cloud or any other cloud platform so it is easy to maintain for the users and have their own flexibility and customizations.

%company doctype%
    Where it contains the company details and where we can also manage group of company if client have and they can easily manage it

    %COA%
    In this they can also maintain all their company accounts as one by merging it and they can have COA by the standards or buy cutomizing it they can also take the structure COA from other company template and if the company is child or sister company the parent company COA will apply to it

    %Default%
    In this we can set the default of the company like letter head etc

    %Accounts%
    In this we can set banck accounts for each every transaction for example for employee they can maintain in one bank account and for suppliers a separate account and for the payables separate account like that so they can manage the accounts separately and easy to maintain accounts and cash flow

    %Bank Remittance Settings%
    In this where they can make multiple transactions in the single flow and not to have separate flow for each and every bank transactions

    %Exception Budget approver%
    Who have the access to approve the expense that exceeds the default budget and only that person can approve the expense that exceeds.

    %Delete%
    In this where the owner or the administrator can clear all the transactions and invoices of the company but it should be done cautios because once it is deleted then it cannot be retrived

    %System Settings%
    In this where we can set the default like language,time and country then where we can set the session settings and login methods,then default email settings of the company and the uploading of the files, they can also disable the notifications,they can also set the default backups and control the backgroud jobs and can reduce their usage by restricting to run once in a day

    %Global defaults%
    In this where we can set the defaults values like company name,currency and coutry etc

    %Domain settings%
    By using this we can disable the domain that should be disable and user cannot use it

    %Set settings%
    In this where we can set the language for particular user
    In precison where we can set precision for the particular user
    In show or hide modules we can access in the ERP home page but it is depreceated in from V15

    %Data Import%
    This is the important feature let assume the customer wants to upload their old of 500 data we cannot do the manual entry so we use the excel,csv or google sheets to upload the bulk data  so where we have two options first the insert new records and next is update the existing data 

    * First we should download the template by choosing the doctype with the needed fields then we can easily do the changes or enter the data
    *second we should not give the duplicate data then it shows duplicate data error and we should not change the field name after we create the data import document then also it shows error 
    *third where we can import the files from local,library or from the google sheets and where if it is google sheets we dont want to import the always the file from local and where if we use the google sheets we should keep the public access for that file and we should only copy and give the url tab link
    *If any error it will throw the error in each row if not it will add that data 
    *During the update of record we cannot change the id of any record
    * we should not also give large data like 50000 so we split and add the data

    %Chart Of Accounts Importer%
    Where we can import the structure of chart accounts using this tool before making any transactions where we can download the template and can edit according to the user and can import that for the change of structure and if it is the child company then parent company should give the permission to chnage the structure else the same parent's coa itself apply for that company also

    %Export%
    In this we have the export tool where we can export the data as csv or excel and even we can filter out the data we needed and the second option is download the backups of db where by default it saves every 8 hours and we can set number to take backups to download at the time and even we have the facility to take the backups from cloud and we can also send the download link files in the email including the public and private and we can also encrypt the backups to make more safe

    %Bulk Operations%
    Bulk update
        where we can bulkly update the particular field of the doctype instead we manually changes every thing and we can also set how many records to update at the time 
    Bulk rename
        where it is used to rename the id of the documents where it is only applicable to non-core doctypes we cannot change the id for core doctypes
    Delete company transactions
        where using this tool we can delete company transactions like doctypes and records and where it is irreversible so we should handle it more carefully and only the owner and administrator have that access to delete it
    
    %Personal Data%
        where using this tool we can dowload the personal data as json file using request data url and can see the request record in personal data download request as same we can also request the delete account using the request delete and can delete the personal data account by verfying through email or in by showing the link in the website for that particular user
    
    %user permissions%
        Where we can manage the customers,employee and all other members who involve in this company and we can set the permissions also based on the role,document,and field also so we can maintain the data securely and also we set the user permissions and can choose the doctype to the users to access that alone and can also in advanced we can set the value based permission also so we can manage best user management
    
    %Role permssions%
        Here I learned hoe to keep the read write permissions to the particular users and learn how to keep the perm levels and learnt about the perm level errors where we should fix the system manager level as 0 or remove the perm level 1 or 2 for that user and learnt about maxiumu user limit based on subscription
    
    %Open invoice creation tool%
        Let's keep scenario when a customer comes new to the ERP they have unclose invoices which is used to maintain the accounting and ledger so to import that bulk data we use open invoice creation tool and where we can create new supplier or customer using the create missing party where it automatically add in the supplier table or customer table 
    
    %period closing voucher%
        Where it is used to close the fiscal year expenses of that company which is used to calculate the profit and losses and completely close that year accounts and if any payable or recivables is pending where during the audit they can create another period closing voucher and can make a journal entry to add that expense or income to the same fiscal year
    
    %Accounting Period%
        Where the accounting period is used to create the fiscal year where after that period we cannot create any sales or purchase orders which will block because to maintain the audit intergrity and where we cannot create the journal entry also if the period is closed

    %Fiscal Year%
        Where the fiscal year is similar to the financial year where it can be even fix as default and also can set less or more than 12 months and we can mention the companies which will come under that fiscal year
    
    %Mode of payment%
        where we can set the mode of payment for each company to maintain the point of sales(pos) and where we can create the mode of payment and can use it during the payment entry
    
    %Payment Term Templates%
        where it hepls during the payment request where we can set the payment template first to get the advance and next after the completion of shipping or job we can transfer the remaining 70 % of money so it is easy to maintain the payments
    
    %Sales Taxes and Charge Template%
        This is the template where we can define the tax and charge template for the sales in this we have 5 types of tax they are
            actual-fix amount
            on previous row amount-where it includes only the tax amount of the reference row
            on prevoius row total-where it includes tax amount for that whole total
            on net amount-where it will apply the tax on net total
            on item quantity-where it will apply the tax on each and every item 
        
        where we can also keep the item tax template for the particular item even if the default is applied it overrides where we can see in the tax breakup
    
    %Purchase Taxes and Charge Template%
        Where it also follows the same tax engine but where it apply to suppliers instead of customers
    
    %Tax Rule%
        Instead of selecting the the tax category manually for each and every customer during the sales order or sales invoice where we can define rules where it will automatically set so there will be no human error and where we should only maintain the either rule or tax template for each item else where it will creates the duplicate tax entry
    
    %Tax category%
        This can be set in the rule and tax template to choose the tax according to the state and nations for example for state it applies the sgst+cgst and if it is between the inter states there separate category will applies so it helps to mainitain the tax for varsius scenario and where we can even set that in the account master to apply by default
    
    %Tax Template%
        where for each customer we can fix the separate the tax template what type of taxes should be apply and where we can also fix that for both suppliers and customers according to sales and purchase and it also easy to mainitain the tax for each and every customers and suppliers
    
    %Item Tax Template%
        In this template where some items or group of items will have the separate tax for them so to exclude that from standard tax we sue this template even if the default is apply for that invoice or order where it will override that apply the item tax template rate to that particular product
    
    %Tax witholding template%
        Where durting the sales or purchase payments if any tds or tcs is applied it also adds or deducts in the grand total and reflects as three ledger entry in account ledger one as debit or credit of accounts and the tds debit or credit so it easy to maintain the goverment taxes
