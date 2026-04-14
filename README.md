# 📚 School Fees Management System

A complete web-based solution for managing school fees, student records, payments, and financial reports. Built with HTML, CSS, and JavaScript using localStorage for data persistence.

## Features

### ✨ Core Features

- **🔐 Admin Authentication** - Secure login system with demo credentials
- **👥 Student Management** - Add, edit, and manage student records
- **💰 Fee Management** - Create and manage fee structures for students
- **💳 Payment Recording** - Track all payments with detailed records
- **📊 Financial Reports** - Generate various reports and analytics
- **📄 Invoice Generation** - Create and print professional invoices
- **📈 Dashboard Analytics** - Real-time financial statistics and metrics
- **⚙️ Settings Management** - Configure school information and system settings
- **💾 Data Backup & Restore** - Export and import data for backup

### Dashboard Features

- Total students count
- Total fee amount and collection status
- Recent payment history
- Pending payment reminders
- Real-time statistics

### Student Management

- Add/edit/delete student records
- Store contact information (email, phone)
- Assign student to class
- Track parent contact details
- Search and filter students

### Fee Management

- Create fee records for students
- Support multiple fee types (tuition, bus, etc.)
- Set due dates
- Track fee status (pending, paid, partial, overdue)
- Filter by class or search

### Payment Tracking

- Record student payments
- Support multiple payment methods (cash, check, transfer, card)
- Track payment reference numbers
- Automatic fee status updates
- Payment history and records

### Reports & Analytics

- **Fee Summary Report** - Overview of all fees
- **Student-wise Report** - Individual student financial status
- **Class-wise Report** - By-class fee collection analysis
- **Monthly Report** - Payment trends over time
- **Overdue Report** - Identify late payments
- **Export to CSV** - Download reports as CSV files
- **Invoice Generation** - Print professional invoices

## Getting Started

### System Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- No backend server required
- Uses browser localStorage for data persistence

### Installation

1. Open `index.html` in your web browser
2. Or serve the files using a local server (e.g., Python, Node.js)

#### Using Python:
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

#### Using Node.js:
```bash
# Install http-server globally
npm install -g http-server

# Run in the project directory
http-server
```

Then open `http://localhost:8000` in your browser.

## Desktop App with Electron

This project can be packaged as a desktop application using Electron.

1. Install dependencies:
```bash
npm install
```
2. Start the desktop app locally:
```bash
npm run start
```
3. Package the app for Windows:
```bash
npm run package
```

The packaged app will be created in the `dist/` folder.

## Publish to GitHub Pages

1. Create a new GitHub repository and push this project to it.
2. In the repository settings, enable **GitHub Pages**.
   - Set the source to `main` or `master` branch and `/root` folder.
3. Wait a few minutes for GitHub Pages to build your site.
4. Your site will be available at `https://<your-username>.github.io/<repo-name>/`.
5. Add that public URL to Google Search Console and request indexing.

### Optional: Add a custom domain

- Add a `CNAME` file with your custom domain name.
- Configure your DNS provider to point to GitHub Pages.

## Usage Guide

### Login

**Demo Credentials:**
- **Username:** `admin`
- **Password:** `admin123`

### Navigation

The sidebar provides easy access to all modules:
- 📊 Dashboard - Main overview
- 👥 Students - Student management
- 💰 Fees Management - Fee administration
- 💳 Payments - Payment recording
- 📈 Reports - Financial reports
- ⚙️ Settings - System configuration

### Adding Students

1. Go to **👥 Students** page
2. Click **+ Add Student**
3. Fill in student details:
   - Full Name
   - Roll Number
   - Class (1-5)
   - Email
   - Phone (optional)
   - Parent Phone (optional)
   - Address (optional)
4. Click **Save Student**

### Creating Fees

1. Go to **💰 Fees Management**
2. Click **+ Add Fee**
3. Select Student
4. Enter Fee Details:
   - Fee Type (e.g., "Tuition Fee")
   - Amount
   - Due Date
   - Academic Year (optional)
   - Description (optional)
5. Click **Save Fee**

### Recording Payments

1. Go to **💳 Payments**
2. Click **+ Record Payment**
3. Select Student and Fee
4. Enter Payment Details:
   - Amount Paid
   - Payment Date
   - Payment Method
   - Reference Number (optional)
   - Notes (optional)
5. Click **Record Payment**

### Generating Reports

1. Go to **📈 Reports**
2. Select Report Type:
   - Fee Summary Report
   - Student-wise Report
   - Class-wise Report
   - Monthly Payment Report
   - Overdue Fees Report
3. Set date range if applicable
4. Click **Generate Report**
5. Use **📥 Export Report** to download as CSV

