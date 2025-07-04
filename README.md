# Minimal Library Management System 📚

## **Project Overview**

Develop a **minimal library management system** using React, Redux Toolkit Query (RTK Query), and TypeScript. The system will allow users to view a list of books, perform CRUD operations, borrow books, and view a simple borrow summary—all without authentication, category filters, or payment integration.

The main goal is to build a functional and clean client-side application that interacts with a RESTful API, demonstrating proper state management, UI design, and core functionality.

---

## **Features**

### **1. Public Routes 🚀**

All pages of this project are accessible without login or authentication. The focus is on essential book and borrowing features only.

---

### **2. Book Management 🛠️**

- **Book List Table:**
    - Show all books in a table format.
    - Columns: Title, Author, Genre, ISBN, Copies, Availability, and Actions.
- **Action Buttons/Icons:**
    - **Edit Book**: Opens a form with existing book data to edit book info. On submit, updates via API and reflects instantly in UI.
        - Business logic:
            - If copies set to 0, the book will mark as unavailable.
    - **Delete Book**: Opens a confirmation dialog before removal.
    - **Borrow Book**: Opens a simple form to borrow a book.
- **Add New Book:**
    - Button to open a form for creating a new book.
    - Fields: Title, Author, Genre, ISBN, Description, Copies, Available (optional, defaults to true).
    - After creation, redirect to book list and update UI immediately.

---

### **3. Borrow Book**

- Open from “Borrow” button in the book list.
- Fields: Quantity (number), Due Date (date).
- Business logic:
    - Quantity cannot exceed available copies.
    - If copies reaches 0, the book is marked unavailable.
- Submit via API and show success message.
- Redirect to borrow summary page.

---

### **4. Borrow Summary**

- Displays a list of books that have been borrowed, along with the **total quantity borrowed** for each book.
- Retrieved from aggregation API.
- Columns: Book Title, ISBN, Total Quantity Borrowed.

---

### **Landing Page Components**

- **Navbar**: Simple navigation bar with links to:
    - All Books
    - Add Book
    - Borrow Summary
- **Book Table/List/Grid**: Display list of books with all core actions.
- **Footer**: Standard footer with site info or credits.

---

## **Page List**

> *(You may choose your preferred UI pattern—pages or modals—for these functionalities.)*
> 
- **/books** – Displays a list of all books with options to view, edit, delete, and borrow.
- **/create-book** – Form interface to add a new book to the system.
- **/books/:id** – Detailed view of a single book’s information.
- **/edit-book/:id** – Interface to update an existing book’s details.
- **/borrow/:bookId** – Form to borrow a selected book.
- **/borrow-summary** – Displays an aggregated summary of all borrowed books.

---

## **UI/UX**

- **Minimalist UI**: clean and featureful UI using Tailwind CSS or plain CSS.
- **User Experience**: Easy navigation between pages, clearly labeled buttons, and simple forms.
- **Responsive**: The layout must be fully responsive and adapt seamlessly to mobile, tablet, and desktop devices.

---

## **Bonus Features**

These are optional and will earn extra points:

| **Feature** | **Bonus** |
| --- | --- |
| Optimistic UI Updates | +2 |
| Toast Notifications | +2 |
| Responsive Layout | +4 |
| Type-Safe Forms | +2 |

---

## **🌐 References for Idea Generation**

You may refer to these minimal systems for visual or architectural ideas:

- https://booklovers.ancorathemes.com/
- https://preview.themeforest.net/item/printpress-book-publishing-wordpress-theme/full_screen_preview/24014694?_ga=2.20131384.1669901765.1750772448-288147160.1750772448&_gac=1.116000500.1750772448.CjwKCAjwmenCBhA4EiwAtVjzmusDrHd09NjQ8OrLFRbSuhVJmTj9RvLZZfk3JNwDPDqwvcCPoMQ0ohoCVXcQAvD_BwE

> ⚠️ Please do not copy from these sources. Use them only for inspiration and UI layout ideas.
> 

---

## **Backend Requirements (Moduler/MVC Pattern):**

- **Database:** Use MongoDB with a schema including:
    - **Books** (with attributes like title, author, **genre, isbn, description, copies, available**)
    - **Borrows** (linked to book, quantity, dueDate etc)
- **Book Management:**
    - Implement CRUD operations for book (create, read, update, delete).
- **Borrow Management:**
    - Execute CRUD operations for borrow (borrow, summery), ensuring copies levels before borrow are placed.
- **Error Handling:**
    - Establish consistent, user-friendly error messa.
- **Additional Changes:**
    - Ensure backend APIs support pagination for book listings and order retrieval.
    - Add authentication middleware to protect private routes (if needed).

`You may use an existing backend that you have developed previously or create a new version by modifying the older one. Make any additional updates if necessary.`

---

## **Technical Requirements (Frontend + API Integration)**

**1. API Integration**

- Consume backend endpoints via **RTK Query** in the frontend.
- All API calls should be typed and organized using Redux Toolkit Query best practices.

**2. State Management**

- **Redux Toolkit with RTK Query**:
    - Used for managing all book and borrow-related API calls and states.
- **Slices (Optional)**: Use extra slices for UI states if necessary (e.g., modals).

**3. Technology Stack**

| **Layer** | **Technology** |
| --- | --- |
| Frontend | React + TypeScript |
| State Management | Redux Toolkit + RTK Query |
| Backend | Node.js + Express.js |
| Database | MongoDB + Mongoose |
| Styling | Tailwind CSS or any basic CSS framework |

---

## **Submission:**

1. **GitHub Repository Link (backend and frontend) with Professional README file** 
2. **Live Deployment Link (backend and frontend)**

---

## **Deadline:**

- **60 Marks:** July 04, 2025 - 11:59 PM
- **50 Marks:** July 05, 2025 - 11:59 PM
- **30 Marks:** After July 05, 2025

## 🚫 **Important Note:**

Plagiarism will not be tolerated. Ensure that the code you submit is your work. Any instances of plagiarism will result in 0 Marks.
