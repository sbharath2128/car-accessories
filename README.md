# c2j car accessories

A comprehensive Django-based e-commerce website for car accessories with user registration, product catalog, and MySQL database integration.

## Features

### User Management
- User registration with name, phone number, car name, and car type (4 sets or above 4 sets)
- Login/logout functionality
- User profile management
- Secure authentication system

### Product Catalog
- Product categories and filtering
- Search functionality
- Product details pages
- Featured products display
- Related products recommendations

### Website Pages
- **Home**: Hero section, featured products, categories showcase
- **Products**: Product catalog with filters and search
- **Product Detail**: Individual product information
- **About**: Company information and team
- **Contact**: Contact form and information

### Technical Features
- Django 4.2.7 framework
- MySQL database integration
- Bootstrap 5 responsive design
- Crispy Forms for form styling
- Django admin panel for content management

## Installation

### Prerequisites
- Python 3.8+
- MySQL server
- pip

### Setup Instructions

1. **Clone and navigate to the project:**
   ```bash
   cd "c:/Users/abc/Desktop/sandaru anna"
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up MySQL database:**
   ```sql
   CREATE DATABASE caraccessories_db;
   ```

4. **Configure database settings:**
   - Edit `caraccessories_shop/settings.py`
   - Update MySQL connection details (username, password)

5. **Run migrations:**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Create superuser:**
   ```bash
   python manage.py createsuperuser
   ```

7. **Collect static files:**
   ```bash
   python manage.py collectstatic
   ```

8. **Run the development server:**
   ```bash
   python manage.py runserver
   ```

9. **Access the website:**
   - Frontend: http://127.0.0.1:8000/
   - Admin Panel: http://127.0.0.1:8000/admin/

## Project Structure

```
caraccessories_shop/
├── caraccessories_shop/     # Main Django project settings
├── accounts/               # User management app
│   ├── models.py          # User profile, products, orders models
│   ├── views.py           # Registration, profile views
│   ├── forms.py           # User registration forms
│   └── admin.py           # Django admin configuration
├── shop/                  # Shop functionality app
│   ├── views.py           # Home, products, about, contact views
│   └── urls.py            # Shop URL routing
├── templates/             # HTML templates
│   ├── accounts/          # User-related templates
│   └── shop/              # Shop-related templates
├── static/                # CSS, JavaScript, images
├── media/                 # User uploaded files
├── requirements.txt       # Python dependencies
└── manage.py             # Django management script
```

## Database Models

### CustomerProfile
- Links to Django User model
- Phone number
- Car name
- Car type (4 sets or above 4 sets)

### ProductCategory
- Category name and description

### Product
- Product name, description, price
- Category relationship
- Image upload
- Stock and featured status

### Order & OrderItem
- Order management system
- Customer relationship
- Order status tracking

## Admin Panel Features

- User management
- Product catalog management
- Order processing
- Category management
- Inventory tracking

## Frontend Features

- Responsive Bootstrap 5 design
- Modern UI with Font Awesome icons
- Product search and filtering
- User authentication forms
- Contact form
- FAQ section

## Usage

1. **Register as a user** with your details and car information
2. **Browse products** by category or search
3. **View product details** and related items
4. **Contact support** through the contact form
5. **Manage your profile** information

## Development

To add new features:
1. Create models in `accounts/models.py`
2. Update admin configuration in `accounts/admin.py`
3. Add views in relevant apps
4. Create templates in the `templates/` directory
5. Update URL configurations

## License

This project is open source and available under the MIT License.
