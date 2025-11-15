Project Portfolio Manager
A web-based application built with Tailwind CSS that helps you track and organize projects for your portfolio. Store project details locally in your browser and easily filter by category or importance to prioritize which projects to showcase.

Features
Project Management: Add, view, and delete projects with detailed information

Image Upload: Upload thumbnail images for projects with drag-and-drop support

Category System: Organize projects by customizable categories

Priority Levels: Mark projects as High, Medium, or Low importance

Advanced Filtering: Filter projects by category and importance level

Local Storage: All data persists locally in your browser

Responsive Design: Works seamlessly on desktop and mobile devices

Project Details Captured
Project Name

Date

Category

Importance Level (High/Medium/Low)

Description

Thumbnail Image

Getting Started
Prerequisites
A modern web browser (Chrome, Firefox, Safari, Edge)

No additional dependencies required

Installation
Download the index.html file

Open it directly in your web browser

Start adding your projects!

Usage
Adding a New Project
Fill in the project details in the form:

Project Name (required)

Date (required)

Category (select from dropdown or add new)

Importance Level (High/Medium/Low)

Description

Thumbnail Image (upload via drag-and-drop or click to browse)

Click "Add Project" to save

Managing Categories
To add a new category:

Type the category name in the "Add New Category" field

Click the plus (+) button

The new category will be available in all dropdowns

Filtering Projects
Use the "Filter by Category" dropdown to show projects from specific categories

Use the "Filter by Importance" dropdown to show projects by priority level

Click "Clear Filters" to reset all filters

Deleting Projects
Click the "Delete" button on any project card

Confirm deletion in the prompt

Data Storage
All project data and categories are stored locally in your browser's localStorage. This means:

✅ Your data persists between browser sessions

✅ No server or internet connection required

✅ Your data remains private on your device

⚠️ Clearing browser data will delete your projects

⚠️ Data is not synced across devices

Browser Compatibility
Chrome 60+

Firefox 55+

Safari 11+

Edge 79+

File Structure
text
project-portfolio-manager/
│
└── index.html (single file containing all HTML, CSS, and JavaScript)
Technical Details
Built with vanilla JavaScript

Uses Tailwind CSS for styling

Font Awesome for icons

LocalStorage for data persistence

Base64 encoding for image storage

Drag-and-drop file upload support

Customization
Adding Default Categories
Modify the categories array in the JavaScript section to include your preferred default categories:

javascript
let categories = JSON.parse(localStorage.getItem('portfolioCategories')) || [
    'Web Development', 'Mobile App', 'Design', 'Research', 'Other'
];
Modifying Image Upload Limits
Change the file size limit (currently 5MB) in the initImageUpload() function:

javascript
// Change from 5MB to 10MB
if (file.size > 10 * 1024 * 1024) {
    showNotification('Image size should be less than 10MB!', 'error');
    return;
}
Troubleshooting
Common Issues
Projects not saving: Check if localStorage is enabled in your browser

Images not uploading: Ensure files are under 5MB and are valid image formats

Filters not working: Try refreshing the page or clearing browser cache

Data Backup
To backup your projects:

Open Developer Tools (F12)

Go to Application tab → Local Storage

Copy the values for portfolioProjects and portfolioCategories

To restore:

Replace the values in Local Storage with your backup data

Refresh the page

License
