### **1. Log into PostgreSQL**

You need administrative access to PostgreSQL to create a new user.

#### Log in as the `postgres` user:

```bash
sudo -u postgres psql
```

- If PostgreSQL is configured for local authentication, you may need to use a password.

---

### **2. Create a New User**

Once inside the `psql` shell, use the `CREATE USER` command.

#### Basic Example:

```sql
CREATE USER new_user WITH PASSWORD 'secure_password';
```

- Replace `new_user` with the desired username.
- Replace `secure_password` with a strong password.

---

### **3. Grant Privileges (Optional)**

You can grant specific privileges to the new user.

#### Grant All Privileges on a Database:

```sql
GRANT ALL PRIVILEGES ON DATABASE database_name TO new_user;
```

- Replace `database_name` with the name of your database.

#### Create a Superuser (Optional):

If the user needs full access to the database system:

```sql
ALTER USER new_user WITH SUPERUSER;
```

---

### **4. Exit the psql Shell**

Type:

```sql
\q
```

---

### **5. Test the New User**

You can test the new user by logging in with it:

```bash
psql -U new_user -d database_name -W
```

- `-U`: Specifies the username.
- `-d`: Specifies the database to connect to.
- `-W`: Prompts for the password.
