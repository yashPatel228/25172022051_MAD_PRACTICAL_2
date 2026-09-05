# Android Activity Life Cycle and Basic UI

![Android](https://img.shields.io/badge/Platform-Android-green)
![Language](https://img.shields.io/badge/Language-Kotlin-blue)
![UI](https://img.shields.io/badge/UI-XML-orange)
![IDE](https://img.shields.io/badge/IDE-Android%20Studio-lightgrey)

A basic Android application developed using **Kotlin and XML** to demonstrate the **Activity Life Cycle** and **Basic User Interface**. 

The application displays **"Hello World"** in the center of the screen and demonstrates Activity Life Cycle methods using **Logcat, Toast, and Snackbar messages**.

---

## 📌 Practical Information

| Field                      | Details                                  |
| -------------------------- | ---------------------------------------- |
| **Subject**                | Mobile Application Development           |
| **Practical No.**          | 2                                        |
| **Practical Title**        | Android Activity Life Cycle and Basic UI |
| **Student Enrollment No.** | 25172022051                              |
| **Programming Language**   | Kotlin                                   |
| **UI Technology**          | XML                                      |
| **Development Tool**       | Android Studio                           |

---

## 🎯 Aim

To create an Android application that demonstrates the functions of **Activity Life Cycle** and **Basic UI**.

---

## 📖 Introduction

An **Activity** is one of the fundamental components of an Android application. It represents a single screen with a user interface.

The **Activity Life Cycle** describes the different states through which an Activity passes during its lifetime.

This practical demonstrates the following Activity Life Cycle methods:

* `onCreate()`
* `onStart()`
* `onResume()`
* `onPause()`
* `onStop()`
* `onRestart()`
* `onDestroy()`

The application also demonstrates:

* TextView
* ConstraintLayout
* Toast Message
* Snackbar Message
* Logcat
* Android built-in colors

---

## 🛠️ Technologies Used

* **Android Studio**
* **Kotlin**
* **XML**
* **Android SDK**
* **ConstraintLayout**
* **TextView**
* **Toast**
* **Snackbar**
* **Logcat**
* **Activity Life Cycle**

---

## ✨ Features

* Displays **Hello World** in the center of the screen.
* Uses a **yellow background**.
* Displays text in **blue color**.
* Uses **bold and italic** text style.
* Demonstrates all major Activity Life Cycle methods.
* Displays lifecycle messages using **Logcat**.
* Displays lifecycle messages using **Toast**.
* Displays lifecycle messages using **Snackbar**.
* Uses **Edge-to-Edge** layout support.
* Uses **WindowInsetsCompat** for system bar handling.

---

## 🎨 User Interface Requirements

The application contains a `TextView` with the following properties:

| Property             | Value                             |         |
| -------------------- | --------------------------------- | ------- |
| **Text**             | `Hello World`                     |         |
| **Text Color**       | `@android:color/holo_blue_bright` |         |
| **Text Size**        | `27sp`                            |         |
| **Text Style**       | `bold                             | italic` |
| **Background Color** | `#FFFF00`                         |         |
| **Position**         | Center of Activity                |         |
| **Layout**           | ConstraintLayout                  |         |

---

## 🖼️ Application UI

The application screen contains:

* A yellow background.
* A centered TextView.
* Blue-colored text.
* Bold and italic text.
* Text size of 27sp.

### Example UI

```text
┌──────────────────────────────┐
│                              │
│                              │
│         Hello World          │
│                              │
│                              │
└──────────────────────────────┘
```

---

## 🔄 Activity Life Cycle

The Activity Life Cycle consists of the following important methods:

### 1. onCreate()

`onCreate()` is called when the Activity is created.

It is generally used to:

* Initialize the Activity.
* Set the layout.
* Initialize UI components.
* Perform initial setup.

Example:

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_main)
}
```

---

### 2. onStart()

`onStart()` is called when the Activity becomes visible to the user.

```kotlin
override fun onStart() {
    super.onStart()
}
```

---

### 3. onResume()

`onResume()` is called when the Activity comes into the foreground and becomes interactive.

```kotlin
override fun onResume() {
    super.onResume()
}
```

---

### 4. onPause()

`onPause()` is called when the Activity is partially losing focus.

```kotlin
override fun onPause() {
    super.onPause()
}
```

---

### 5. onStop()

`onStop()` is called when the Activity is no longer visible to the user.

```kotlin
override fun onStop() {
    super.onStop()
}
```

---

### 6. onRestart()

`onRestart()` is called when a stopped Activity is about to start again.

```kotlin
override fun onRestart() {
    super.onRestart()
}
```

---

### 7. onDestroy()

`onDestroy()` is called before the Activity is destroyed.

```kotlin
override fun onDestroy() {
    super.onDestroy()
}
```

---

## 🔁 Activity Life Cycle Flow

```text
             onCreate()
                 ↓
              onStart()
                 ↓
             onResume()
                 ↓
          Activity Running
                 ↓
              onPause()
                 ↓
               onStop()
                 ↓
             onRestart()
                 ↓
              onStart()
                 ↓
             onResume()
```

### When Activity is Permanently Closed

```text
onPause()
    ↓
onStop()
    ↓
onDestroy()
```

> **Note:** The exact lifecycle sequence may vary depending on the operation performed and Android system behavior.

---

## 📝 Logcat Message

**Logcat** is used to display Activity Life Cycle events in Android Studio.

The application uses:

```kotlin
Log.i("MainActivity", message)
```

Example output:

```text
I/MainActivity: onCreate function called.
I/MainActivity: onStart function called.
I/MainActivity: onResume function called.
```

### How to View Logcat

1. Open the project in Android Studio.
2. Run the application.
3. Open the **Logcat** window.
4. Search for:

```text
MainActivity
```

5. Observe the lifecycle messages.

---

## 📱 Toast Message

A **Toast** displays a short message to the user.

The application uses:

```kotlin
Toast.makeText(this, message, Toast.LENGTH_SHORT).show()
```

Example:

```text
onCreate function called.
```

Toast messages are useful for displaying short notifications.

---

## 💬 Snackbar Message

A **Snackbar** displays a short message at the bottom of the screen.

The application uses:

```kotlin
Snackbar.make(rootView, message, Snackbar.LENGTH_SHORT).show()
```

Example:

```text
onResume function called.
```

Snackbar messages are useful for displaying temporary information to the user.

---

## 📂 Project Structure

```text
25172022051_MAD_PRACTICAL_2/
│
├── .idea/
│
├── app/
│   └── src/
│       └── main/
│           │
│           ├── java/
│           │   └── com/
│           │       └── example/
│           │           └── a25172022051_MAD_PRACTICAL_2/
│           │               └── MainActivity.kt
│           │
│           ├── res/
│           │   └── layout/
│           │       └── activity_main.xml
│           │
│           └── AndroidManifest.xml
│
├── gradle/
│
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
├── gradlew
├── gradlew.bat
└── README.md
```

---

## 📄 MainActivity.kt Responsibilities

`MainActivity.kt` is responsible for:

* Initializing the Activity.
* Connecting the XML layout with the Activity.
* Implementing Activity Life Cycle methods.
* Printing lifecycle messages in Logcat.
* Displaying Toast messages.
* Displaying Snackbar messages.
* Handling Window Insets.

---

## 📄 activity_main.xml Responsibilities

`activity_main.xml` is responsible for:

* Creating the ConstraintLayout.
* Setting the yellow background.
* Creating the TextView.
* Positioning the TextView at the center.
* Setting TextView properties.

---

## 🧩 ConstraintLayout

`ConstraintLayout` is used to position UI elements using constraints.

To place the TextView at the center, constraints are applied to all four sides:

```xml
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintEnd_toEndOf="parent"
```

This ensures that the TextView remains centered inside the layout.

---

## 🆔 View ID

Every UI component should have a unique ID so that it can be accessed from Kotlin code.

Example:

```xml
android:id="@+id/textView"
```

The `+id` creates a new ID for the TextView.

The root layout uses:

```xml
android:id="@+id/mainLayout"
```

This ID is used in `MainActivity.kt` to apply Window Insets.

---

## ⚙️ Edge-to-Edge Support

The application uses:

```kotlin
enableEdgeToEdge()
```

This allows the application content to extend behind the system bars.

The application also uses:

```kotlin
ViewCompat.setOnApplyWindowInsetsListener(...)
```

to apply the required system bar padding.

This helps prevent UI elements from overlapping with the status bar and navigation bar.

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/yashPatel228/25172022051_MAD_PRACTICAL_2.git
```

### Step 2: Open the Project

Open the cloned project in **Android Studio**.

### Step 3: Wait for Gradle Sync

Allow Android Studio to complete the Gradle synchronization.

### Step 4: Connect a Device

Connect an Android device using USB debugging or start an Android Emulator.

### Step 5: Run the Application

Click the **Run ▶️** button in Android Studio.

### Step 6: Observe the Output

The application will display:

```text
Hello World
```

in the center of the screen.

### Step 7: Check Lifecycle Messages

Open **Logcat** and search for:

```text
MainActivity
```

### Step 8: Test Lifecycle Methods

Perform operations such as:

* Opening the application.
* Minimizing the application.
* Returning to the application.
* Rotating the device.
* Closing the application.

Observe the lifecycle messages.

---

## 📊 Expected Output

### Initial Launch

```text
onCreate function called.
onStart function called.
onResume function called.
```

### When App Goes to Background

```text
onPause function called.
onStop function called.
```

### When App Returns to Foreground

```text
onRestart function called.
onStart function called.
onResume function called.
```

### When Activity is Destroyed

```text
onPause function called.
onStop function called.
onDestroy function called.
```

> **Note:** Lifecycle callbacks are controlled by Android. The exact order may differ depending on the device, Android version, and operation performed.

---

## 🧪 Testing

The application can be tested using the following operations:

| Test Case                 | Expected Result                                 |
| ------------------------- | ----------------------------------------------- |
| Open the application      | `onCreate`, `onStart`, and `onResume` messages  |
| Minimize the application  | `onPause` and `onStop` messages                 |
| Return to the application | `onRestart`, `onStart`, and `onResume` messages |
| Rotate the device         | Lifecycle messages may be triggered             |
| Close the Activity        | `onPause`, `onStop`, and possibly `onDestroy`   |
| Check Logcat              | Lifecycle messages are displayed                |
| Check Toast               | Short lifecycle messages are displayed          |
| Check Snackbar            | Messages appear at the bottom of the screen     |

---

## 🎓 Study / Viva Questions

### 1. What is an Activity?

An Activity is a component of an Android application that represents a single screen with a user interface.

### 2. What is Activity Life Cycle?

Activity Life Cycle is the sequence of states through which an Activity passes during its lifetime.

### 3. What is onCreate()?

`onCreate()` is called when the Activity is created.

### 4. What is onStart()?

`onStart()` is called when the Activity becomes visible.

### 5. What is onResume()?

`onResume()` is called when the Activity becomes interactive.

### 6. What is onPause()?

`onPause()` is called when the Activity is partially losing focus.

### 7. What is onStop()?

`onStop()` is called when the Activity is no longer visible.

### 8. What is onRestart()?

`onRestart()` is called when a stopped Activity is about to start again.

### 9. What is onDestroy()?

`onDestroy()` is called before the Activity is destroyed.

### 10. What is Toast?

Toast is a small temporary message displayed to the user.

### 11. What is Snackbar?

Snackbar is a temporary message displayed at the bottom of the screen.

### 12. What is Logcat?

Logcat is a tool in Android Studio used to view application logs.

### 13. What is ConstraintLayout?

ConstraintLayout is a layout used to position UI elements using constraints.

### 14. What is TextView?

TextView is an Android UI component used to display text.

### 15. What is Edge-to-Edge?

Edge-to-Edge allows application content to extend behind the system bars.

---

## 📚 Learning Outcomes

After completing this practical, students will understand:

* How to create a basic Android UI.
* How to use TextView properties.
* How to use Android built-in colors.
* How to use ConstraintLayout.
* How to generate and use View IDs.
* How Activity Life Cycle methods work.
* How to display Toast messages.
* How to display Snackbar messages.
* How to print messages in Logcat.
* How to handle Window Insets.

---

## ✅ Conclusion

This practical demonstrates the **basic Android UI** and the **complete Activity Life Cycle**.

It shows how **TextView, ConstraintLayout, Toast, Snackbar, Logcat, and Activity Life Cycle methods** work together in an Android application.

Through this practical, students learn how an Android Activity is created, started, resumed, paused, stopped, restarted, and destroyed.

---

## 👨‍💻 Author

**Yash Patel**

**Enrollment No.:** 25172022051

**Subject:** Mobile Application Development

---

## 📌 Repository

This project is available on GitHub:

[25172022051_MAD_PRACTICAL_2](https://github.com/yashPatel228/25172022051_MAD_PRACTICAL_2)

---

## 📄 License

This project is created for **educational and practical purposes**.
