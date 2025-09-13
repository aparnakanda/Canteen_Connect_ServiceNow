# 🍴 Canteen Connect  
Canteen Connect is a **mobile application** designed to streamline the food ordering experience within college campuses. It enables students to explore multiple canteens, browse real-time menus, place and track orders, write reviews, raise issues, and enjoy a seamless ordering experience. Admins and canteen staff can view orders and manage items efficiently.  

---

## 🎯 Project Goals  

- Reduce long queues in college canteens by enabling online food ordering.  
- Provide a transparent and interactive food ordering system.  
- Display real-time food availability.  
- Enable users to view and navigate to different canteens within the college.  
- Help new users easily locate canteen locations with integrated navigation support (e.g., maps or directions).  

---

## 🚀 Features  

- 🔍 View and filter food items from different canteens  
- 📦 Place and track food orders  
- 📊 View order history with date and price  
- ✍️ Post reviews and rate menu items  
- 🛠️ Raise issues directly integrated with **ServiceNow**  
- 🔐 Secure authentication for users and admins  
- 🧑‍💼 Admin dashboard to manage:  
  - Menu items  
  - Order details  
  - User feedback  
- 🗂️ Menu filters based on availability and type (Veg/Non-Veg/Beverages)  
- 💬 Rule-based chatbot for quick assistance  
- 🔁 Dynamic data loading via ServiceNow REST APIs  

---

## 🧑‍💻 Tech Stack  

| Layer          | Tech                          |
| -------------- | ----------------------------- |
| Frontend       | React Native                  |
| Backend        | Node.js, Express.js           |
| Database       | ServiceNow                    |
| Integration    | ServiceNow REST APIs          |
| Authentication | AsyncStorage (React Native)   |  

---

## 🔗 ServiceNow Integration  

Canteen Connect leverages **ServiceNow** as the backend for data, workflows, and automation.  

### 🔹 Tables  
- **Canteen List (`canteen_list`)** – Stores canteen details like name, image, timings, and ratings.  
- **Menu Items (`u_canteen_menu`)** – Stores food items with fields such as item name, price, availability, and type.  
- **Orders (`u_order_details`)** – Captures order details including user, items, price, and order status.  
- **User Profiles (`u_canteen_user`)** – Stores user details like email, username, and photo URL.  
- **Issues (`u_issues`)** – Allows students to raise issues (service-related, billing, delays).  

### 🔹 Flow Designer  
- Automated workflows for order confirmation, order completion, and issue resolution.  
- Example: When an order is placed → Create order record → Trigger notification to canteen staff → Update user on order status.  

### 🔹 Notifications  
- Email/SMS/Push notifications for order status (Placed, Ready, Completed).  
- Alerts to canteen staff when a new order is raised.  
- Escalation notifications for unresolved issues.  

### 🔹 Reports & Dashboards  
- Daily/Weekly reports on total orders, revenue, and top-selling items.  
- Dashboard for admins to monitor order volume and customer feedback.  
- Issue analytics for tracking delays or complaints.  

### 🔹 Roles & Groups  
- **Student/User Role** – Can browse menus, place orders, post reviews, and raise issues.  
- **Canteen Staff Role** – Can view orders assigned to their canteen, update order status.  
- **Admin Role** – Can manage menu items, view all orders, resolve issues, and generate reports.  
- **Groups** – Staff grouped by canteen (e.g., Canteen A Staff, Canteen B Staff).  

### 🔹 ACLs (Access Control Rules)  
- Restrict order details so that students only see their own orders.  
- Ensure canteen staff can only view and manage orders from their assigned canteen.  
- Admin has full access to all tables and records.  

---

## 💡 Why ServiceNow?  

Instead of traditional databases like **MySQL or MongoDB**, Canteen Connect leverages **ServiceNow** because:  

- ⚡ **Low-Code Development** – Tables, forms, and workflows can be created quickly without complex backend coding.  
- 🔔 **Automation Ready** – Built-in Flow Designer and Notifications make it easy to send updates (e.g., order ready alerts).  
- 🔐 **Access Control** – Role-based access (student, staff, admin) is simple to configure.  
- 📊 **Reporting & Dashboards** – Daily/weekly order stats and issue tracking can be viewed directly in ServiceNow.  
- 🌐 **Scalability** – Can easily expand into HR, IT, or facilities modules if the project grows beyond canteen services.  
- 🔗 **Integration Friendly** – REST APIs allow seamless connection with external apps like this mobile app.  

---

## 📱 Key Screens  

- **Home Screen** – Displays all available canteens dynamically.  
- **Menu Page** – Shows items with availability and filters.  
- **Cart & Orders** – Add items, confirm orders, and track them.  
- **Profile** – View user info, past orders, and reviews.  
- **Issue Raising** – Submit issues directly linked to ServiceNow.  
- **Admin Dashboard** – Manage menu items, orders, and user feedback.  

