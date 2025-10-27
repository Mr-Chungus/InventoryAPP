#  Inventory App

**Author:** Greg Gordon  
**Language:** Java (Android Studio)  
**Target SDK:** Android 14 (API 34)

---

##  Overview
The **Inventory App** is a lightweight Android application for tracking and managing items locally on a device.  
It allows users to **log in**, **add**, **edit**, or **delete inventory items**, and receive **SMS alerts** when stock levels run low.

The app was designed to be **simple**, **fast**, and **fully offline**, so small shops, storerooms, or individuals can manage inventory without needing an internet connection or external servers.

---

##  Goals and User Needs
The main goal of the project was to create a **user-centered app** that focuses on **ease of use** and **reliability**.

It was built to help users:
- Keep track of inventory items locally  
- Log in securely with username and password  
- Receive alerts when items are low in stock  
- Quickly add, move, or remove inventory entries  

The layout follows **Android Material Design** for a clean and consistent experience that doesn’t require training to use.

---

## 📱 Screens and Features

###  Login / Create Account
- Allows users to sign in or register  
- Validates credentials and prevents duplicate usernames  
- Includes a default `admin/admin` user for first-time access  

###  Inventory List
- Displays all items in a grid layout using a `RecyclerView`  
- Floating action button for adding new items  
- Tap on an item to view or edit details  

###  Item Details
- Displays all item data including name, location, quantity, and notes  
- Allows users to modify and save changes  

###  SMS Permissions
- Requests SMS permission only when needed  
- Sends low-stock alerts if permission is granted  
- Continues functioning even if SMS permission is denied  

###  Additional Options
- Change password feature  
- Logout option to return to the login screen  

---

##  Development Approach
The app was developed using **modular classes** (`DbHelper`, `ItemRepo`, `UserRepo`, etc.) to keep the code organized.  
I tested functionality frequently using the **Android Emulator**, focusing on verifying login behavior, database persistence, and UI alignment.

Each feature was built and tested in small chunks to avoid breaking existing components. This method made debugging easier and helped ensure the app worked as intended.

---

##  Testing
Testing included:
- **Functional testing** on emulator devices (Android 12–14)  
- **Database testing** to verify CRUD operations persisted after closing the app  
- **Permission testing** for SMS functionality  
- **UI testing** for alignment and layout consistency across screen sizes  

Testing revealed issues like overlapping layouts and incorrect database queries, which were fixed iteratively.

---

##  Innovation and Problem-Solving
One key challenge was ensuring that the app remained fully functional even without SMS permissions.  
To solve this, I created conditional logic that bypasses the SMS alert system while still maintaining core inventory functionality.  

Another challenge was implementing user authentication with a default admin account — this was achieved through an idempotent database seeding approach.

---

##  Successes
I was particularly successful in implementing:
- A **secure and persistent login system**
- A **responsive RecyclerView-based inventory UI**
- **SQLite database integration** for offline data storage
- A **clean user flow** that keeps simplicity and usability as top priorities  

---

##  Future Improvements
- Add barcode scanning via camera  
- Implement cloud synchronization for multi-device use  
- Add export/import features for backup  
- Introduce light/dark theme support  

---

##  License
This project is open source and free to use for educational or personal projects.

---

> *“Built with care to make inventory tracking simple, reliable, and fully offline.”*
