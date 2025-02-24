# 105DBSys_ProjectExample  
105-1 IECS.FCU DBSys Project Example

## Environment Setup
1. Download [XAMPP](https://www.apachefriends.org/zh_tw/index.html) and install it.
2. Run the `XAMPP Control Panel` as an administrator.
3. Click `Start` for both `Apache` and `MySQL`.
4. Click `Admin` for MySQL to open the phpMyAdmin interface.
5. Create the database `testdb`.
6. Create a user:
    - Username: `hj`
    - Hostname: `localhost`
    - Password: `test1234`
7. Grant the user `hj` full privileges on the `testdb` database.
8. Enter the `testdb` database and import `db/init.sql`.

---

## db_example
1. Compile the `.java` files:
    ```bash
    javac -cp ".;.\mysql-connector-java-5.1.40-bin.jar" .\db_example\*.java
    ```
2. Run `MyAppServer` or `MyEchoServer`:
    ```bash
    java -cp ".;.\mysql-connector-java-5.1.40-bin.jar" db_example.MyAppServer
    java db_example.MyEchoServer
    ```
3. Run `MyC1Client` or `MyCCClient`:
    ```bash
    java db_example.MyC1Client
    java db_example.MyCCClient
    ```
4. Enter text in the client. The server will respond:
    - If connected to MyAppServer, it will query the database for that name, and if the name exists, it will print out the description.
    - If connected to MyEchoServer, it will simply echo back the entered text.

---

## jsp_example
1. Run the `XAMPP Control Panel` as an administrator.
2. Click `Explorer`.
3. Place the `jsp_example` folder into the `Tomcat/webapps` directory.
4. Download the `JDBC Driver for MySQL (Connector/J)` from the [Download Connector/J](https://dev.mysql.com/downloads/connector/j/) page.
    - Choose `Platform Independent` and click `Download` to get the compressed file.
5. Extract and place the `mysql-connector-java-8.X.XX.jar` from the compressed file into the `Tomcat/lib` folder.
6. Click `Start` for Tomcat in the XAMPP Control Panel.
7. Open a browser and visit [http://localhost:8080/jsp_example/](http://localhost:8080/jsp_example/).
8. Enter the desired name in the text output field and click `Submit`.
9. If the name exists in the database, its description will be listed on the page.

---

## php_example
1. Run the `XAMPP Control Panel` as an administrator.
2. Click `Explorer`.
3. Place the `php_example` folder into the `htdocs` directory.
4. Open a browser and visit [http://localhost/php_example/](http://localhost/php_example/).
5. Enter the desired name in the text output field and click `Submit`.
6. If the name exists in the database, the name will be displayed on the page.

---

## python_example
1. Open a command prompt and navigate to the `python_example` folder.
2. Install the required packages:
    ```bash
    pip3 install -r requirements.txt
    ```
3. If you encounter an error while installing `mysqlclient` that says `error: Microsoft Visual C++ 14.0 is required.`, manually install the corresponding package file based on your Python version and architecture.
    ```bash
    pip3 install mysqlclient/mysqlclient-1.4.6-cp37-cp37m-win32.whl
    ```
    If there is no matching whl file, you can download one [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/#mysql-python).
4. Run `python_example.py`:
    ```bash
    python3 python_example.py
    ```
5. Open a browser and visit [http://localhost:5000/](http://localhost:5000/).
6. Enter the desired name in the text output field and click `Submit`.
7. If the name exists in the database, the name will be displayed on the page.

---

This translation maintains the original structure and instructions provided in the Chinese version.
