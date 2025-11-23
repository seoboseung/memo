# Memo App

A simple and lightweight memo application for Android developed with Android Studio.

## Overview

This is a basic memo application that allows users to create, view, edit, and manage their notes efficiently. The app uses SharedPreferences with JSON format for local data storage, making it simple and fast without requiring external database dependencies.

## Features

- ✏️ **Create Memos**: Write new memos with title and content
- 📋 **View Memos**: Browse all saved memos in a list view
- ✨ **Edit Memos**: Update existing memos
- 🗑️ **Delete Memos**: Remove unwanted memos
- 💾 **Auto-save**: Memos are automatically saved locally using SharedPreferences
- 📱 **Material Design**: Clean and intuitive user interface following Material Design guidelines

## Technical Specifications

- **Language**: Java
- **Minimum SDK**: API 21 (Android 5.0 Lollipop)
- **Target SDK**: API 31 (Android 12)
- **Build Tool**: Gradle 7.0.3
- **UI Components**: RecyclerView, Material Components
- **Data Storage**: SharedPreferences with JSON format

## Dependencies

```gradle
implementation 'androidx.appcompat:appcompat:1.4.0'
implementation 'com.google.android.material:material:1.4.0'
implementation 'androidx.constraintlayout:constraintlayout:2.1.2'
implementation 'androidx.recyclerview:recyclerview:1.2.0'
```

## Installation

### Prerequisites
- Android Studio (Arctic Fox or later)
- JDK 8 or higher
- Android SDK with API 31

### Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/seoboseung/memo.git
   ```

2. Open the project in Android Studio

3. Wait for Gradle to sync and download dependencies

4. Build the project:
   - From menu: `Build > Make Project`
   - Or press `Ctrl+F9` (Windows/Linux) / `Cmd+F9` (Mac)

5. Run the app:
   - Connect an Android device or start an emulator
   - Click the Run button or press `Shift+F10` (Windows/Linux) / `Ctrl+R` (Mac)

## Usage

### Creating a New Memo
1. Tap the `+` button on the main screen
2. Enter the memo title
3. Enter the memo content
4. Tap the checkmark button to save

### Viewing Memos
- All saved memos are displayed on the main screen in a list format
- Each memo shows the title and a preview of the content
- Tap on any memo to view its full content

### Editing a Memo
1. Tap on a memo to view it
2. Modify the title or content as needed
3. Tap the save button to update the memo

### Deleting a Memo
- Open a memo and use the delete option to remove it

## Project Structure

```
app/src/main/java/com/example/memo/
├── MainActivity.java          # Main screen with memo list
├── Add.java                   # Activity for creating new memos
├── ViewActivity.java          # Activity for viewing memo details
├── ReWriteActivity.java       # Activity for editing memos
├── MainAdapter.java           # RecyclerView adapter for memo list
├── MemoItem.java              # Data model for memo items
├── PreferenceManager.java     # Helper for SharedPreferences operations
└── CancelPopup.java          # Popup dialog for confirmation
```

## Data Storage

Memos are stored locally using Android's SharedPreferences with the following structure:
- **Key**: Timestamp (ensures unique identifier)
- **Value**: JSON object containing:
  ```json
  {
    "title": "Memo title",
    "content": "Memo content"
  }
  ```

## License

This project is available for educational and personal use.

## Contributing

Contributions, issues, and feature requests are welcome!

## Author

seoboseung

---

Built with ❤️ using Android Studio
