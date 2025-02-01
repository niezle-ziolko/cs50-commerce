# CS50 Project 2 - Commerce

A custom design project for CS50's Web Programming with Python and JavaScript course, which is a simple clone of eBay. The project utilizes Django, HTML, and CSS.

## Demo

A short video where I go through the required specifications of the project: [https://youtu.be/yONq8muabkU](https://youtu.be/yONq8muabkU)

### Test Login Credentials

|  Username   |    Password    |
|-------------|----------------|
|    Admin    |    password    |
|    John     |    password    |

---

## Project Requirements

### Website Structure

Your site must include the following core features:

1. **User Authentication**:
   - Users can register for an account, log in, and log out.
   - The application displays different content based on whether a user is signed in.

2. **Create Listing**:
   - Users can create new auction listings by providing a title, description, starting bid, and optional image URL and category.
   - Listings are saved to the database and displayed on the active listings page.

3. **Active Listings Page**:
   - The default route of the application displays all currently active auction listings.
   - Each listing shows the title, description, current price, and photo (if available).

4. **Listing Detail Page**:
   - Clicking on a listing takes users to a dedicated page with all details about the listing.
   - Signed-in users can bid on the item, add it to their watchlist, and leave comments.
   - If the user created the listing, they can close the auction, declaring the highest bidder as the winner.

5. **Watchlist**:
   - Users can view all listings they have added to their watchlist.
   - Clicking on a watchlisted item takes the user to that listing's detail page.

6. **Categories**:
   - Users can browse listings by category.
   - Clicking on a category name displays all active listings within that category.

7. **Django Admin Interface**:
   - Administrators can manage listings, bids, and comments through the Django admin interface.

---

## Additional Notes

- **Consistency**: Ensure that the layout, styling, and navigation maintain a cohesive design across the site.
- **Error Handling**: Provide clear feedback for invalid inputs, such as bids that do not meet the required criteria.
- **Extensibility**: The design and code should allow for future enhancements without significant rework.

---

## Running the Application

To start the application, follow these steps:

1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt

2. Running migrations:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   
2. Start the application
   ```bash
   python manage.py runserver

## Build static assets

To build static assets, follow these steps:

```bash
python manage.py collectstatic