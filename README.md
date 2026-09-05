# Android Activity Life Cycle and Basic UI

## AIM

Create an Android application to demonstrate the functions of **Activity Life Cycle** and **Basic UI**.

The application displays **"Hello World"** in a `TextView` at the center of the Activity screen. The Activity demonstrates all major Activity Life Cycle methods using **Log messages, Toast messages, and Snackbar messages**.

## Technologies Used

* Android Studio
* Kotlin
* XML
* Android SDK
* ConstraintLayout
* TextView
* Toast
* Snackbar
* Logcat
* Activity Life Cycle

## UI Requirements

The application contains a `TextView` with the following properties:

| Property   | Value                             |
| ---------- | --------------------------------- |
| Text       | `Hello World`                     |
| Text Color | `@android:color/holo_blue_bright` |
| Text Size  | `27sp`                            |
| Text Style | `bold\|italic`                    |
| Background | `#FFFF00`                         |
| Position   | Center of Activity                |
| Layout     | ConstraintLayout                  |

## TextView XML

The main `TextView` can be created using:

```xml id="u7q9ke"
<TextView
    android:id="@+id/textView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Hello World"
    android:textColor="@android:color/holo_blue_bright"
    android:textSize="27sp"
    android:textStyle="bold|italic"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />
```

## Background Color

The Activity layout uses a yellow background:

```xml id="g7w4ap"
android:background="#FFFF00"
```

## Activity Life Cycle

The Activity Life Cycle consists of the following important methods:

1. `onCreate()`
2. `onStart()`
3. `onResume()`
4. `onPause()`
5. `onStop()`
6. `onRestart()`
7. `onDestroy()`

### Life Cycle Flow

```text id="c3f9rx"
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

If the Activity is permanently closed:

```text id="j1k8qp"
onPause()
    ↓
onStop()
    ↓
onDestroy()
```

## Log Message

`Log` is used to display Activity Life Cycle events in **Logcat**.

Example:

```kotlin id="f6x2md"
Log.d("ActivityLifecycle", "onCreate called")
```

The messages can be viewed in:

**Android Studio → Logcat**

## Toast Message

A Toast displays a short message to the user.

Example:

```kotlin id="v2p5qa"
Toast.makeText(this, "onCreate called", Toast.LENGTH_SHORT).show()
```

## Snackbar Message

A Snackbar displays a short message at the bottom of the screen.

Example:

```kotlin id="r8n4zs"
Snackbar.make(
    findViewById(android.R.id.content),
    "onCreate called",
    Snackbar.LENGTH_SHORT
).show()
```

## Activity Life Cycle Demonstration

Each Activity Life Cycle method should:

* Print a message using `Log`.
* Display a Toast message.
* Display a Snackbar message where appropriate.

Example:

```kotlin id="x5d2mn"
override fun onStart() {
    super.onStart()

    Log.d("ActivityLifecycle", "onStart called")

    Toast.makeText(
        this,
        "onStart called",
        Toast.LENGTH_SHORT
    ).show()
}
```

## Main Files

```text id="p4v8cy"
app/
└── src/
    └── main/
        ├── java/com/example/activitylifecycle/
        │   └── MainActivity.kt
        │
        ├── res/
        │   └── layout/
        │       └── activity_main.xml
        │
        └── AndroidManifest.xml
```

## MainActivity.kt Responsibilities

`MainActivity.kt` is responsible for:

* Initializing the Activity.
* Connecting the XML layout with the Activity.
* Implementing Activity Life Cycle methods.
* Printing Life Cycle messages in Logcat.
* Displaying Toast messages.
* Displaying Snackbar messages.

## activity_main.xml Responsibilities

`activity_main.xml` is responsible for:

* Creating the `ConstraintLayout`.
* Setting the yellow background.
* Creating the `TextView`.
* Positioning the TextView at the center.
* Setting TextView properties.

## Generate ID of TextView

Every UI component should have a unique ID so that it can be accessed from Kotlin code.

Example:

```xml id="b2r6ht"
android:id="@+id/textView"
```

The `+id` creates a new ID for the `TextView`.

## ConstraintLayout

`ConstraintLayout` is used to position UI elements using constraints.

To place the `TextView` at the center, constraints are applied to all four sides:

```xml id="n9c3wf"
app:layout_constraintTop_toTopOf="parent"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintEnd_toEndOf="parent"
```

## How to Run

1. Open the project in Android Studio.
2. Wait for Gradle synchronization.
3. Connect an Android device or start an emulator.
4. Run the application.
5. The screen displays **Hello World** in the center.
6. The background appears yellow.
7. The TextView appears blue, bold, italic, and 27sp.
8. Open **Logcat** in Android Studio.
9. Perform Activity operations such as opening, minimizing, rotating, or closing the Activity.
10. Observe the Activity Life Cycle methods in Logcat.

## Study / Viva Topics

The following topics should be studied:

* TextView and its properties
* Toast Message
* Snackbar Message
* Android built-in resources
* Activity Life Cycle
* Log Message
* Logcat
* ConstraintLayout properties
* Generating IDs for Views
* `onCreate()`
* `onStart()`
* `onResume()`
* `onPause()`
* `onStop()`
* `onRestart()`
* `onDestroy()`

## Learning Outcome

After completing this practical, students will understand:

* How to create a basic Android UI.
* How to use `TextView` properties.
* How to use Android built-in colors.
* How to use `ConstraintLayout`.
* How to generate and use View IDs.
* How Activity Life Cycle methods work.
* How to display Toast and Snackbar messages.
* How to print messages in Logcat.

## Conclusion

This practical demonstrates the **basic Android UI** and the complete **Activity Life Cycle**. It shows how `TextView`, `ConstraintLayout`, Toast, Snackbar, Logcat, and Activity Life Cycle methods work together in an Android application.
