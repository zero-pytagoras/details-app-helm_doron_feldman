# Helm Details App
Application that can store your personal details and list all the written users on html

## Prerequistes
Helm
K3S

To run the app:
helm install <choose a name> ./<folder with Chart.yaml>

To access the endpoints you have two options:
1. "kubectl get endpoints" and copy the addresses to the browser.
2. Use port forwarding.

## Enter details:
Go to the "details-app-helm" app endpoint and type in name and email.

## See the data:
Go to pgadmin endpoint and enter user: admin@example.com, password: admin

After logging in:
click on "add new server":
in tab general -> "name" -> enter whatever you want
in tab connect -> "host name" is "postgres-database", maintance database is "postgres", username and password are both "postgres", click "save".
on the left sidebar click on "servers"->the name you entered->databases->user-details->scehmas->tables. right click on details->query tool-> to see all data you entered do: "SELECT * FROM details"