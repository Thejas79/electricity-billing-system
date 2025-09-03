# electricity-billing-system
This is a Java-based Electricity Billing System with a graphical user interface (GUI) using Java Swing and MySQL as the database. It allows employees or admins to manage electricity bills, customers, meter data, and generate invoices.

📦 Project Structure
Once unzipped, the folder typically contains:

graphql
Copy
Edit
Electricity-Billing-System-master/
├── src/                          # Java source files
│   ├── login.java
│   ├── dashboard.java
│   ├── customer.java
│   ├── bill.java
│   └── ...
├── icons/                        # Icon images used in the GUI
├── sql/                          # Database SQL file (e.g., schema.sql)
├── README.md                     # Instructions (you’re reading it)
🛠 Requirements
Java JDK 8 or higher

MySQL Server (e.g., via XAMPP, WAMP, or standalone)

Any IDE (IntelliJ IDEA, Eclipse, NetBeans)

MySQL JDBC Driver (Connector/J)

🚀 How to Run This Project
1️⃣ Step 1: Setup Database
Open phpMyAdmin or MySQL CLI.

Create a new database, e.g., electricity.

Import the SQL file:

Navigate to the sql/ folder.

Run schema.sql (or similar file) to create tables.

2️⃣ Step 2: Configure the Database Connection
Open the Java file handling the DB connection (e.g., conn.java or DBConnection.java).

Set the appropriate values:

java
Copy
Edit
Connection c;
Statement s;

public conn() {
    try {
        c = DriverManager.getConnection("jdbc:mysql://localhost:3306/electricity", "root", "");
        s = c.createStatement();
    } catch (Exception e) {
        e.printStackTrace();
    }
}
Make sure the:

Host: localhost

Port: 3306

Username: root

Password: "" (empty if no password set)

3️⃣ Step 3: Compile and Run
Option A: Using IDE
Open the project in your IDE.

Mark src/ as the source folder.

Run the main class, typically login.java.

Option B: Using Terminal
bash
Copy
Edit
cd Electricity-Billing-System-master/src
javac *.java
java login
🔑 Default Login (if hardcoded)
Check login.java for hardcoded login credentials like:

java
Copy
Edit
if (username.equals("admin") && password.equals("admin123"))
Or see if users are stored in the database.

✨ Features
Admin/Employee Login

Add Customer

Add/View Meter Information

Generate Monthly Bills

View Bill History

GUI using Java Swing

Database integration using MySQL

