# Holidate - Holiday Management System

A comprehensive web application for managing employee holidays, time-off requests, and team scheduling. Built with Django and designed for efficient workplace holiday management.

## Features

- **Holiday Management**: View used and upcoming holidays/breakdays
- **Request System**: Submit, approve, cancel, and update time-off requests
- **Role-based Access**: Separate interfaces for employees and managers
- **Calendar Integration**: Schedule events in team Google calendars
- **Team Schedule**: View upcoming team schedules and availability
- **Email Notifications**: Automated email notifications for request status updates

## Technology Stack

### Backend
- **Django 1.9** - Web framework
- **PostgreSQL** - Database
- **Python** - Programming language

### Frontend
- **HTML5/CSS3** - Structure and styling
- **JavaScript** - Interactive functionality
- **Bootstrap** - Responsive UI framework
- **jQuery** - JavaScript library
- **FullCalendar** - Calendar component

### Third-party Integrations
- **Google Calendar API** - Calendar synchronization
- **Django Tables2** - Enhanced table displays
- **Bootstrap DateRangePicker** - Date selection

## Installation

### Prerequisites
- Python 3.x
- PostgreSQL
- pip (Python package manager)

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Holidate.git
   cd Holidate
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Database Setup**
   - Create a PostgreSQL database named `cal_data`
   - Update database credentials in `mysite/settings.py`
   - Run migrations:
     ```bash
     python manage.py migrate
     ```

5. **Google Calendar Integration (Optional)**
   - Place your `client_secret.json` file in the `timeline/` directory
   - Configure Google Calendar API credentials

6. **Create a superuser**
   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server**
   ```bash
   python manage.py runserver
   ```

8. **Access the application**
   - Open your browser and navigate to `http://127.0.0.1:8000/`

## Configuration

### Environment Variables
Create a `.env` file in the project root and configure:

```env
SECRET_KEY=your-secret-key-here
DEBUG=True
DB_NAME=cal_data
DB_USER=postgres
DB_PASSWORD=your-password
DB_HOST=localhost
DB_PORT=5432
EMAIL_HOST=your-email-host
EMAIL_USER=your-email-username
EMAIL_PASSWORD=your-email-password
```

### Settings
Key configuration files:
- `mysite/settings.py` - Main Django settings
- `timeline/client_secret.json` - Google Calendar API credentials

## Usage

### For Employees
- Log in to view personal holiday calendar
- Submit time-off requests
- View request status and history
- Access team calendar

### For Managers
- Review and approve/deny employee requests
- View team-wide holiday schedules
- Manage employee records
- Schedule team events

## Project Structure

```
Holidate/
├── manage.py                 # Django management script
├── mysite/                   # Main project directory
│   ├── settings.py          # Django settings
│   ├── urls.py              # URL routing
│   └── wsgi.py              # WSGI configuration
├── timeline/                 # Main application
│   ├── models.py            # Database models
│   ├── views.py             # View logic
│   ├── forms.py             # Django forms
│   ├── urls.py              # App URL routing
│   ├── templates/           # HTML templates
│   └── static/              # CSS, JS, images
└── requirements.txt         # Python dependencies
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Development History

Originally developed by Jason Lee in 2017 during a summer internship at Coinplug, Inc (South Korea). The application was designed to create an organized system for managing employee holidays and time-off requests in a corporate environment.

## Support

For support, please open an issue on GitHub or contact the development team.

---

**Note**: This application was built with Django 1.9. For production deployment, consider upgrading to a more recent version of Django and review security settings.