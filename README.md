# Create-a-SQL-database-using-Sqlectron
(install → connect → create DB → insert data → write queries for table)


## ✅ Step 1: Install **Sqlectron GUI**

> Sqlectron is a desktop SQL client that works with databases like MySQL, PostgreSQL, etc.

### 🖥️ For Windows:

1. Go to: [https://sqlectron.github.io/](https://sqlectron.github.io/)
2. Click on **Download** for your OS (Windows/macOS/Linux).
3. Install like any other software.

---

## ✅ Step 2: Connect to a MySQL database (RDS or Local)

### If you're using **AWS RDS MySQL**:

Make sure:

* Your RDS DB is in **Available** state.
* Port 3306 is open in **Security Groups**.
* DB endpoint, username, and password are ready.

### In Sqlectron:

1. Click on **"New Connection"**.
2. Choose: **MySQL** (or your DB type).
3. Fill:

   * **Name**: `RDS Connection` or anything
   * **Server/Host**: `your-rds-endpoint.rds.amazonaws.com`
   * **Port**: `3306`
   * **User**: `admin`
   * **Password**: `your-password`
   * **Database**: leave blank (for now)
4. ✅ Click **Test Connection**.
5. If successful, click **Save** and then **Connect**.

---

## ✅ Step 3: Create a Database

Once connected:

1. Open the SQL editor inside Sqlectron.
2. Run query:

```sql
CREATE DATABASE my_project_db;
```

3. Refresh → You will now see `my_project_db` in the DB list.

---

## ✅ Step 4: Connect to the new database

1. Go back to "New Connection" → Duplicate or create new one.
2. Now fill:

   * Database: `my_project_db`
3. Save and Connect again — you are now inside the correct DB.

---

## ✅ Step 5: Create Tables (without code)

> 🎯 Example: Suppose you want a **`users`** table.

### You’ll create it using SQL Query:

* Click on **New Query**
* Write a query like:

```sql
CREATE TABLE users (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    email VARCHAR(100),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

* Then click **Run** ✅

> Similarly, create any number of tables — like `products`, `orders`, etc.

---

## ✅ Step 6: Insert Some Sample Data (Optional)

You can insert data by writing queries like:

```sql
INSERT INTO users (name, email) VALUES ('Vishal', 'vishal@example.com');
```

---

## ✅ Step 7: Export This for Repository

To include in your GitHub repo:

1. Save your SQL queries as a `.sql` file (e.g., `init.sql`).
2. Write a simple `README.md` that explains:

   * How to install Sqlectron
   * How to connect
   * How to run queries

---

---

If you want, I can generate the actual `.sql` and `README.md` content too — just ask!
