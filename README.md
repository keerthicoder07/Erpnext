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

    * First we should download the template by choosiing the doctype with the needed fields then we can easily do the changes or enter the data
    *second we should not give the duplicate data then it shows duplicate data error and we should not change the field name after we create the data import document then also it shows error 
    *third where we can import the files from local,library or from the google sheets and where if it is google sheets we dont want to import the always the file from local and where if we use the google sheets we should keep the public access for that file and we should only copy and give the url tab link
    *If any error it will throw the error in each row if not it will add that data 
    *During the update of record we cannot change the id of any record
    * we should not also give large data like 50000 so we split and add the data