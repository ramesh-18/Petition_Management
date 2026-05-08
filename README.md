# Petit - Petition Management System

Petit is a comprehensive console-based Java application designed to streamline the process of filing, managing, and tracking public petitions. It provides a modular environment for Users, Administrators, and Department Officers to interact effectively.

## 🚀 Features

### **👤 User Module**
- **Registration & Login**: Secure account creation with field validation (Email, Password, Phone).
- **Petition Filing**: Create petitions with titles, descriptions, categories (Department), and priority levels.
- **Tracking**: View personal petition history and current statuses.
- **Profile Management**: View and update personal profile details.

### **🛡️ Admin Module**
- **Officer Management**: Create and delete departmental officers.
- **Global Oversight**: Monitor all petitions in the system across all users and departments.
- **Detailed Analytics**: View complete metadata for any petition.

### **👮 Officer Module**
- **Departmental Filtering**: Officers see only the petitions relevant to their assigned department (e.g., Water, Road, Electricity).
- **Status Control**: Update petition progress from `OPEN` to `IN_PROGRESS`, `RESOLVED`, or `CLOSED`.
- **Audit Trail**: Automatic timestamping for every status update.

---

## 🏗️ Technical Architecture

- **Language**: Java 17+
- **Pattern**: 
    - **Model-View**: Separation of presentation logic and business validation.
    - **Singleton**: Centralized data state management via `PetitDB`.
- **Encapsulation**: Models are package-private to ensure modularity.
- **Data Integrity**: Centralized CRUD operations within the singleton repository.

---

## 📂 Project Structure

```text
src/com/cheeks/petit/
├── data/
│   ├── dto/          # Data Transfer Objects (User, Admin, Petition, etc.)
│   ├── enums/        # System Enums (Department, Status, Priority)
│   └── repository/   # Singleton PetitDB and Data Initializer
└── features/         # Modular feature sets (Admin, User, Officer, Petition)
    ├── admin/
    ├── officer/
    ├── user/
    └── petition/
```

---

## 🛠️ Getting Started

### **Prerequisites**
- Java Development Kit (JDK) 8 or higher.

### **Running the Application**
1. Navigate to the project root directory.
2. Compile the source files:
   ```bash
   javac -d out src/Main.java src/com/cheeks/petit/**/*.java
   ```
3. Run the application:
   ```bash
   java -cp out Main
   ```

### **Default Credentials**
- **Admin Email**: `admin@gmail.com`
- **Admin Password**: `admin123`

---

## 📝 License
This project was developed as part of a CAD (Customer Application Development) training.
