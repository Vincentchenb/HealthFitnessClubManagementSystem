# **Health and Fitness Club Management System**

A comprehensive Python application for managing a health and fitness club, featuring member profiles, trainer schedules, class registrations, room bookings, equipment maintenance, and billing systems.



## Member Functions:
- Profile Management: Register new members and update personal information
- Dashboard: View fitness goals, class schedules, and progress tracking
- Schedule Management: Book, reschedule, or cancel personal training sessions
- Class Registration: Sign up for group fitness classes
- Payment Processing: Handle monthly membership fees

## Trainer Functions:
- Schedule Management: Add or remove availability slots
- Member Viewing: Access member profiles and dashboards
- Session Management: Handle personal training sessions

## Admin Functions:
- Room Booking Management: Create, confirm, and cancel room bookings
- Equipment Monitoring: Track maintenance schedules and equipment status
- Class Scheduling: Create and update fitness class schedules
- Billing System: Process payments and generate bills

## Prerequisites:
- Python 3.x
- PostgreSQL
- psycopg3 library
- pgAdmin4 (recommended)

## Installation & Setup:

1.  Install Dependencies
- `pip install psycopg`
2. Database Setup
- Open pgAdmin4 and create a new database named 3005_Project
- Run the 3005_Project_DDL.sql file in the PostgreSQL query tool to create all tables
- Run the 3005_Project_DML.sql file to populate the database with sample data
3. Configure Database Connection
- In the 3005_Project.py file, locate the database connection line: 
  - `connection = psycopg.connect("dbname=3005_Project user=postgres password=ILove3005")`
- Change ILove3005 to your actual pgAdmin4 password.
4. Run the application
`python 3005_Project.py`

## Database Schema:
- The system uses the following main tables:
- Members: Member profiles and fitness goals
- Trainers: Trainer information
- Sessions: Personal training sessions
- Classes: Group fitness classes
- Registrations: Member-class relationships
- RoomBookings: Room scheduling
- Equipment: Equipment maintenance tracking
- Bills: Payment and billing information
- Availabilities: Trainer availability schedules

## Usage Guide:
For Members:
- Choose "Member" role at startup
- Register as a new member or login with existing ID
- Access dashboard to view progress and scheduled activities
- Manage profile information and fitness goals
- Schedule personal training sessions or register for classes

For Trainers:
- Choose "Trainer" role at startup
- Login with trainer ID
- Manage availability schedule
- View member profiles and progress

For Administrators:
- Choose "Admin" role at startup
- Enter admin password: iamadmin123
- Manage room bookings and equipment maintenance
- Update class schedules and process payments

## Security Notes:
- Default admin password: iamadmin123
- Consider changing default passwords in production environment
- Member and trainer IDs are auto-generated during registration

## Troubleshooting:
 - Ensure PostgreSQL service is running
 - Verify database connection credentials
 - Check that all SQL files executed successfully
 - Confirm psycopg3 installation

## File Structure:
- `3005_Project_DDL.sql` - Database table definitions
- `3005_Project_DML.sql` - Sample data insertion
- `3005_Project.py` - Main application code
