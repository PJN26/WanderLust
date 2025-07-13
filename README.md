# WanderLust
# WanderLust 🧭

A full-stack web application for listing and managing rental properties, built with Node.js, Express, and MongoDB. This project is inspired by Airbnb and allows users to browse, create, edit, and delete property listings.

## Features

- **Property Listings**: View all available rental properties
- **Property Details**: Detailed view of individual properties with images, descriptions, pricing, and location
- **CRUD Operations**: Create, Read, Update, and Delete property listings
- **Responsive Design**: Mobile-friendly interface using Bootstrap
- **Image Handling**: Default image fallback for properties without images
- **Database Integration**: MongoDB integration for data persistence

## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB with Mongoose ODM
- **Frontend**: EJS templating engine
- **Styling**: Bootstrap 5, Font Awesome icons, Custom CSS
- **Additional Libraries**: 
  - `ejs-mate` for layout support
  - `method-override` for HTTP method support

## Project Structure

```
WanderLust/
├── app.js              # Main application file
├── package.json        # Dependencies and scripts
├── models/
│   └── listing.js      # Mongoose model for listings
├── init/
│   ├── data.js         # Sample data for seeding
│   └── index.js        # Database initialization script
├── views/
│   ├── layouts/
│   │   └── boilerplate.ejs  # Main layout template
│   ├── includes/
│   │   ├── navbar.ejs       # Navigation bar
│   │   └── footer.ejs       # Footer
│   └── listings/
│       ├── index.ejs        # All listings page
│       ├── show.ejs         # Individual listing page
│       ├── new.ejs          # Create new listing form
│       └── edit.ejs         # Edit listing form
└── public/
    ├── css/
    │   └── style.css        # Custom styles
    └── js/                  # JavaScript files
```

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd WanderLust
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up MongoDB**
   - Make sure MongoDB is installed and running on your system
   - The application connects to `mongodb://127.0.0.1:27017/wanderlust`

4. **Initialize the database with sample data**
   ```bash
   node init/index.js
   ```

5. **Start the application**
   ```bash
   node app.js
   ```

6. **Access the application**
   - Open your browser and go to `http://localhost:8080`

## API Routes

| Method | Route | Description |
|--------|-------|-------------|
| GET | `/` | Home page |
| GET | `/listings` | View all listings |
| GET | `/listings/new` | Form to create new listing |
| POST | `/listings` | Create new listing |
| GET | `/listings/:id` | View specific listing |
| GET | `/listings/:id/edit` | Form to edit listing |
| PUT | `/listings/:id` | Update listing |
| DELETE | `/listings/:id` | Delete listing |

## Database Schema

The `Listing` model includes:
- `title` (String, required): Property title
- `description` (String): Property description
- `image` (String): Property image URL with default fallback
- `price` (Number): Price per night
- `location` (String): Property location
- `country` (String): Property country

## Dependencies

```json
{
  "ejs": "^3.1.10",
  "ejs-mate": "^4.0.0",
  "express": "^5.1.0",
  "method-override": "^3.0.0",
  "mongoose": "^8.16.1"
}
```

## Features Overview

### Home Page
- Welcome message and navigation to listings

### Listings Page
- Grid layout displaying all properties
- Property cards with images, titles, and pricing
- Responsive design for different screen sizes

### Individual Listing Page
- Detailed property information
- Edit and delete functionality
- High-quality image display

### Create/Edit Listing
- Form-based property management
- Image URL validation with fallback
- Input validation and error handling

## Styling

The application uses:
- **Bootstrap 5** for responsive grid system and components
- **Font Awesome** for icons
- **Google Fonts** (Plus Jakarta Sans) for typography
- **Custom CSS** for brand-specific styling

## Future Enhancements

- User authentication and authorization
- Image upload functionality
- Search and filtering capabilities
- Reviews and ratings system
- Booking functionality
- Payment integration
- Email notifications

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the ISC License.

## Contact

For questions or support, please contact the development team.

---

**Note**: This is a learning project created as part of web development training. It demonstrates full-stack development concepts including RESTful routing, database integration, and responsive web design.
