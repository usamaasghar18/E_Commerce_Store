E-Commerce Store

This is an E-Commerce Store project built with FastAPI that provides an online shopping platform. The platform includes features like browsing products, adding them to a shopping cart, making purchases, and tracking orders. The system also generates invoices and integrates with third-party payment gateways like Stripe and PayPal.

Project Structure

```
ecommerce_store/
├─ app/
│  ├─ api/
│  │  ├─ __init__.py
│  │  ├─ main.py                            # FastAPI entry point
│  │  ├─ routes/
│  │  │  ├─ __init__.py
│  │  │  ├─ auth.py                         # User signup/login endpoints
│  │  │  ├─ health.py                       # Health check
│  │  ├─ dependencies.py                    # Shared dependencies (e.g., DB sessions)
│  │  └─ error_handlers.py                  # Error handling
│  │
│  ├─ core/
│  │  ├─ __init__.py
│  │  ├─ config.py                          # App config, environment variables
│  │  ├─ logging_config.py                  # Logging setup
│  │  ├─ security.py                        # Authentication & JWT
│  │  ├─ settings.py                        # Global settings
│  │  └─ scheduling.py                      # Scheduling ETL jobs (if using cron or Celery)
│  │
│  ├─ db/
│  │  ├─ __init__.py
│  │  ├─ database.py                        # SQLAlchemy engine, sessions
│  │  ├─ models.py                          # SQLAlchemy models (Users, Products, Orders, etc.)
│  │  ├─ migrations/                        # Alembic migrations
│  │  │  ├─ env.py
│  │  │  ├─ script.py.mako
│  │  │  └─ versions/
│  │  └─ crud/
│  │     ├─ __init__.py
│  │     ├─ users.py                        # CRUD for user accounts
│  │     ├─ products.py                     # CRUD for products
│  │     ├─ orders.py                       # CRUD for orders
│  │     └─ cart.py                         # CRUD for cart
│  │     └─ categories.py                   # CRUD for categories
│  │
│  ├─ schemas/
│  │  ├─ __init__.py
│  │  ├─ auth.py                            # Signup/Login request/response models
│  │  ├─ product.py                         # Pydantic models for products
│  │  ├─ order.py                           # Pydantic models for orders
│  │  ├─ cart.py                            # Pydantic models for cart
│  │  ├─ common.py                          # Shared Pydantic models
│  │
│  ├─ services/
│  │  ├─ __init__.py
│  │  ├─ payment_gateway.py                 # Integration with Stripe/PayPal
│  │  ├─ email_notifications.py             # Email services for order confirmation
│  │
│  ├─ utils/
│  │  ├─ __init__.py
│  │  ├─ constants.py
│  │  ├─ helpers.py
│  │  └─ exceptions.py
│  │
│  └─ docs/
│     ├─ __init__.py
│     └─ openapi_description.md
│
├─ .env.example
├─ .gitignore
├─ Dockerfile
├─ docker-compose.yml
├─ requirements.txt or pyproject.toml
├─ README.md
└─ alembic.ini
```

Features
- Product Listings with categories, search, and filters
- User Registration, Cart, and Checkout System
- Order Tracking and Invoice Generation
- Admin Panel for managing products, categories, and orders
- Payment Gateway Integration with Stripe/PayPal
