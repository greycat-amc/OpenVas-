
## OpenVAS Installation > Setup Check Issue
If any issue is detected, the tool provides recommendations on how to resolve it.  
In our case, two issues were identified:

1. A problem related to PostgreSQL where the database was reported as **"does not exist"**. 
<p align="center">
  <img src="../screenshots/gvmchecksetuppostgres.png" width="700">
  <br>
  <em>OpenVAS check setup</em>
</p>

The suggested solution was to recreate or initialize the PostgreSQL database used by GVM.
````markdown
kali@kali:~$ sudo runuser -u postgres -- /usr/share/gvm/create-postgresql-database
````
<p align="center">
  <img src="../screenshots/gvmchecksetuppostgres_solve.png" width="700">
  <br>
  <em>OpenVAS check setup</em>
</p>

2. The absence of a user account required to access the web interface.

<p align="center">
  <img src="../screenshots/gvmchecksetupuser.png" width="700">
  <br>
  <em>OpenVAS check setup</em>
</p>

In this case, it is necessary to create an administrator user in order to log in to the platform.

````markdown
kali@kali:~$ sudo runuser -u _gvm -- gvmd --creat-user=admin --password=openvas
````

<p align="center">
  <img src="../screenshots/gvmchecksetupuser_solved.png" width="700">
  <br>
  <em>OpenVAS check setup</em>
</p>
-----
For other issues, consult the official link: https://greenbone.github.io/docs/latest/22.4/kali/troubleshooting.html

## Lab Setup > Metasploitable2 Installation and Configuration

-----


## Scan Configuration > Feed Owner Issue

