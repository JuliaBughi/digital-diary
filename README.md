# Digital Diary

A web application designed to help users organize, preserve, and share their digital memories. It allows users to upload personal content such as photos, videos, documents, and texts, organizing them chronologically and thematically.

## Features

- **Digital Archive:** Store and organize personal memories and multimedia content.
- **SIP Ingestion:** Upload ZIP packages containing a JSON manifest and associated files, with automatic validation and storage.
- **Timeline & Search:** Browse public content through chronological timelines, filters, and text search.
- **Content Management:** Create, edit, delete, and manage archived items.
- **Access Control:** Different user roles — Administrator, Producer, and Consumer.
- **Comments & Tags:** Add comments and categorize content using predefined classifications.
- **SIP/DIP Export:** Export archived resources as downloadable ZIP packages.
- **Administration Dashboard:** Manage users, content, news, logs, and usage statistics.
- **Authentication:** Local authentication and Google OAuth integration.

## Technologies

- **Backend:** Node.js, Express.js
- **Database:** MongoDB, Mongoose
- **Authentication:** Passport.js, Google OAuth
- **Frontend:** Pug, JavaScript, Bootstrap, CSS3
- **Deployment:** Docker, Docker Compose

## Project Structure

```text
digital-diary/
├── apiDados/    # REST API, authentication, models and controllers
├── UI/          # Frontend application and views
└── DBs/         # Database-related JSON files
```

## Getting Started

Clone the repository:

```bash
git clone https://github.com/JuliaBughi/digital-diary.git
cd digital-diary
```

Install dependencies in both application directories:

```bash
cd apiDados && npm install
cd ../UI && npm install
```

Configure the required environment variables, including MongoDB connection details and authentication credentials, then start the backend and frontend applications.

## SIP Format

The application uses **Submission Information Packages (SIP)** for content ingestion. Each ZIP package contains a `manifesto-SIP.json` file describing the resource and its associated files.

After validation, metadata is stored in MongoDB and uploaded files are stored on the server. Archived resources can later be exported as **Dissemination Information Packages (DIP)** in ZIP format.
