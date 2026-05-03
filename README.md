# 🛒 SHOP.JAVA — Full-Stack E-Commerce Backend

A robust, modular Java backend for an e-commerce platform. This project manages the entire retail lifecycle — from user authentication and inventory control to atomic checkout transactions and automated email invoicing.

---

## 🌟 Core Features

### 🔐 User & Security
- **Role-Based Access**  
  Distinguishes between `admin` and `customer` roles to control access to sensitive operations.

- **Authentication**  
  Secure login system that returns user data and roles via JSON for frontend integration.

- **Address Management**  
  Users can manage a digital address book, including setting default shipping locations.

---

### 📦 Inventory & Admin Tools
- **Product Management**  
  Admins can add, update stock, or delete products through a dedicated `AdminServlet`.

- **Live Catalog**  
  Dynamically fetches products with available stock for customer browsing.

---

### 🛒 Checkout & Processing
- **Atomic Transactions**  
  Ensures data integrity by processing orders, logging items, and reducing stock as a single database transaction.

- **Automated Invoicing**
  - Generates local `.txt` invoice files for every order.
  - Sends professional HTML receipts to the admin via SMTP using Jakarta Mail.

- **Tax Logic**  
  Automatically calculates an **18% GST** on the order subtotal.

---

## 🛠️ Technology Stack

- **Language**: Java  
- **Server Logic**: Java Servlets (Jakarta EE)  
- **Database**: MySQL with JDBC  
- **Data Format**: JSON (Google Gson)  
- **Email Service**: Jakarta Mail  

---

## 📋 Setup Instructions

### 1️⃣ Database Setup
Ensure you have a MySQL server running. Create the following tables:

- `users`
- `products`
- `addresses`
- `orders`
- `order_items`

---

### 2️⃣ Environment Variables

For the **Email Service** to function, set these variables:

```bash
MAIL_USERNAME=your_email@gmail.com
MAIL_PASSWORD=your_app_password
