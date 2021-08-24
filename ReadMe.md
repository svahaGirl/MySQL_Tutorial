## Tutorial for using MySQL Workbench  Mac Book Pro
# Lesson 1
# https://dev.mysql.com/downloads/workbench/
# Step 1:
![image](https://user-images.githubusercontent.com/56694905/130517198-4dfc8f52-d3d9-4023-a924-1716d2a4bd6f.png)
# Step 2: click download, and you can choose download without register.
![image](https://user-images.githubusercontent.com/56694905/130517249-6bc0b03f-28ec-44da-b27d-5e0e7573cdf7.png)
# Step 3: Initialize a connection after installation
# Windows:

# Mac book Pro: use Homebrew install mysql first otherwise you will fail a connection with localhost
 # If you already installed homebrew in Mac, use this command:
 #  brew install mysql
 #  brew services start mysql
 #  mysqladmin -u root password 'yourpassword'
# Now Setup New Connection, give a name for the connection, then use default Hostname and Port, add a password, Test Connection, if successful, click ok.
# After you successfully created connection, click the connection, you can see the GUI, then click add a new_Schema to create a database.

## Common Errors for creating table using Entity
# -Error:java.lang.IllegalArgumentException: Not a managed type: class com.svaha.common.entity.Role
# --Fix:ADD: @EntityScan({"com.svaha.common.entity", "com.svaha.admin.user"})
# --- it means: Add your package that you are using To your SpringApplication main class before you run Junit test to create table.
# -Error: Table empty, not writing data to it.
# --Fix: Add @Rollback(false)     
# --- To your Test class, also config "spring.jpa.hibernate.ddl-auto=update" in your application.properties for data, make sure you are using jpa and sql dependencies as well.
