# Toyota Kenya Inventory and Parts Tracking System

## Project Description
A comprehensive database management system designed for Toyota Kenya to manage vehicle sales and spare parts inventory across its nationwide branches. The system tracks stock levels, repair parts usage, customer purchases, and supplier deliveries.

### Key Features
- Multi-branch inventory management
- Vehicle sales tracking
- Spare parts inventory control
- Customer management
- Supplier management
- Service records tracking
- Parts order processing
- Stock level monitoring

## Database Structure
The system consists of 12 interconnected tables:
1. `branches` - Branch information
2. `suppliers` - Supplier details
3. `vehicle_models` - Vehicle model catalog
4. `parts` - Spare parts catalog
5. `inventory` - Stock levels across branches
6. `customers` - Customer information
7. `vehicle_sales` - Vehicle sales records
8. `parts_orders` - Parts order headers
9. `parts_order_details` - Parts order line items
10. `supplier_deliveries` - Supplier delivery headers
11. `supplier_delivery_details` - Supplier delivery line items
12. `service_records` - Vehicle service history
13. `service_parts_used` - Parts used in services

## Setup Instructions

### Prerequisites
- MySQL Server (version 5.7 or higher)
- MySQL Workbench (recommended for database management)

### Installation Steps
1. Clone or download this repository
2. Open MySQL Workbench or your preferred MySQL client
3. Create a new database connection if needed
4. Open the `one.sql` file
5. Execute the SQL script to create the database and tables

### Alternative Method (Command Line)
```bash
# Login to MySQL
mysql -u your_username -p

# Once logged in, run the SQL file
source path/to/one.sql
```

## Database Schema
The database implements the following relationships:
- One-to-Many relationships between branches and inventory
- Many-to-Many relationships between orders and parts
- One-to-One relationships in service records
- Foreign key constraints ensuring data integrity
- Unique constraints on critical fields

## Entity Relationship Diagram (ERD)
![toyota_erd png](https://github.com/user-attachments/assets/8d2e2ab5-b42f-4164-8ec0-dfc2c4755012)


The ERD shows the relationships between all tables in the system. Key relationships include:
- Branches to Inventory (One-to-Many)
- Customers to Orders (One-to-Many)
- Parts to Inventory (One-to-Many)
- Orders to Parts (Many-to-Many through order_details)
- Services to Parts (Many-to-Many through service_parts_used)

## Data Types and Constraints
- Primary Keys: Auto-incrementing integers
- Foreign Keys: Referential integrity maintained
- NOT NULL constraints on required fields
- UNIQUE constraints on critical fields
- Timestamps for tracking creation and updates
- Appropriate data types for different fields (VARCHAR, INT, DECIMAL, etc.)

## Contributing
Feel free to submit issues and enhancement requests.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
