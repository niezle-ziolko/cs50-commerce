# CS50 Project 2 - Commerce

This project is a simple clone of eBay built with Django, HTML, and CSS. It is part of CS50’s Web Programming with Python and JavaScript course and features user authentication, auction listings, bidding, watchlists, categories, and an admin interface.

## 🗂️ Project Structure

The Django project contains the following key elements:

```
commerce/
├── auctions/                # Django app for listings, bids, and categories
│   ├── migrations/
│   │   ├── __init__.py
│   │   ├── 0001_initial.py
│   │   ├── 0002_alter_auctionlisting_image_url.py
│   │   ├── 0003_comment_image.py
│   │   ├── 0004_remove_auctionlisting_image_url_auctionlisting_image_and_more.py
│   │   ├── 0005_alter_auctionlisting_id_alter_bid_id_and_more.py
│   │   ├── 0006_alter_bid_amount_alter_bid_created_at_and_more.py
│   │   └── 0007_remove_bid_unique_bid_per_time_alter_bid_amount_and_more.py
│   ├── static/
│   │   └── auctions/
│   │       ├── favicon.ico
│   │       ├── logo.png
│   │       ├── logo.svg
│   │       ├── market-sans-regular.woff2
│   │       ├── market-sans-semibold.woff2
│   │       ├── register.webp
│   │       ├── script.js
│   │       └── styles.css
│   ├── templates/
│   │   └── auctions/
│   │       ├── categories.html
│   │       ├── category.html
│   │       ├── create.html
│   │       ├── index.html
│   │       ├── layout.html
│   │       ├── listing.html
│   │       ├── login.html
│   │       ├── register.html
│   │       └── watchlist.html
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── commerce/                # Main project configuration
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── media/
│   ├── auction_images
│   └── placeholder.webp
├── .gitignore
├── LICENSE
├── manage.py
├── README.md
└── requirements.txt
```

## ✅ Features Overview

This section summarizes the core features implemented in the application.

### 🔑 User Authentication
  - **Registration**: Users can create a new account by providing their username and password.
  - **Login/Logout**: Users can log in and log out of the platform.
  - The content displayed on the site changes depending on whether the user is signed in.

### 📝 Create Listing
  - Users can create new auction listings by providing:
    - Title
    - Description
    - Starting bid
    - Optional image URL and category
  - Listings are saved to the database and are visible on the **Active Listings** page.

### 📄 Active Listings Page
  - The main page of the site shows all currently active auction listings.
  - Each listing includes:
    - Title
    - Description
    - Current price
    - Image (if provided)

### 🏷️ Listing Detail Page
  - Clicking on a listing takes users to a dedicated detail page with more information.
  - **Signed-in users** can:
    - Bid on the item
    - Add the listing to their watchlist
    - Leave comments
  - Listing owners can close the auction, declare the highest bidder as the winner, and finalize the sale.

### 👁️ Watchlist
  - Users can view all listings they have added to their watchlist.
  - Clicking on a watchlisted item redirects to its detail page.

### 🗂️ Categories
  - Users can browse listings by category.
  - Clicking on a category name displays all active listings within that category.

### 🛠️ Django Admin Interface
  - **Administrators** can manage listings, bids, and comments through the Django admin interface.

### 💡 Additional Notes
  - **Consistency**: Ensure that the layout, styling, and navigation are cohesive and easy to use.
  - **Error Handling**: The app provides clear error messages, e.g., if a bid doesn’t meet the required criteria.
  - **Extensibility**: The design and code are modular, allowing for future features and improvements.

## 🚀 Running the Application

To run the app locally:

# Install dependencies

```bash
pip install -r requirements.txt
```

# Database setup

```bash
python manage.py makemigrations
python manage.py migrate
```

# Start development server

```bash
python manage.py runserver
```

## 🧱 Static Assets

To collect and build static assets:

```bash
python manage.py collectstatic
```

## 🎥 Demo

Video walkthrough of the project and specifications:
👉 https://youtu.be/yONq8muabkU

### 🔐 Test Login Credentials

| Username | Password |
|----------|----------|
|  Admin   | password |
|  John    | password |

## 📜 Certification
This project was submitted as part of the CS50’s Web Programming with Python and JavaScript course offered by Harvard University.
Upon successful completion, I was awarded a certificate, which is available here:

🎓 [View Certificate](https://certificates.cs50.io/6f5116d0-882d-4fc1-9dc6-0c96c5d4c7b1.pdf)
