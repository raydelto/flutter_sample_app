# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview
A Flutter application that generates random word pairs using the Provider pattern for state management. Users can favorite word pairs and view them in a separate page with navigation rail-based navigation.

## Development Commands

### Running the App
```powershell
flutter run
```

### Testing
```powershell
# Run all tests
flutter test

# Run a specific test file
flutter test test/widget_test.dart
```

### Code Quality
```powershell
# Analyze code for issues
flutter analyze

# Format code
flutter format lib test
```

### Dependencies
```powershell
# Get dependencies
flutter pub get

# Update dependencies
flutter pub upgrade
```

### Build
```powershell
# Build for specific platform
flutter build windows
flutter build apk
flutter build ios
```

## Architecture

### State Management
- **Provider Pattern**: Uses `ChangeNotifierProvider` for app-wide state management
- **MyAppState**: Central state class that extends `ChangeNotifier`
  - Manages current word pair and favorites list
  - Notifies listeners on state changes via `notifyListeners()`
  - Contains business logic for toggling favorites and generating new words

### Widget Structure
- **MyApp**: Root widget that sets up `ChangeNotifierProvider` and `MaterialApp`
- **MyHomePage**: Stateful widget managing navigation between pages via `NavigationRail`
- **GeneratorPage**: Displays current word pair with like/next actions
- **FavoritesPage**: Displays list of favorited word pairs with removal capability
- **BigCard**: Reusable presentational component for displaying word pairs

### Data Flow
1. User interactions trigger methods in `MyAppState`
2. `MyAppState` updates internal state and calls `notifyListeners()`
3. Widgets watching the state via `context.watch<MyAppState>()` rebuild automatically
4. UI updates reflect the new state

## Code Style
Based on `analysis_options.yaml`, this project:
- Allows `print` statements for debugging
- Does not enforce `const` constructors throughout
- Does not require keys in widget constructors
- Uses `flutter_lints` package for base linting rules

## Dependencies
- **provider**: State management solution
- **english_words**: Generates random English word pairs
- **flutter_lints**: Linting rules for Flutter projects
