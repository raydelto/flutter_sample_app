# Namer App

A Flutter application that generates random word pairs and allows users to favorite them. Built with the Provider pattern for state management.

## Features

- 🎲 Generate random English word pairs
- ❤️ Favorite word pairs you like
- 📋 View all favorited pairs in a dedicated page
- 🗑️ Remove favorites with a tap
- 🎨 Navigation rail for smooth page switching

## Screenshots

The app features two main pages:
- **Generator Page**: Display random word pairs with Like/Next buttons
- **Favorites Page**: List of all favorited word pairs

## Getting Started

### Prerequisites

- Flutter SDK 3.9.0 or higher
- Dart SDK (included with Flutter)

### Installation

1. Clone the repository:
```powershell
git clone <repository-url>
cd flutter_namer_app
```

2. Install dependencies:
```powershell
flutter pub get
```

3. Run the app:
```powershell
flutter run
```

## Development

### Project Structure

```
lib/
  └── main.dart          # Main application code
test/
  └── widget_test.dart   # Widget tests
```

### Key Components

- **MyAppState**: State management using ChangeNotifier
- **MyHomePage**: Main layout with navigation rail
- **GeneratorPage**: Word pair generator interface
- **FavoritesPage**: Favorites list interface
- **BigCard**: Reusable word pair display widget

### Running Tests

```powershell
flutter test
```

### Code Analysis

```powershell
flutter analyze
```

### Code Formatting

```powershell
flutter format lib test
```

## Dependencies

- **provider**: ^6.1.5 - State management
- **english_words**: ^4.0.0 - Random word pair generation
- **flutter_lints**: ^6.0.0 - Linting rules

## Platform Support

- ✅ Android
- ✅ iOS
- ✅ Web
- ✅ Windows
- ✅ Linux
- ✅ macOS

## License

This project is open source and available under the [MIT License](LICENSE).
