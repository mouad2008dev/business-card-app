# Business Card Application

This repository contains an Android application built using **Jetpack Compose**. The app demonstrates the creation of a digital business card with portfolio information. Below, you'll find details about the features, structure, and usage of the app.

---

## Features

- **Business Card Layout**: Displays profile information, including a profile picture, name, profession, and a clickable button to view the portfolio.
- **Portfolio Section**: Dynamically displays a list of projects in a scrollable format.
- **Responsive Design**: Uses Jetpack Compose to create a modern, visually appealing, and adaptable UI.

---

## Code Structure

### 1. `MainActivity.kt`
The main entry point of the app:
- Initializes the app's theme and sets the content to display the business card using `CreateBusCard()`.

### 2. Composables

#### `CreateBusCard()`
- Creates the main surface that holds the business card.
- Adds styling to the card using rounded corners and elevation.
- Integrates the `info()` composable to display the user's information.

#### `info()`
- Displays profile details such as:
  - **Name**: "Miles P."
  - **Profession**: "Android Compose Programmer"
  - **Handle**: "@themilesCompose"
- Includes a button to toggle the portfolio section.

#### `Content()`
- A container for the portfolio section.
- Uses a `Surface` with rounded corners and a border.
- Calls the `Portfolio()` composable to display the list of projects.

#### `Portfolio(data: List<String>)`
- Dynamically generates a list of projects using `LazyColumn`.
- Each project is displayed in a card format with a title and description.

#### `CreateImageProfile()`
- Displays a circular profile image with a border and shadow.
- Uses `painterResource` to load a drawable resource (`R.drawable.user`).

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/business-card-app.git
   ```

2. Open the project in **Android Studio**.

3. Ensure you have the following:
   - Android SDK configured.
   - Jetpack Compose dependencies installed.

4. Add a profile picture:
   - Place an image file named `user.png` or `user.jpg` in the `res/drawable` folder.

5. Build and run the app on an emulator or physical device.

---

## Dependencies

This project uses the following:
- **Jetpack Compose**: Modern toolkit for building native Android UI.
- **Material 3 Components**: For theming and prebuilt UI components.

---

## App Flow

1. **Home Screen**: Displays the business card with a profile picture, name, profession, and a button.
2. **Portfolio Button**: Toggles the visibility of the portfolio section.
3. **Portfolio Section**: Lists various projects dynamically in a scrollable format.

---

## Customization

- To update the user details, modify the `info()` composable:
  ```kotlin
  Text(text = "Your Name")
  Text(text = "Your Profession")
  Text(text = "@YourHandle")
  ```

- To change the list of portfolio items, update the `data` parameter in the `Portfolio()` composable:
  ```kotlin
  Portfolio(data = listOf("New Project 1", "New Project 2"))
  ```

---

## License

This project is licensed under the MIT License. Feel free to use and modify it as you like.

---

## Contributions

Contributions are welcome! Feel free to open issues or submit pull requests.

---

## Contact

For any inquiries or feedback, please contact: `mouadomri91@gmail.com`.

