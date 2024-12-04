# Voice to Image Generator

A web application that converts voice input into high-definition images using AI technology. This project combines speech recognition with state-of-the-art image generation models to create images from spoken descriptions.

## Features

- 🎤 Real-time voice recording and transcription
- 🖼️ AI-powered image generation using Stable Diffusion
- 🔐 Secure user authentication system
- 📱 Responsive web interface
- 🔄 Image generation history tracking
- ⚡ Fast and efficient API responses

## Tech Stack

### Frontend
- React.js
- Material-UI (MUI) for UI components
- Web Speech API for voice recognition
- Axios for API communication
- JWT for authentication

### Backend
- Flask (Python)
- SQLAlchemy for database management
- Flask-JWT-Extended for JWT authentication
- Hugging Face API integration
- PostgreSQL database

## Prerequisites

- Python 3.8+
- Node.js 14+
- PostgreSQL
- Hugging Face API token

## Installation

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Copy .env.example to .env and configure:
   ```bash
   cp .env.example .env
   ```
   Set your Hugging Face API token and database credentials.

5. Initialize the database:
   ```bash
   flask db upgrade
   ```

6. Run the backend server:
   ```bash
   flask run
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Copy .env.example to .env:
   ```bash
   cp .env.example .env
   ```

4. Start the development server:
   ```bash
   npm start
   ```

## Environment Variables

### Backend (.env)
- `FLASK_APP`: Flask application entry point
- `FLASK_ENV`: Development/production environment
- `DATABASE_URL`: PostgreSQL database URL
- `JWT_SECRET_KEY`: Secret key for JWT tokens
- `HUGGING_FACE_TOKEN`: Your Hugging Face API token

### Frontend (.env)
- `REACT_APP_API_URL`: Backend API URL
- `REACT_APP_JWT_SECRET`: JWT secret key (must match backend)

## API Endpoints

### Authentication
- `POST /api/auth/register`: User registration
- `POST /api/auth/login`: User login
- `POST /api/auth/logout`: User logout

### Image Generation
- `POST /api/image/generate`: Generate image from voice input
- `GET /api/image/history`: Get user's image generation history

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Hugging Face for providing the Stable Diffusion model
- Material-UI team for the excellent React components
- Web Speech API for voice recognition capabilities
