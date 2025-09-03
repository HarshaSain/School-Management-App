# School Management System

A modern web application built with Next.js for managing school information. This system allows you to add new schools with complete details and view all registered schools in a beautiful, responsive interface.

## Features

- ✅ **Add New Schools**: Complete form with validation for school information
- ✅ **View All Schools**: Beautiful card-based layout showing all school details
- ✅ **Image Upload**: Support for school image uploads
- ✅ **Responsive Design**: Works perfectly on desktop, tablet, and mobile
- ✅ **Form Validation**: Client-side validation with error messages
- ✅ **Database Integration**: MySQL database for persistent storage
- ✅ **Modern UI**: Built with Tailwind CSS for a professional look

## Tech Stack

- **Frontend**: Next.js 15, React 19, Tailwind CSS
- **Backend**: Next.js API Routes
- **Database**: MySQL with mysql2 driver
- **Form Handling**: React Hook Form
- **File Upload**: Formidable for image handling

## Prerequisites

Before running this application, make sure you have:

- Node.js (v18 or higher)
- MySQL database server
- npm or yarn package manager

## Installation & Setup

### 1. Clone and Install Dependencies

```bash
cd my-app
npm install
```

### 2. Database Setup

1. Create a MySQL database:
```sql
CREATE DATABASE school_management;
```

2. Run the database setup script:
```bash
mysql -u your_username -p school_management < database_setup.sql
```

### 3. Environment Configuration

Create a `.env.local` file in the root directory:

```env
# Database Configuration
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=school_management
DB_PORT=3306
```

### 4. Run the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the application.

## Project Structure

```
my-app/
├── pages/
│   ├── index.js              # Home page with navigation
│   ├── addSchool.jsx         # Add new school form
│   ├── showSchools.jsx       # Display all schools
│   └── api/
│       ├── addSchool.js      # API endpoint for adding schools
│       └── getSchools.js     # API endpoint for fetching schools
├── lib/
│   └── db.js                 # Database connection configuration
├── public/
│   └── schoolImages/         # Directory for uploaded school images
├── database_setup.sql        # Database schema and sample data
└── .env.local               # Environment variables (create this)
```

## Usage

### Adding a New School

1. Navigate to the home page
2. Click "Add New School"
3. Fill in the required information:
   - School Name
   - Address
   - City
   - State
   - Contact Number
   - Email Address
   - School Image (optional)
4. Click "Add School" to save

### Viewing Schools

1. From the home page, click "View Schools"
2. Browse all registered schools in a card layout
3. Each card shows:
   - School image
   - Name and address
   - City and state
   - Contact information
   - Email address

## API Endpoints

- `POST /api/addSchool` - Add a new school
- `GET /api/getSchools` - Retrieve all schools

## Database Schema

The `schools` table includes:
- `id` (Primary Key)
- `name` (School Name)
- `address` (Full Address)
- `city` (City)
- `state` (State)
- `contact` (Contact Number)
- `email_id` (Email Address)
- `image` (Image Path)
- `created_at` (Timestamp)
- `updated_at` (Timestamp)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).
