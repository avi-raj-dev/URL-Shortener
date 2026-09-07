# URL Shortener

A full-stack web application to create short, easy-to-share URLs from long URLs.

## Features
- Shorten any valid URL
- Responsive layout for desktop and mobile
- View list of shortened links (persisted in browser)
- One-click copy to clipboard
- Input validation with error messages

## Tech Stack
- **Frontend:** React.js, Tailwind CSS, HTML5, CSS3
- **Backend:** Node.js, Express.js
- **Database:** MongoDB
- **Other:** nanoid for short ID generation

## Project Structure
```
URL-Shortener/
├── client/   # React frontend
├── server/   # Express backend
├── install.sh
└── run.sh
```

## Getting Started

### Prerequisites
- Node.js (v16+)
- MongoDB (local or Atlas)

### Installation
```bash
# Clone the repo
git clone https://github.com/avi-raj-dev/URL-Shortener.git
cd URL-Shortener

# Install dependencies
chmod +x install.sh
./install.sh
# or manually:
# cd server && npm install
# cd ../client && npm install
```

### Environment Variables
Create `.env` in `server/`:
```
MONGO_URI=your_mongodb_connection_string
BASE_URL=http://localhost:5000
PORT=5000
```

Create `.env` in `client/` if needed:
```
REACT_APP_API_URL=http://localhost:5000
```

### Run
```bash
chmod +x run.sh
./run.sh
# or manually:
# cd server && npm run dev
# cd client && npm start
```

## API Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/shorten | Create short URL |
| GET | /:shortId | Redirect to original URL |

## License
ISC
