#### Branch Build Status ####
 
- develop - [![build status](https://git.around.com.ar/around/internal/badges/develop/build.svg)](https://git.around.com.ar/around/internal/commits/develop)
- master - [![build status](https://git.around.com.ar/around/internal/badges/master/build.svg)](https://git.around.com.ar/around/internal/commits/master)

Tracker (internal)
===================

The purpose of this document is to define the necessary steps for clone and build the application

----------

Index
-------------

 - [Prerequisites](#prerequisites)
 - [Get the source code](#Get-the-source-code)
 - [Develop instance vs Local instance](#develop-instance-vs-Local-instance)
 - [Build and run the app](#build-and-run-the-app)

----------


Prerequisites
-------------

 - [Visual Studio 2017 or higher][1]
 - Net Framework 4.5.2
 - [SQL Server 2017][2]
 - [GIT][3] or [SourceTree][4] (optional)
 - [Flyway][5]

----------


Get the source code
-------------

 1. Go to https://git.around.com.ar/around/internal and copy the URL
 2. In GIT Bash --> 
	 2.1. Clone the repo: `git clone [url]`
	 2.2. Run `git submodule update --init --recursive` for download the Atlassian.Jira submodule
	 2.3. Change to develop branch: `git checkout develop`
 
	> For more information about git submodules:  http://openmetric.org/til/programming/git-pull-with-submodule/
 ----------


Develop instance vs Local instance
-------------
When you connect to a local instance, your changes will remain on your machine and will not affect the development database.
But, anyway, keep in mind that any change in data structure or update in DB implies a new restoration of the updated DB.

 **If you want to connect to a develop instance** modify the connection string with this line
 
```
 <add name="Entities" connectionString="metadata=res://*/Entities.csdl|res://*/Entities.ssdl|res://*/Entities.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=192.168.10.241;initial catalog=dev-AccountDB;uid=intdev;password=v1kSEvB7fl5r;MultipleActiveResultSets=True&quot;" providerName="System.Data.EntityClient" />
```
**If you want to connect to a local instance**

 1. Download here the DB backup
 2. Copy the file in this path: `C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\Backup`
 3. Open Microsoft SQL Mannagement Studio and connect to a local server
 4. Right click in the folder "Databases" inside the local server
 5. Choose the option "Restore database..."
 6. In the source section, choose "Device" and click the three dots "..."
 7. In the modal windows "Select backup devices" click in the "Add" button
 8. Select the database who previously we copy
 9. Press OK --> OK --> OK
 10. The DB now should be appear in the local server 
 ----------



Build and run the app
-------------
Simply build and execute, for logging use your google account credentials.

  [1]: https://visualstudio.microsoft.com/downloads/
  [2]: https://www.microsoft.com/es-es/sql-server/sql-server-downloads
  [3]: https://git-scm.com/
  [4]: https://www.sourcetreeapp.com/
  [5]: https://flywaydb.org/download/
