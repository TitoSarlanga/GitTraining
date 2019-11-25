[Prerequisites](#prerequisites)
[Obtaining source code](#obtaining-source-code)
[Start MongoDB](#start-mongodb)
[Create seed for Localhost instance DB](#create-seed-for-localhost-instance-db)
[Connect to Localhost instance DB](#connect-to-localhost-instance-db)
[First build - Hello Logger](#first-build-hello-logger)
[Run the application](#run-the-application)
[Testing](#testing)
[Admin login (configuration)](#admin-login-connfiguration)

Sport Logger (SL)
===================

This project was generated with the Angular Full-Stack Generator version 3.6.1.


Prerequisites
-------------
 - [VS Code][1] → Run installer with default options
 - [Git][2] → Run installer with default options
 - [NodeJs][3] → Run installer with default options
 - [MongoDB][4] → v 4.2.1. Run installer with default options
 - [NoSQLBooster][5] → Run installer with default options
 - Grunt → Install with NPM
 - Express → Install with NPM


Obtaining source code
-------------
 - Open git bash and go to the path where you like to clone Logger project
 - Go to → 
 - Select Clone, and click in the icon  into **Clone with HTTPS**. This will copy the URL to the clipboard.
 - Into git bash run: git clone [press SHIFT + Insert to paste the URL]
	 - i.e → `git clone 
 - Get into the src folder → `cd src`
 - Open the project in VS Code → `code .`


Start MongoDB
-------------
 - Go to the folder as MongoDB was installed and execute mongod.exe. Usually, the path may be this: `C:\Program Files\MongoDB\Server\3.2\bin>mongod`


Create seed for Localhost instance DB
-------------
 - Open NoSQLBooster for MongoDB
 - Go to File/Connect (or press Ctrl + N)
 - Press ‘Create’ Button
 - Add this configuration
	 - Server: 
	 - Port: 
	 - Name: 
 - Press **Test Connection** button and **Save & Connect** button
 - We need to copy logger-dev database, for this, right click over this DB and select copy option
 - Now, add a new connection called ‘localhost’
	 - Server: localhost
	 - Port: 27017
	 - Name: localhost
 - Press **Test Connection** button and **Save & Connect** button
 - Paste the database in this connection. Right click over the DB instante and select **Paste Database**


Connect to Localhost instance DB
-------------
 - [Start MongoDB](#start-mongodb)
 - Open NoSQLBooster for MongoDB
 - Click in ‘Connect’ and  select localhost instance


First build - Hello Logger
-------------
 - [Start MongoDB](#start-mongodb)
 - [Connect to Localhost instance DB](#connect-to-localhost-instance-db)
 - Open a terminal window in VS Code (Press Ctrl + ñ) (inside /logger/scr folder)
 - Type in this order:
	 - `npm install -g bower`
	 - `bower install`
	 - `npm install -g grunt `
	 - `npm install -g grunt-cli`
	 - `npm install -g express`
	 - `npm install`
	 - `grunt serve`


Run the application
-------------
 - Open a terminal window in VS Code (Press Ctrl + ñ)
 - Run `grunt serve`


Testing
-------------
 - Open a terminal windows in VS Code (Press Ctrl + ñ)
 - Run `npm test`. This will run the unit test with karma


Admin login
-------------
 - [Run the application](#run-the-application)
 - For local login, press ALT + L
 - user: admin | pass: admin

  [1]: https://code.visualstudio.com/download
  [2]: https://git-scm.com/downloads
  [3]: https://nodejs.org/es/download/
  [4]: https://drive.google.com/file/d/1C2aIMl7knB3JcDe8MZCFkHSmpmULLI3_/view?usp=sharing
  [5]: https://nosqlbooster.com/downloads

