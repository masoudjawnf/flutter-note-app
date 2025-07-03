# flutter-note-app
A simple Flutter note-taking app with local SQLite storage. Create, Edit, and delete your notes easily with a clean UI.

# 📝 Flutter Note-Taking App

A simple and clean note-taking application built with Flutter and Dart. This app allows users to add, update, and delete personal notes. The data is stored locally using SQLite.

## 📱 Features

- Add new notes with title and content
- Edit existing notes
- Delete unwanted notes
- Simple and minimal user interface
- Local data storage using SQLite

## 🛠️ Tech Stack

- **Flutter** (UI Toolkit)
- **Dart** (Programming Language)
- **SQLite** (Local Database using sqflite package)

## 📁 Project Structure

The main Dart files used in this project:

### `main.dart`

The entry point of the app. It initializes the main UI and routes to the `NotePage`.

### `note_page.dart`

This is the main screen of the app that displays the list of notes. It handles:
- Fetching notes from the database
- Displaying them in a `ListView`
- Adding or updating notes through a dialog
- Deleting notes with a delete button

### `note.dart`

A simple `Note` model class that represents a note item with an optional `id`, a `title`, and `content`. It also includes:
- `toMap()` method for converting the object to a Map for SQLite
- `fromMap()` factory constructor for reconstructing a Note from a Map

### `database_helper.dart`

Handles all database operations including:
- Initializing and creating the database
- Inserting new notes
- Reading all notes
- Updating existing notes
- Deleting notes

✅ **Important:**  
These Dart files are part of a complete Flutter project. Make sure to place them in the proper directories within your Flutter project (e.g., inside `lib/`).

## 📦 Dependencies

Add the following dependency to your `pubspec.yaml`:

```yaml
dependencies:
  flutter:
    sdk: flutter
  sqflite: ^2.0.0+3
  path: ^1.8.0
