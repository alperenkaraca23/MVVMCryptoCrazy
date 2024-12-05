 
```markdown
# Crypto Price Tracker

Crypto Price Tracker is a modern iOS application designed to display the current prices of cryptocurrencies. The project showcases industry-standard technologies and architectural patterns such as **MVVM** and **RxSwift** to ensure scalability, maintainability, and responsiveness.

## Features

- **Real-Time Data**: Fetches and displays live cryptocurrency prices from a JSON API.
- **Reactive Programming**: Utilizes **RxSwift** for efficient data binding and UI updates.
- **MVVM Architecture**: Ensures a clean codebase by separating concerns:
  - **Model**: Handles data structures for cryptocurrencies.
  - **ViewModel**: Manages data transformations and logic.
  - **View**: Subscribes to data streams and updates the UI dynamically.
- **Custom Web Service**: Implements a web service to handle API requests and parse JSON responses.
- **Publish-Subscribe Mechanism**: Uses RxSwift to publish data from the ViewModel and subscribe in the View.

## How It Works

1. **Data Fetching**:
   - Fetches cryptocurrency price data from an external JSON API using `URLSession`.
   - Parses the data into models for easy handling.

2. **MVVM Implementation**:
   - **Model**:
     - Defines the structure of cryptocurrency data (e.g., name, price).
   - **ViewModel**:
     - Uses RxSwift’s `PublishSubject` to publish data streams.
     - Transforms and filters data for the View.
   - **View**:
     - Subscribes to the ViewModel’s data streams using RxSwift.
     - Dynamically updates the UI when new data is published.

3. **RxSwift in Action**:
   - Handles asynchronous data streams for fetching and displaying data.
   - Simplifies managing user interactions and state changes.

4. **UI Updates**:
   - Displays cryptocurrency data in a user-friendly format.
   - Automatically updates the View when new data is received.

## Technologies Used

- **Swift**: Programming language for iOS development.
- **RxSwift**: For reactive programming, enabling efficient data flow and UI updates.
- **MVVM Architecture**: To improve code organization and testability.
- **URLSession**: For network requests to fetch JSON data.
- **Swift Package Manager (SPM)**: Used for integrating RxSwift and other dependencies.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/alperenkaraca23/MVVMCryptoCrazy.git
   cd MVVMCryptoCrazy
   ```

2. Open the project in Xcode:
   ```bash
   open MVVMCryptoCrazy.xcodeproj
   ```

3. Ensure dependencies are installed using Swift Package Manager:
   - Navigate to **File > Swift Packages > Add Package Dependency**.
   - Add the RxSwift package by entering the following URL:
     ```
     https://github.com/ReactiveX/RxSwift.git
     ```

4. Run the project on a simulator or physical device.

## Video Demo

https://github.com/user-attachments/assets/3784c128-2076-46a4-b0b0-86765c0f9081

## Folder Structure

```
CryptoPriceTracker/
├── Models/
│   ├── Crypto.swift        # Data model for cryptocurrencies
├── ViewModels/
│   ├── CryptoViewModel.swift # Handles business logic and data transformations
├── Views/
│   ├── ViewController.swift # Displays cryptocurrency data
├── Services/
│   ├── WebService.swift     # Handles API requests and JSON parsing
```
