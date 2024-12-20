🌟 How to Connect MySQL with Power BI: A Simple Guide 🌟

Are you looking to connect MySQL with Power BI to create powerful dashboards and analyze your data? This guide will walk you through the process step by step. 🚀

🛠️ Step 1: Install MySQL ODBC Connector
Go to the MySQL website and download the ODBC connector that matches your system (32-bit or 64-bit).
Follow the installation wizard to install it on your computer.
https://dev.mysql.com/downloads/file/?id=412152

🌐 Step 2: Connect MySQL with Power BI
⚠ Note: Power BI sometimes defaults to Windows credentials, which may not work with MySQL. Here’s how you can connect successfully:
Open Power BI Desktop.
Go to Home Tab → Get Data → MySQL Database → Connect.
In the connection dialog:
Enter localhost (for a local server) or the name of your MySQL server in the Server field.

Enter the Database Name ( I have selected World as my database)
Click OK to connect.
![mysql snapshot](https://github.com/user-attachments/assets/111af539-bc61-4f36-8328-113e75917cfd)


💡 If you encounter errors, double-check your MySQL server name, username, password, and port settings.

💡 You may see the following error in your query editor window:

"DataSource.Error: Object reference not set to an instance of an object."

You are most likely getting a "user not authorized error". To resolve this issue, go to File | Options and Settings | Data source settings and edit your data source and set the credentials to "Database credentials", not Windows credentials.

https://learn.microsoft.com/en-us/archive/technet-wiki/32004.power-bi-tips-for-working-with-mysql

📥 Step 3: Load and Explore Your Data
Once connected:
You’ll see a list of tables from your database.
Select the tables you need or write a custom SQL query for specific data.
Click Load to bring the data into Power BI or Transform Data to prepare it before loading.

you can also try Custom Query like below: 
SELECT Code, GNP FROM world.country
order by GNP desc

![mysql snapshot](https://github.com/user-attachments/assets/7eefcab6-6da2-41eb-9b08-63c3d1035404)


![ETL](https://github.com/user-attachments/assets/2ee1eb0a-16f7-4cbc-a0a7-72a0ef99e6ad)

📊 Step 4: Start Building Dashboards
✨ You’re all set! Use Power BI to create stunning dashboards, visualize trends, and extract actionable insights from your MySQL data.

![pbi](https://github.com/user-attachments/assets/3ec1c791-3e48-4729-96aa-34f983852ef2)

📌 Tips
Ensure that your MySQL server is running and accessible.
Always validate your credentials and connection details.
For advanced users, custom SQL queries can help in fetching optimized datasets for analysis.