### Creating Invoices

1. Go to **📈 Reports**
2. Scroll to "Generate Invoices"
3. Select Student
4. Select Fee
5. Click **Generate Invoice**
6. Print or save the invoice

## File Structure

```
html-css/
├── index.html                 # Login page
├── dashboard.html             # Main dashboard
├── pages/
│   ├── students.html         # Student management
│   ├── fees.html             # Fee management
│   ├── payments.html         # Payment tracking
│   ├── reports.html          # Reports & analytics
│   └── settings.html         # System settings
├── css/
│   └── styles.css            # Main stylesheet
├── js/
│   ├── data.js               # Data management & localStorage
│   ├── auth.js               # Authentication
│   ├── main.js               # Dashboard functionality
│   ├── students.js           # Student management
│   ├── fees.js               # Fee management
│   ├── payments.js           # Payment processing
│   ├── reports.js            # Reports & analytics
│   └── settings.js           # Settings management
└── README.md                 # This file
```

## Key JavaScript Modules

### data.js (DataManager)
Handles all data operations with localStorage:
- Student management
- Fee management
- Payment tracking
- School settings
- Data import/export

### auth.js (AuthManager)
Manages user authentication:
- User login/logout
- Session management
- Auth verification
- Remember me functionality

### main.js (Dashboard)
Dashboard initialization and statistics:
- Load statistics
- Recent payments
- Pending payment reminders

### students.js (StudentManager)
Student CRUD operations:
- Add/edit/delete students
- Search and filter
- Modal management

### fees.js (FeeManager)
Fee management system:
- Create and manage fees
- Fee status tracking
- Filter by class

### payments.js (PaymentManager)
Payment recording system:
- Record payments
- Update fee status
- Payment history

### reports.js (ReportManager)
Reporting and analytics:
- Multiple report types
- Invoice generation
- CSV export

### settings.js (SettingsManager)
System configuration:
- School settings
- Data backup/restore
- User management
- Fee categories

## Data Storage

All data is stored in browser localStorage under these keys:
- `users` - User accounts
- `students` - Student records
- `fees` - Fee information
- `payments` - Payment records
- `schoolSettings` - School configuration
- `currentUser` - Currently logged-in user (session)

## Features Detail

### Fee Status

- **Pending** - Fee not paid
- **Partial** - Partially paid
- **Paid** - Fully paid
- **Overdue** - Past due date and not paid

### Payment Methods

- Cash
- Check
- Bank Transfer
- Card
- Online Payment

### Report Types

1. **Fee Summary** - Fee type breakdown
2. **Student-wise** - Individual student status
3. **Class-wise** - Class-level analysis
4. **Monthly** - Time-based trends
5. **Overdue** - Late payment identification

## Limitations & Notes

- **Browser Storage Limit**: LocalStorage has ~5-10MB limit per domain
- **No Backend**: Data is not synced across devices
- **Single User**: Session-based, not multi-user aware
- **No Real Authentication**: For demo purposes only
- **No Encryption**: Passwords stored in plaintext

## Future Enhancements

- Backend database integration
- Email notifications
- SMS reminders
- Advanced permission system
- Multi-user support
- Data encryption
- Payment gateway integration
- Mobile app version
- Dark mode
- Multi-language support

## Browser Compatibility

- ✅ Chrome (Latest)
- ✅ Firefox (Latest)
- ✅ Safari (Latest)
- ✅ Edge (Latest)
- ✅ Opera (Latest)

## Tips & Best Practices

1. **Regular Backups**: Use Settings → Backup Data regularly
2. **Before Clearing Data**: Always backup first
3. **Password Management**: Change default admin password in settings
4. **Browser Tools**: Use browser DevTools to inspect localStorage
5. **Print Reports**: Generate and print reports to PDF for archival

## Troubleshooting

### Data Not Saving

1. Check if localStorage is enabled in browser
2. Check browser console for errors
3. Ensure cookies/storage is not blocked

### Page Not Loading

1. Ensure you're logged in
2. Check browser console for errors
3. Try clearing browser cache

### Missing Data

1. Check if you're on the correct page
2. Use filter/search functionality
3. Check localStorage in DevTools

## Performance Tips

1. Limit data entries for optimal performance
2. Archive old payment records periodically
3. Use date filters in reports
4. Clear browser cache if slow

## Support & Contact

For issues or feature requests, refer to the code comments or documentation.

## License

This system is provided as-is for educational and business purposes.

---

**Version:** 1.0  
**Last Updated:** March 2026  
**Created for:** School Management  
**Tech Stack:** HTML5, CSS3, JavaScript (Vanilla)
