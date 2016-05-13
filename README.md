# Java-Database
###Java Database (Add, Delete, Update and Search from Access Database).

This tutorial help you to understand about how to connect your Java application with the Access database and  Add, Delete, Update and 
Search record from your Database.

>Database Name: - db1.accdb

To run this program you need to place this databse in to your **D:/** Drive of your Computer.if there is no any drivers except **C:/** the 
you need to change the following line of the code.
```
Class.forName("sun.jdbc.odbc.JdbcOdbcDriver");
    String url = "jdbc:odbc:Driver={Microsoft Access Driver " + "(*.mdb, *.accdb)};DBQ=D:\\db1.accdb";
        
```
for the whole program Try following function to connect with your datyabase.
```
try {
    Class.forName("sun.jdbc.odbc.JdbcOdbcDriver");
    String url = "jdbc:odbc:Driver={Microsoft Access Driver " +"(*.mdb, *.accdb)};DBQ=D:\\db1.accdb";
    Connection con = DriverManager.getConnection(url);

    label1.setText("Status: Database connection passed!");
    con.close();
    
} catch (SQLException e) {
    label1.setText("Status: SQL Exception: "+ e.toString());
    
} catch (ClassNotFoundException cc) {
    label1.setText("Status: Class Not Found Exception: "+cc.toString());}
    
```

Application code & developed by : [Kasun Herath](http://engtute.com/About.html).



