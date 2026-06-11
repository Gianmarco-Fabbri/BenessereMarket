# Benessere Market - Web Technologies Project

Benessere Market is an e-commerce web application specializing in wellness, cosmetics, perfumes, and green living products. It was developed as a team project for the Web Technologies course (Tecnologie Web) at the University of Bologna (Unibo), Academic Year 2024/2025.

---

## Authors

* **Gianmarco Fabbri** - gianmarco.fabbri3@studio.unibo.it
* **Kevin Shimaj** - kevin.shimaj@studio.unibo.it
* **Lisa Vandi** - lisa.vandi2@studio.unibo.it

---

## Key Features

The application is divided into two distinct portals to accommodate both buyers and sellers:

### Customer Portal
* **Catalog Browsing**: Discover wellness products categorized under Health (Salute), Beauty (Bellezza), Perfumes (Profumi), and Green Living (Casa & Green).
* **Price Filtering**: Live range filters allow users to dynamically filter product catalogs by minimum and maximum prices.
* **Shopping Cart**: Session-based cart allowing users to add/remove products, adjust quantities, and view live subtotal calculations.
* **Loyalty Points Program**: A reward system where customers earn 1 point for every 1 EUR spent. Points can be accumulated and redeemed for discounts during checkout.
* **Order Tracking**: Detailed purchase history showing order stages (e.g., ordered, shipped, delivered) and delivery estimates.
* **Notification System**: Customers receive instant alerts regarding order updates and feedback logs.
* **Profile Management**: Section to edit personal details, change account password, delete the account, view earned points, and track submitted reviews.

### Vendor Portal
* **Inventory Management**: Full CRUD dashboard to add new items, update product details (images, descriptions, category, price), and delete stock.
* **Promotion Management**: Tools to apply discounts, manage active offers, and run marketing campaigns on specific products.
* **Order Fulfillment**: Overview of all client orders, allowing vendors to update delivery states and process shipments.
* **Review Moderation**: Access to view and monitor customer ratings and reviews left on the vendor's products.

---

## Architecture and Technology Stack

The application employs a structured architecture dividing business logic and template presentation.

### Technologies Used
* **Frontend**: HTML5, Vanilla CSS3, Bootstrap 5 (for responsive layouts), JavaScript (ES6+, utilizing Fetch API for asynchronous page updates).
* **Backend**: PHP 8.x (object-oriented database connections and controller routing).
* **Database**: MySQL (relational database storage with custom triggers for data integrity).

### Directory Structure
* `/` (Root): Main PHP controller files acting as entry points (e.g., `index.php`, `accedi.php`, `carrello.php`, `profilo.php`).
* `ajax/`: Backend asynchronous API scripts serving JSON responses grouped by category, login, profile, and cart actions.
* `css/`: Stylesheets containing the custom layout definitions (`style.css`) and page-specific styles.
* `db/`: SQL creation and seeding scripts (`creazione_db.sql`, `popolamento_db.sql`) alongside the central `database.php` controller helper.
* `img/`: Static and uploaded image assets representing product photos, icons, and logo graphics.
* `js/`: Client-side JavaScript logic managing DOM interactions, price filters, and AJAX requests.
* `mockup/`: UX/UI design wireframes and visual mockups of key user journeys.
* `template/`: Presentation files (e.g., `base.php`, `base_venditore.php`) separated from business logic to render dynamic headers, footers, and main blocks.
* `utils/`: Shared utilities and function scripts.

---

## Database Configuration

The system connects to a MySQL schema named `benessereDB`. 

### Setup Instructions
1. Open your MySQL server client (e.g., phpMyAdmin or command-line terminal).
2. Import the database schema from the file `db/creazione_db.sql`.
3. Seed the tables with initial demo datasets using the file `db/popolamento_db.sql`.
4. Ensure your server configuration matches the credentials defined in `bootstrap.php`:
   * **Host**: localhost
   * **Port**: 3306
   * **User**: root
   * **Password**: (empty by default)
   * **Database Name**: benessereDB

---

## Installation and Local Deployment

1. **Clone the Repository**:
   Clone this repository into your local web server's public directory (e.g., `htdocs` for XAMPP or `html` for Apache).
   ```bash
   git clone https://github.com/Gianmarco-Fabbri/ProgettoWeb.git
   ```
2. **Start Web Server & Database**:
   Launch Apache and MySQL via your local development stack (e.g., XAMPP, MAMP, or Docker).
3. **Import SQL**:
   Import database files using the steps mentioned in the *Database Configuration* section above.
4. **Access the Application**:
   Navigate to the entry path in your browser:
   `http://localhost/ProgettoWeb/index.php`

---

## Design and Documentation

* **Visual Mockups**: Refer to the `mockup/` folder for graphical representations of the user interface flow.
* **Written Project Report**: The repository includes the comprehensive project report `Relazione_Web.pdf` (written in Italian), which documents design guidelines, architectural blueprints, and engineering decisions.
