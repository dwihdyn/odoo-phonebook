# How to replicate this project :

1. Setup odoo11 app by following (https://linuxize.com/post/how-to-deploy-odoo-11-on-ubuntu-18-04/#disqus_thread) and npm install issue at (https://stackoverflow.com/questions/60637003/python3-odoo-typeerror-sys-print-is-not-a-function)
2. You can create your own module boilerplate by : - `cd /opt/odoo/custom_addons` # provided custom_addons path has been added in /etc/odoo11.cont - `./odoo-bin scaffold module-name custom_addons` # module boilerplate - `sudo systemctl restart odoo11` # restart odoo server - go to odoo app in localhost:8069 and refresh app list. search the name of the new module name

## Plans :

1. add phonebook app into this module
2. run metabase locally & integrate psql data to metabase local
3. deploy to google cloud at (https://www.cloudbooklet.com/install-odoo-13-on-ubuntu-18-04-with-nginx-google-cloud/)
4. once deployed, integreate psql db with metabase (or google bigquery & data studio)
   ~
   `
