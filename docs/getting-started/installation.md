# Installation Guide

This guide will help you install and set up the AI Moderation Project on your system.

## Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.8 or higher
- pip (Python package manager)
- Git
- Docker (optional, for containerized deployment)

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/ai-moderation-project.git
cd ai-moderation-project
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the project root:

```bash
cp .env.example .env
```

Edit the `.env` file with your configuration:

```env
API_KEY=your_api_key_here
MODEL_PATH=/path/to/model
DATABASE_URL=your_database_url
```

### 5. Initialize the Database

```bash
python manage.py init_db
```

## Docker Installation (Optional)

If you prefer using Docker:

```bash
docker build -t ai-moderation .
docker run -p 8000:8000 ai-moderation
```

## Verification

To verify your installation:

1. Start the server:
```bash
python manage.py runserver
```

2. Visit `http://localhost:8000/health` in your browser
3. You should see a success message

## Next Steps

- [Quick Start Guide](quick-start.md)
- [Configuration Guide](configuration.md)
- [Troubleshooting](troubleshooting.md) 