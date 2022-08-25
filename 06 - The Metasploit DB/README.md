# The Metasploit Database

- You will first need to start the ***PostgreSQL database***, which Metasploit will use with the following command: 
```
systemctl start postgresql
```

- Then you will need to initialize the Metasploit Database using the `msfdb init` command. 

  ![image](https://user-images.githubusercontent.com/63872951/186691655-aba63f1a-44bc-4da1-8065-fa18ace20bfc.png)

- You can now launch `msfconsole` and check the database status using the `db_status` command.
  
  ![image](https://user-images.githubusercontent.com/63872951/186692383-a37ba376-03a3-4375-ab02-284c3a8e868b.png)

- The database feature will allow you to create workspaces to isolate different projects. When first launched, you should be in the default workspace. You can list available workspaces using the `workspace` command. 

  ![image](https://user-images.githubusercontent.com/63872951/186692629-f6f7455f-ee43-4ed4-9165-1e126782db65.png)

- You can ***add*** a workspace using the `-a` parameter or ***delete*** a workspace using the `-d` parameter, respectively. The screenshot below shows that a new workspace named `tryhackme` was created.

  ![image](https://user-images.githubusercontent.com/63872951/186692924-978501eb-f52c-4fdc-834e-8279a88a7db3.png)

- You will also notice that the new database name is printed in ***red***, starting with a `*` symbol.

- You can use the `workspace` command to navigate between workspaces simply by typing workspace followed by the desired workspace name. 
  
  ![image](https://user-images.githubusercontent.com/63872951/186693345-945fd84f-7501-4118-8bde-00bfa71249a8.png)

- You can use the `workspace -h` command to list available options for the `workspace` command.  

  ![image](https://user-images.githubusercontent.com/63872951/186693558-ee2f910d-a2ef-40dd-80ba-57f74d33a694.png)

- Different from regular Metasploit usage, once Metasploit is launched with a database, the `help` command, you will show the Database Backend Commands menu.

  ![image](https://user-images.githubusercontent.com/63872951/186693868-931e57c0-db23-4f96-83fc-e0bfc8b6e645.png)

- If you run a ***Nmap scan*** using the `db_nmap` shown below, all results will be saved to the database. 

  ![image](https://user-images.githubusercontent.com/63872951/186694092-8675e8a6-e45a-4131-ab43-88d350c102bc.png)

- You can now reach information relevant to ***hosts*** and ***services*** running on target systems with the `hosts` and `services` commands, respectively. 

  ![image](https://user-images.githubusercontent.com/63872951/186694402-ad8635ef-afc0-4016-808d-12ce16a01d65.png)

- The `hosts -h` and `services -h` commands can help you become more familiar with available options. 

- Once the host information is ***stored*** in the database, you can use the `hosts -R` command to ***add*** this value to the `RHOSTS` parameter. 

#

### [Example Workflow](https://github.com/ShubhamJagtap2000/Metasploit/tree/main/06%20-%20The%20Metasploit%20DB/Example%20Workflow)



