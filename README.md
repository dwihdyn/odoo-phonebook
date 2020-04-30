# How to replicate this project :

1. Setup odoo11 app by following (https://linuxize.com/post/how-to-deploy-odoo-11-on-ubuntu-18-04/#disqus_thread) and npm install issue at (https://stackoverflow.com/questions/60637003/python3-odoo-typeerror-sys-print-is-not-a-function)
2. Git clone this project anywhere you like (eg : `~/Documents/odoo/custom-modules/phonebook`)
3. Copy that path (or just copy the parent address : `~/Documents/odoo/custom-modules` and make any custom modules here) and paste it in `/etc/odoo11.conf` under `addon_path =`
4. Restart odoo server using `sudo systemctl restart odoo11`
5. Go browser -> `localhost:8069` -> Settings tab -> Turn on developer mode -> Apps tab -> Update Apps List -> Search "phonebook" -> Install
6. REMEMBER to pip install any packages inside odoo virtualenv, by going terminal type -> `sudo su - odoo` -> `source odoo11-venv/bin/activate` -> back to normal by `deactivate` and `exit`

## Plans :

1. add phonebook app into this module
2. run metabase locally & integrate psql data to metabase local
3. deploy to google cloud at (https://www.cloudbooklet.com/install-odoo-13-on-ubuntu-18-04-with-nginx-google-cloud/)
4. once deployed, integreate psql db with metabase (or google bigquery & data studio)

## You can create your own module boilerplate by :

- `cd /opt/odoo/custom_addons` # provided custom_addons path has been added in /etc/odoo11.cont
- `./odoo-bin scaffold module-name custom_addons` # module boilerplate
- `sudo systemctl restart odoo11` # restart odoo server
- go to odoo app in localhost:8069 and refresh app list. search the name of the new module name
