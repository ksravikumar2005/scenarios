To access the MongoDB Ops Manager URL:

Render port 8080: http://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/

Render port 80: http://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com/

Display page allowing user to select port:
http://[[HOST_SUBDOMAIN]]-[[KATACODA_HOST]].environments.katacoda.com/


Display Dashboard Tabs


"environment": {
  "showdashboard": true,
  "dashboards": [{"name": "Display 80", "port": 80}, {"name": "Display 8080", "port": 8080}],
}

