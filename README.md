### 1. Back Up Your Home Assistant

---

### 2. Navigate to Settings → Add-ons  

2.1 Install **MariaDB**.  

2.1.1 Once the installation is complete, open **MariaDB**.  
2.1.2 Go to the **Configuration** tab.  
2.1.3 Under **Databases**, enter `bookstack` and add it.  
2.1.4 Under **Logins**, change the username and password to your preferred values.  
2.1.5 Add the following code under **Rights**:  
```yaml
- database: bookstack
  username: your_username
  password: your_password
  allow_external_connections: true
```
2.1.6 Save the changes.  
2.1.7 Start **MariaDB**.

---

2.2 Install **PhpMyAdmin**.  

---

2.3 Install **Bookstack**.  

2.3.1 Go to the **Configuration** tab.  
2.3.2 Update the configuration as follows:
```yaml
remote_mysql_host: core-mariadb
remote_mysql_database: bookstack
remote_mysql_username: your_username
remote_mysql_password: your_password
remote_mysql_port: 3306
certfile*: fullchain.pem
keyfile*: privkey.pem
```
2.3.3 Save the changes.  
2.3.4 Start **Bookstack**.

---

### 3. Web Interface  
3.1 Open Bookstack in your browser by visiting your Home Assistant IP and port 2665 (e.g., `192.168.X.X:2665`).  
3.2 Log in with the following credentials:  
- **Email**: `admin@admin.com`  
- **Password**: `password`  

---

Enjoy using **Bookstack**! 😊

