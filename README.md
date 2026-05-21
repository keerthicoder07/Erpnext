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
    
    %TCS%
        For this where we can only apply with cumulative threshold and we assign to the customer and where it automatically saves
    
    %Lower Deduction Certificate%
        Where this apply when some suppliers have comes under some scheme and the normal tax not applied then we use the lower deduction certificate where if normal tax has 5% and by using it we can have 1% for that particular supplier
    
    %Tax applies on Total or valuvation%
        where it is mainly used in maintaining the balance on the accounts of inventory if it is the total where it just affects the supplier payable like the tax of gst,vat etc and the valuvation just increase the stock like we use internal transportation and where if both gst and transportation done by the supplier both the total and valuvation increases
    
    %Tax Inclusive Accounting%
        where some items will billed including the tax for that items where we can just tick the enable checkbox includes in the basic rate and where we can set it in the sales tax and charges template
    
    %Serial and bundle%
        where every item should have the physical serial no to identify unique and bundle no for every transaction so it is easy to maintain the stock and helpful to stock restore and to generate the purchase reciept and also it automatically creates the bundle no for inward and outward entry and to update the serial and batch no manually we can import using the csv or excel
    
    %Stock Reconciliation%
        where it is used to make the entry and for counting the stock in the warehouse where we can alos maintain the opening stock and remaining stock updates which used to purchase the items that are in the low stock
    
    %Opening Balance Account%
        where after the end of fiscal year the company may have the bank balance and liabilities so to maintain that where we create the account temporary opening ans add the assests in debit and liabilities to the credit to their respective accounts and where atlast the balance must be zero because where to know where from the source comes and where it goes so it is easy to transfer the bank balances and liabilites to be pay during the new fiscal year
    
    %Multi currency Accounting%
        In this where we can set the party currency to their bank accounts currency anad where the transaction can be only make if the company also have the default account in that currency and also where we should always be careful before making any transactions because that only affects in the report ledger so always ensure the currency before transactions or it will create inefficiency in the report generation
    
    %Balance Sheet Accounts%
        In this where we can generate the report and check whether the assests and liabilities are equal by ensuring whether the balance sheet has zero balance during the end and start of the year to transfer the balance details in each and every account to maintain the proper accout details without any conflicts.
    
    %Profit and Loss Accounts%
        In this where it will maintain the income and expenses account and it will give how much profit or loss we attained and generate the report for us and the if we get the profit where that money will be credited to the account of the equity or capital using opening entry using the temporary opening account so the profit and loss reset to zero at every start of the year
    
    %Groups and Ledgers%
        where the groups are just heads where they can have the chidren but cannot make the transactions but ledgers are the child of group where they can record the transactions so in COA we have the four groups assests,income,expenses,liabilities and where each group have their ledgers to make the transactions
    
    %sales Invoice%
        where the sales invoice plays a major role in the erp where it have several options lets see all that

        FLOW
        first we create the sales order to get the confirmation of the customer approval
        second we create the delivery note to update the stock and it is also skipable if it is direct sale
        third we create the sales invoice and where we can use many functionalities here

            *We can use the pos profile for the billing terms for the particular customers or products
            *payment terms -where we can set here or the default for the customers in masters account
            *We can get the invoice discounting using this sales invoice
            *we can create the credit note if there is any return of product
            *we can make the immediate pos payment
            *we can mention the shipping and customer details 
            *we can add the campaign and sources for the marketing purposes
            *Rate adjustment entry if any changes in the previous invoice
            *we can apply the additional discount as grand total or net total
            *we can also update the stock without delivery note
            *we can add the subscrription invoice if it is
            *We can add the loyalty program and reedem points 
            *Where we can add the timesheets like hour billing for employee based on the timesheet
    %Credit Note%
        When a customer need the refund for the product by returning it we use the credit note where it creates the credit note for the customer and where we can update the stock also and in the ledger also we can see that where the payment can be done and also can reduce the amount in the future invoices for that customer
    
    %Payment Recoincillation%
        when the company decides to reduce the amount from the future invoice bill where we will create the recoincillation and it directly make changes in the outstanding field by reducing the outstanding  amount in the invocie which will be balanced in the general ledger also.
    
    %Dunning%
        The dunning is the tool where we can get the interest for the overdue invoices so we can also have the templates and notice for that like first and second notice in first notice we can just give the warning where in next notice we can put the interest rate for the invoice
    
    %General Ledger%
        In the general ledger where all the entries will be recorded with debit and credit and where it is based on the general ledger table and it also record the what type of transaction,voucher and records the bank account that invloves in the transaction and where we can apply the various filters 
    
    %Trial Balance%
        Where in the trial balance report we can see the balance of all account during the time period where opening dr is the amount own by company before the starting date and opening credtors also the how many credits the company owns and the debit and credit are the in between transactions by the company during that time period and closing debtors and credtors are the money that owns and to payable by the company upto that time period
    
    %Balance Sheet%
        where in this we can see the assest balance,liability and the equity balance for the fiscal year and we can see for the previous fiscal years also we can choose any currency to check the balances and also can apply many filters in it.
    
    %Cash Flow%
        In this report we can see the how much cash come in and goes during the fiscal year and we can also ensure the liquidity of the company
    
    %Profit loss statement%
        In this report also where we can see the total income and the total expense and by calculating the difference between it and gives the how much profit or a loss the company gains for that fiscal year
    
    %Consolidated financial report%
        In this report where we can see all the balance sheet,profit and loss statement,cash flow of all the internal or child company of the parent company so where the cutomer can get the overall profil/loss or balance data of the whole enterprise to see over all performance of the company financially
    
    %Deffered Revenue%
        In this report we can see the subscrption split amounts that is sending to the deffered revenue account from the income account and we can see the visual and ledger report how it works and where it helps to maintain the monthly record where the deffered revunue gets debit and in the income account there will be credit so we can generate the yearly report correctly.
    
    %Payment Term Status Report%
        Where it is used to check the payemnt status of the sales invoice with its terms whether it is the advance or full payment so helps to check the paid and unpaid easily
    
    %Purchase order%
        Where by using the material request we can get the items need for the company and can wait for the official approval if there any changes we can change here and after submitting where we can create the purchase receipt 
    
    %Purchase Receipt%
        In this where we can confirm that the order is recieved and where it make the general ledger entry where in the stock in hands it debits the amount and in the stock recieved but not recieved it will make the credit and after the submitting the receipt where we can generate the purchase invoice 
    
    %purchase invoice%
        In this where we can make the bill for the purchase receipt where we also have the options to hold the invoice for specific reasons and can also hold indefinitely or can choose the release date when we submit the purchase invoice in the stock ledger where the  stock received but not billed will get the debit and credit goes to accounts payable(credtors) and atlast when we pay the bill for that invoice then credtors will be debit and where the credit goes to the paid account of the company and the complete flow is

        example invoice amount(1000)

                                        Debit                                   Credit
        purchase receipt --->           1000(stock in hands)                    1000(stock received but not billed)

        purchase invoice --->           1000(stock received but not billed)     1000(Account payable(credtors))

        After Payment    --->           1000(credtors)                          1000(Bank account that paid from company(Sample ERP-canara))
    
    %Provisional Allotment Account%
        where we create the account for the non stock items to create the purchase invoice for the service we used not the stock we should use this provisional allotment account for the transaction and where for that we can create purchase receipt and purchase invoice before that where we should set the default account and enable in the company master settings
    
    %Debit Note%
        In this when a buyer wants to return the product to the supplier they will create the debit note and where it will make the credit form stock recieved but not billed and after the payment where the assests get the money from the credtors and it is the debit note which reverses the purchase flow to get back the money from the supplier
    
    %Bank%
        In this where we can create the bank and give the name to it and where after that we can do the reconcilation with invoice and payment entry by importing data configuration the bank transactions as per the field in the ERPnext.
    
    %Bank Account%
        In this we can create the bank accounts and can choose whether it is a company account or a default account and if the bank supports the plaid integration we can just choose the date to synchronize the transactions and after where we can recoincile them with payment transactions
    
    %Bank Transaction%
        In this where the bank account should properly link with COA account of the company and where this tool is used to maintain the bank transactions and where we can also make entry using the bank statement import and which helps to make a bulk entry
    
    %Bank Reconcillation%
        In this where we can reconcillate the payment entry and bank transaction which are unreconcile and can link them and here we have several filters to apply where we can link through payment,journal entry and sales invoice,purchase invoice and using the exact amount and where we can also filter using the reference date
    
    %Auto Reconcile%
        Where it automatically matches the match against voucher and make the link between the transaction and payment entry but it should be match correctly with the bank account and it is not much efficient because it matches using the code logic not the AI
    
    %Fuzzy matching%
        Where it gives the nearest values not the exact match of the value to find the party for ex let's keep party name john technologies but the payment done from the john pvt limited so we use fuzzy matching to match the payment with bank transaction
    
    %Bank Gurantee%
        When the buyer can't pay the payment where they can give the bank gurantee to the supplier or giver so where if buyer fails to pay the giver can claim the gurantee amount from the bank and it also only valids between the some time period and some times the bank also excepts the buyer to pay margin amount for gurantee and can also put the charges for that gurantee amount
    
    %Invoice Discounting%
        In this where the company gets the loan from the bank by giving the invoices as the gurantee so the bank will pay to the company later the customer pays amount will goes to the bank or even the company can also close the loan and get the money from the customer and it is use by company when they need the money immediately.
    
    %Payment Request%
        In the payment request where we send the notification to the customer using email and where we can choose the print format according to that the mail will send to the customer with payment gateway link if we give or we can send the bank account details through mail so the customer can notify for their payments to the company.
    
    %Payment order%
        If the company has the hireachy to pay for the supplier only after the manager approval they will use payment order by aligning all the payment request or entry to be done by the company and send the payment order to the manager for approval by the accountant
    
    %Payment Entry%
        The payment entry is used to note the payment done by the users in the ERP and where we can match that to bank transaction later and also to the sales invoice and we have several payment modes and can also do the internal transfer and can also do the advance payments and later we reconcillate with the sales or purchase invoice
    
    %Payment ledger%
        Where this ledger is used to track the recivable and payable account transactions and which helps to maintain the general ledger and also the fiscal year account of the company by noting the transactions
    
    %Payment terms%
        Like the sales where we also have the payment terms for the particular supplier or group of supplier and where we can also fix the tax and payment schedule using this payment term tool
    
    %Semi-Auto Payment Reconciliation%
        we just want to enable the account settings in master account and where in the process payment reconcillation doctype we give the filters like party name,payable or recivable account and the company the ERP automatically reconcillate the sales or purchase invoice to the payment entry and which will be done by the background job.

    %Journal Entry%
        Where it is the tool used to make the entry of money movement transaction and where we can choose the accounts and it also have different types of journal entry make difference,debit,credit note etc and where we can also do the payment entry for that journal entry
    
    %Journal Entry Template%
        If we use the one of the the journal entry repeatly then we can give the journal entry template with required account so where we can easily easily amke the journal entry in the future which will saves the time by repeating the same JE.
    
    %Inter company Journal Entry%
        when there is  transfer of money to internal company then we use internal journal entry type to make the transaction between the internal company and where there also we can maintain the accouts to be handled correctly.
    
    %GST%
        GSTR-1 -What I Sold
        GSTR-2A-What I buy
        GSTR-2B-What I can claim
        GSTR-3B-What I should pay as tax
    
    %Deferred Expense%
        It is just opposite to the deferred revenue where in this the company will pay for the future assest or service but it should not immediately affect in the ledger as expense where it still we not recieve it so if we enable the deffered expense where at end of the month where it self creates the journal entry and have a option to save also where it will maintain the ledger by booking expense monthly so there will be no misunderstanding in the accounts calculation
    
    %Process Deferred Accounting%
        It is the list where we can see whether the deferred revenue and deferred expense is entered in GL and journal entry and where by enabling the automatic settings we can make the GL and JE automate or we can make the manual entry to make the entry to the revenue and expense account
    
    %Multi Currency%
        In this where the company can have the many branches and can have customers from other country to so they will maintain the multiple currencies so we should maintain the exchange rates, gain and loss in the journal entry where the multi currency plays a role by maintaing the money value integrity and where we can enable and disable the currencies used by the company
    
    %Exchange Rate Revaluvation%
        Instead of giving the manual rates during the payment where we can set the exchange rate which will automatically update the exchange rate field during the payment and also we can use the api integration to fetch the exhange rates and where we can enable it the account master settings
    
    %cost center%
        where the company can have many branches and diffrent type of platform for that business so to maintan the separate profit and loss where during the purchase and sales invoice so we can maintain the transaction flow separately and can also keep the separate budgeting and also limimt for that cost center so we can plan to take the improvisation steps for that branch according to their performance.
    

    
    

    



