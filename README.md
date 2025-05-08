# MP-Exercise1
Mobile Programming - Exercise 1

# Simple Shoe Shop - Flutter Application

A modern Flutter application for showcasing and shopping for shoes, featuring a clean user interface with product browsing, detailed product views, and cart functionality.

## Project Overview

This application demonstrates a simple e-commerce flow for a shoe store with:
- Splash screen with introduction
- Product listing with grid layout
- Detailed product view with size and color selection
- Shopping cart functionality

## Screenshots
![Screenshot 2025-05-07 215559](https://github.com/user-attachments/assets/b13503e7-81d4-4cf0-9054-d68158622ab8)
![1746674109709](https://github.com/user-attachments/assets/1690cc13-dbbb-45e1-a229-3c24f02401d8)
![Screenshot 2025-05-07 215654](https://github.com/user-attachments/assets/01b665f1-8b44-4378-93b7-72fc0c365416)


## Requirements

- Flutter SDK (latest stable version recommended)
- Dart SDK (included with Flutter)
- Android Studio or VS Code with Flutter/Dart plugins
- Android Emulator or iOS Simulator
  - Recommended: Pixel 9 Pro emulator for Android

## Project Setup

### Environment Setup

1. Install Flutter by following the [official installation guide](https://flutter.dev/docs/get-started/install)
2. Set up your IDE:
   - For Android Studio: Install the Flutter and Dart plugins
   - For VS Code: Install the Flutter and Dart extensions

### Project Configuration

1. Clone this repository or download the source code
2. Open the project in your IDE
3. Run the following commands in the terminal:
   ```bash
   flutter pub get
   flutter doctor
   ```
4. Ensure all dependencies are resolved and your environment is properly set up

### Asset Configuration

Ensure your project has the following asset structure:
```
assets/
└── images/
    ├── air_jordan_1.png
    ├── air_jordan_11.png
    ├── air_max_90.png
    ├── green sneaker.png
    └── Nike_air_force.png
```

Update your `pubspec.yaml` file to include these assets:
```yaml
flutter:
  assets:
    - assets/images/
```

## Running the Application

### From Android Studio/IntelliJ IDEA:

1. Open the project in Android Studio/IntelliJ IDEA
2. Select your target device (Pixel 9 Pro emulator is recommended)
3. Click the 'Run' button or press `Shift+F10`

### From VS Code:

1. Open the project in VS Code
2. Select your target device from the status bar
3. Press `F5` or click "Run and Debug" from the sidebar

### From Command Line:

```bash
flutter run
```

## Project Structure

```
lib/
└── main.dart     # Main application entry point containing all components
```

### Key Components:

- **MyShopApp**: Main application widget that sets up the theme and root route
- **SplashScreen**: Initial welcome screen with gradient background and call-to-action
- **Product**: Model class for shoe product data
- **ProductListScreen**: Main shopping screen with product grid and shopping cart summary
- **ProductDetailScreen**: Detailed view of selected product with size/color selection
- **Cart**: Static class managing shopping cart functionality
- **CartScreen**: Shopping cart view with ability to remove items

## Architecture & Design

The application follows a simple structure where all components are contained within a single file for educational purposes. In a production environment, it would be recommended to separate these components into individual files with a proper folder structure.

### State Management

- The application uses Flutter's built-in `StatefulWidget` for local state management
- The `Cart` class uses static variables and methods to maintain the shopping cart state across screens

### UI Design

- The UI implements Material Design principles with custom styling
- A consistent color scheme is applied throughout the app (primarily orange and black)
- Custom button styles and card layouts enhance the visual appeal

## Customization

### Theming:

To change the application theme, modify the `ThemeData` in the `MyShopApp` class:

```dart
theme: ThemeData(
  primarySwatch: Colors.orange,  // Change to your preferred color
  // Other theme properties
),
```

### Product Data:

To add or modify products, update the `products` list:

```dart
List<Product> products = [
  Product(
    name: 'New Product Name',
    price: 199.99,
    imageUrl: 'assets/images/your_image.png',
  ),
  // Add more products
];
```

## Future Improvements

- Implement user authentication
- Add product search functionality
- Implement product filtering and categories
- Add payment processing
- Create a wishlist feature
- Improve state management with a dedicated solution (Provider, Bloc, etc.)
- Split code into multiple files for better maintainability

