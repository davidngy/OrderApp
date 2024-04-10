# ServeSavvy: CS50 Web Final Project

### Distinctiveness

ServeSavvy sets itself apart in the landscape of web applications through its focused application and innovative use of technology tailored specifically for the restaurant industry:

- **Industry-Specific Solution**: ServeSavvy addresses the unique operational challenges of restaurants with features such as real-time table management and dynamic menu customization. This targeted approach ensures that ServeSavvy is not just a generic solution but a practical tool designed to enhance the efficiency of restaurant operations.

- **Customized User Experience**: Utilizing token-based mechanisms primarily for session management, ServeSavvy enhances user interaction with the application. This approach allows for a seamless experience, ensuring users have access to features and data relevant to their current context without compromising the application’s responsiveness.

- **Advanced Technology Integration**: The combination of Django with React, complemented by the sophisticated use of serializers and React hooks like `useEffect` and `useState`, demonstrates ServeSavvy's commitment to leveraging cutting-edge technologies. This not only supports complex functionalities but also sets a benchmark for creating dynamic and engaging user interfaces.

The focus on real world use, coupled with innovative technology use, clearly distinguishes ServeSavvy from other cs50 projects.

### Complexity

The development journey of ServeSavvy brought to light several complex aspects that significantly contribute to its sophistication:

- **Intricate Data Relationships**: The application’s core functionality hinged on carefully planned database schemas that captured complex relationships between tables, menu items, and orders. Navigating these relationships was pivotal in ensuring the application could efficiently manage and display interconnected data.

- **Dynamic Session Management**: The strategic use of tokens for maintaining user sessions facilitated a consistent and customized user experience across the application. This focus was essential for managing access to features and information dynamically, based on the user’s interaction context.

- **Responsive Frontend Development**: Employing React and its hooks represented a considerable learning curve but was crucial for achieving a dynamic and responsive user interface. The effective application of `useState` and `useEffect` enabled real-time updates and sophisticated state management, elevating the user experience to new heights.

These elements underscore ServeSavvy's complexity, reflecting the depth of technical challenges overcome and the sophisticated approach adopted in its creation.

## Project Structure

The ServeSavvy project is organized into two main directories: `backend` and `frontend`, each containing specific components of the application. Below is a detailed overview of these directories and their contents:

### Backend

The backend of ServeSavvy handles the business logic, database operations, and API endpoints.

- `backend/`
  - `api/` - Contains the core API logic for the ServeSavvy application.
    - `admin.py` - Configures the admin panel for the ServeSavvy application, allowing administrators to manage app data.
    - `models.py` - Defines the database models used by ServeSavvy, representing tables, menu items, orders, etc.
    - `views.py` - Contains the views that handle requests and responses for the ServeSavvy application. Each view connects to specific API endpoints.
    - `serializers.py` - Contains serializers for converting complex data types, like Django model instances, to native Python datatypes and back, facilitating the serialization of model data into JSON format for API responses.

  - `backend/` - Houses the project's settings and URL configurations.
  
    - `settings.py` - Contains all configurations for the ServeSavvy Django project, including database settings, security configurations, and third-party app registrations.
    - `urls.py` - Defines the URL routes for the entire ServeSavvy application, mapping URLs to their corresponding views.

### Frontend

The frontend of ServeSavvy provides the user interface, allowing users to interact with the application through a web browser.

- `frontend/`

  - `src/`
  - `views/` - This directory contains all the React components that represent pages or views in the application.
    - `Category.js` - Manages the categories section of the menu and displays the menu items
    - `HomePage.js` - Acts as the welcoming interface of ServeSavvy, presenting the central dashboard where users can view and manage restaurant tables
    - `Login.js` - Handles user login functionality.
    - `Menu.js` - Displays the categories and allows for menu management.
    - `OrderPage.js` - Used for creating and managing orders.
    - `Register.js` - Allows new users to register for an account.
  - `App.js`: The main React component that orchestrates the rendering of different pages and components based on user interaction.
  - `public/` - Houses static assets and the `index.html` file, which is the entry point for the React application.

## How to Run ServeSavvy

To get ServeSavvy up and running on your local machine, follow these steps after ensuring you have Python, Node.js, and npm installed:

### Setting Up the Frontend

1. Navigate to the `frontend` directory from the root of the project:
cd frontend


2. Install the required npm packages:
npm install


3. Start the React development server:
npm start


The frontend of the application will now be running on `http://localhost:3000`.

### Setting Up the Backend

1. Open a new terminal window or tab and navigate to the `backend` directory from the root of the project:
cd backend


2. If you haven't already done so, install the required Python packages using:
pip install -r requirements.txt

3. Start the Django development server:
python manage.py runserver

The backend API will now be accessible on `http://localhost:8000`.

Make sure to run both the frontend and backend servers concurrently to have the full functionality of ServeSavvy available.

### Initial Configuration

If it's the first time you are running the project, you might need to set up the database. In the `backend` directory, run:
python manage.py makemigrations
python manage.py migrate


This will prepare your database schema based on the models defined.

### Accessing the Application

With both servers running, open your web browser and go to `http://localhost:3000` to start using ServeSavvy. You should see the ServeSavvy landing page and be able to interact with the application.

## Technology Stack

ServeSavvy is built with the following technologies and libraries:

- **Backend**: Django 5.0.1, Django REST Framework 3.14.0, django-cors-headers 4.3.1
- **Frontend**: React 17.0.2, Tailwind CSS 2.2.19
- **Database**: SQLite (Development)

## Key Features

- **Real-time Table Management**: Dynamically add, remove, and manage tables.
- **Menu Management**: Create and categorize menu items with ease.
- **Order Processing**: Take and manage orders, automatically calculate totals.
- **Visual Indicators**: Quickly identify table statuses with color-coded visual cues.





