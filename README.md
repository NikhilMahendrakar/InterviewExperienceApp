# Interview Experience App

This Flutter application showcases interview experiences, including videos and PDF resumes. It leverages Firebase for data storage and retrieval, and various Flutter plugins for handling video playback and PDF viewing.

## Introduction

This application provides a platform to display interview experiences of various individuals. Users can view profiles, watch interview videos, and read resumes in PDF format. The app is built with Flutter and integrates Firebase for real-time data handling.

## Features

- **Profile Display**: Showcases detailed profiles of individuals, including name, age, city, work, designation, and a profile picture.
- **Video Playback**: Embedded videos of interview experiences using the `chewie` and `video_player` plugins.
- **PDF Viewing**: Displays resumes in PDF format using the `flutter_plugin_pdf_viewer`.
- **Firebase Integration**: Fetches profile data, videos, and PDFs from Firebase Firestore.

## Installation

To run this project locally, follow these steps:

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/interview_experience_app.git
    cd interview_experience_app
    ```

2. **Install Flutter**: If you haven't already, install Flutter by following the instructions on the [official Flutter website](https://flutter.dev/docs/get-started/install).

3. **Install dependencies**:
    ```sh
    flutter pub get
    ```

4. **Set up Firebase**:
    - Create a Firebase project in the [Firebase Console](https://console.firebase.google.com/).
    - Add an Android/iOS app to your Firebase project and follow the setup instructions to download the `google-services.json` or `GoogleService-Info.plist` file.
    - Place the `google-services.json` file in the `android/app` directory for Android, and the `GoogleService-Info.plist` file in the `ios/Runner` directory for iOS.

5. **Run the application**:
    ```sh
    flutter run
    ```

## Usage

1. **Home Page**: Displays a list of profiles fetched from Firebase Firestore.
2. **Profile Page**: Shows detailed information about the selected profile, including an embedded interview video and PDF resume.

### Adding a Profile

1. Add a new document to the `Posts` collection in Firebase Firestore with the following fields:
    - `name`: String
    - `age`: String
    - `city`: String
    - `work`: String
    - `designation`: String
    - `link`: String (URL to LinkedIn profile)
    - `imageurl`: String (URL to profile image)
    - `videourl`: String (URL to interview video)
    - `pdfurl`: String (URL to resume PDF)


### Main Files

- `main.dart`: Entry point of the application. Initializes Firebase and sets up the home page.
- `chewie_item.dart`: Contains the widget for video playback using `chewie` and `video_player`.
- `profile.dart`: Displays detailed profile information including video and PDF resume.
- `pdfview.dart`: Contains the widget for viewing PDF files.
- `productbox.dart`: Defines the widget for displaying profile summary in the list.

## Contributing

Contributions are welcome! If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Feel free to adjust any section as needed. This README file provides a comprehensive overview of the project, including installation steps, usage instructions, and a brief description of the main files and features.



