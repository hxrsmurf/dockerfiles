Description:
- These are some of the notes I took when checking out InvoiceNinja. 

Initial Setup:
- apt install git docker-compose net-tools
- git clone https://github.com/invoiceninja/dockerfiles.git
- docker run --rm -it invoiceninja/invoiceninja php artisan key:generate --show
- Update `APP_URL` and `APP_KEY` in `conf\env`
- chmod 755 docker/app/public
- chown -R 1500:1500 docker/app
- docker-compose up -d

Initial Configuration:
- Currency: US Dollar
- Language: English
- Timezone: US/Central
- Date: YYYY-MM-DD
- Military Time: Yes
- First Month: January
- Task Rate: 
- Expense: Yes - Shouuld be Invoiced
- Invoice Design: Elegant

Import Notes:
- Import Client and Vendor first so Expenses can attach to them. You can do this all in one go.

Import Steps:
- Create Groups (there's a feature request for this)
- Import Client 
- Import Vendor
- Import Expenses
- Refresh Data
- Go to Expenses and Create invoices

---

Bugs:
- Invoice - View PDF, X-CORS (SSL not properly supported)
- Invoice Import - Not importing, no errors

Reported Bugs:
- Expense to Invoice, missing line item
- V5 - Importing Expense "Date - Expense" Column Not Accepting Input

Fixed Bugs:
- messagres
