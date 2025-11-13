# Swift_Exam



## 🧱 iOS Technology Layers


iOS is built on four main layers, each providing a set of frameworks and services that work together to make apps run smoothly.

Think of it like a cake with four layers — each one builds on the one below it.


1. Cocoa Touch Layer (Top Layer)

🎯 Purpose: Handles the User Interface (UI) and user interaction.

🧩 What it includes:

👉 UIKit / SwiftUI → for creating app interfaces (buttons, labels, text fields, etc.)

👉 MapKit → for using maps in apps.

👉 MessageUI → for sending emails or messages.

👉 Push Notifications, Gestures, Touch Events, etc.

💡 Example: When you tap a button, the Cocoa Touch layer handles the touch event and updates the screen.



2. Media Layer

🎯 Purpose: Handles all graphics, audio, and video in your app.

🧩 What it includes:

👉 Core Graphics → 2D drawing.

👉 Core Animation → smooth animations.

👉 AVFoundation → playing and recording audio/video.

👉 SpriteKit / SceneKit → for 2D and 3D games.

👉 Metal → high-performance graphics for advanced apps and games.

💡 Example: When your app shows a video or animation, the Media layer makes it possible.



3. Core Services Layer

🎯 Purpose: Provides data, networking, and system services.

🧩 What it includes:

👉 Core Data → for storing app data locally.

👉 CloudKit → for syncing data with iCloud.

👉 Core Location → for GPS and location tracking.

👉 Networking APIs → for internet connections and web requests.

👉 Address Book, File Handling, Preferences, etc.

💡 Example: When your app saves user information or fetches data from the internet, this layer handles it.



4. Core OS Layer (Bottom Layer)

🎯 Purpose: Interacts directly with the hardware and low-level system functions.

🧩 What it includes:

👉 Kernel → manages the CPU, memory, and system processes.

👉 Security Framework → encryption, keychain, and secure access.

👉 Bluetooth, Wi-Fi, File System, Power Management.

👉 Drivers → control the hardware devices.

💡 Example: When your app uses Bluetooth or accesses the camera hardware, the Core OS layer manages that safely.


---


### 🌀 What is iOS Application Life Cycle?

It is the sequence of stages an iOS app goes through from the time you open it until you close or terminate it.
Each stage defines the state of the app and how it interacts with the system.

<img width="642" height="727" alt="image" src="https://github.com/user-attachments/assets/b6c3ce6b-bb6d-4257-a473-b196abd512f3" />

| Stage              | Description                                                                           | Example                                                                |
| ------------------ | ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| **1. Not Running** | The app is **not launched yet**, or it has been **terminated** by the system or user. | You haven’t opened the app yet, or you closed it from recent apps.     |
| **2. Inactive**    | The app is running **but not receiving user input** (temporarily paused).             | A call or notification appears — your app is visible but not active.   |
| **3. Active**      | The app is **running in the foreground** and **interacting with the user**.           | You are using the app, tapping buttons, typing text, etc.              |
| **4. Background**  | The app is **not visible**, but it’s still **executing code** (doing tasks).          | After pressing the Home button, the app saves data or finishes a task. |
| **5. Suspended**   | The app is in **memory but not running any code**. It’s ready to resume quickly.      | You switched to another app; iOS freezes your app to save battery.     |

----
### 🍎 What is Cocoa?

Cocoa (or Cocoa Touch for iOS) is the main framework provided by Apple to build iOS applications.
It contains all the base classes and APIs needed to:

👉 Create user interfaces

👉 Handle events

👉 Manage app behavior

It’s built on Objective-C / Swift and includes frameworks like UIKit, Foundation, and Core Data.

🧩 Application Class (UIApplication)

In Cocoa (specifically Cocoa Touch for iOS), the Application Class is represented by:

```swift
UIApplication

```
| Function                                     | Description                                                                                          |
| -------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| **1. Manages App Life Cycle**                | Keeps track of the app’s states — launching, active, background, terminated.                         |
| **2. Handles Events**                        | Receives system events like touch, notifications, and app switching.                                 |
| **3. Coordinates Between App and System**    | Communicates with iOS to handle app-wide operations (e.g., opening URLs, handling background tasks). |
| **4. Manages App-Level Settings**            | Manages status bar, background execution, and app notifications.                                     |
| **5. Keeps a Reference to the App Delegate** | Works closely with the `AppDelegate` class, which responds to major app events.                      |

---


### 🍎 1. App
📘 Meaning:

An App is the entire iOS application — it’s what you install and open on your iPhone or iPad.

In iOS programming, the App is managed by the UIApplication class, which handles:

👉 The app’s life cycle (launch, background, terminate)

👉 User events (touches, notifications)

👉 Overall coordination between your app and iOS system

It’s like the main controller that connects everything — user interface, scenes, and logic.

---

### 🪟 2. Scene


📘 Meaning:

A Scene represents one instance of your app’s user interface — basically, a single screen or window.

In iOS 13 and later, Apple introduced the multi-scene feature, which means:

👉 One app can have multiple scenes (like multiple windows in iPad apps).

👉 Each scene is managed by a SceneDelegate.

----


### 🧱 3. Scene Builder (Interface Builder)
📘 Meaning:

Scene Builder (or Interface Builder) is the visual design tool inside Xcode where you create and arrange UI elements like:

👉 Buttons

👉 Labels

👉 Text fields

👉 Images

You use Storyboard files (.storyboard) to visually design app screens (called scenes).


---

## MODULE 2

---

📱 Simple View Application Template

A Simple View Application in SwiftUI is the basic template used to create an iOS app that contains a single view (screen).
It helps you:

👉 Understand the structure of a SwiftUI app

👉 Learn how the App and View components work together

When you create a new iOS project in Xcode, you are asked to choose a template —

👉 A template is a starting structure that gives you some basic code and files to begin your app quickly.

👉 This template creates an app with only one screen (view) — perfect for small or beginner projects.


🧩 Main Components of a SwiftUI App

There are two main files created automatically when you start a new SwiftUI app:

1. App File (Main Entry Point)
 📁 Example: MyFirstApp.swift

  This file defines the starting point of your SwiftUI app.
  It tells iOS what to show when the app launches.


2. View File (User Interface File)
  📁 Example: ContentView.swift

  This file defines what your app shows on the screen — it’s the user interface (UI) of your app.

---
### 🧩 What is a Stack in SwiftUI?

A Stack is a layout container that arranges multiple views (like Text, Image, Button) in a line —
either vertically, horizontally, or overlapping.

SwiftUI provides three types of stacks:

| Stack Type | Layout Direction            | Example                                     |
| ---------- | --------------------------- | ------------------------------------------- |
| **VStack** | Vertical (top to bottom)    | Stack of items placed one below another     |
| **HStack** | Horizontal (left to right)  | Stack of items placed side by side          |
| **ZStack** | Overlapping (front to back) | Stack of items layered on top of each other |

🪜 1. VStack (Vertical Stack)
📘 Definition:

Arranges views vertically (from top to bottom).

💻 Example:
```swift
VStack {
    Text("Welcome")
        .font(.largeTitle)
    Text("to SwiftUI")
        .foregroundColor(.blue)
}

```
----

🧱 2. HStack (Horizontal Stack)
📘 Definition:

Arranges views horizontally (from left to right).

💻 Example:
```swift
HStack {
    Image(systemName: "star.fill")
    Text("Favorites")
}

```
----

🎨 3. ZStack (Overlapping Stack)
Arranges views on top of each other (like layers).

💻 Example:
```swift
ZStack {
    Image("background")
    Text("Hello SwiftUI!")
        .foregroundColor(.white)
        .font(.title)
}

```

----
### 🧩 State Handling in SwiftUI (Simple Explanation)

In SwiftUI, state handling means managing data that can change over time and updating the user interface (UI) automatically when that data changes.

| Property               | Description                                                                                     | Example Use                                  |
| ---------------------- | ----------------------------------------------------------------------------------------------- | -------------------------------------------- |
| **@State**             | Used for **local state** inside a single view. When it changes, the view updates automatically. | A toggle button or counter value.            |
| **@Binding**           | Connects a **@State variable** from one view to another (child view).                           | Sharing data between parent and child views. |
| **@ObservedObject**    | Used for **external data models** that may be used by multiple views.                           | When data comes from a separate model class. |
| **@StateObject**       | Used when a view **owns** the data model and should keep it alive.                              | Declaring main data in a parent view.        |
| **@EnvironmentObject** | Used to share **data across many views** without passing it manually.                           | Sharing user settings or themes globally.    |

###  🧩@State

```swift
import SwiftUI

struct CounterView: View {
    @State private var count = 0   // local state

    var body: some View {
        VStack {
            Text("Count: \(count)")
                .font(.largeTitle)
            Button("Increase") {
                count += 1     // updates state
            }
            .padding()
        }
    }
}

```
### 🧩@Binding

is used in SwiftUI to create a two-way connection between a parent view’s state and a child view’s property.

This means — when the value changes in the child view, it also updates in the parent view, and vice versa.

It allows data sharing between views without creating a new copy of the state.

🪄 Parent View
```swift
import SwiftUI

struct ParentView: View {
    @State private var name = "Sumayya"   // main state variable

    var body: some View {
        VStack {
            Text("Name: \(name)")   // shows updated name
            ChildView(userName: $name)   // pass state using $ (binding)
        }
    }
}

```
🪄 Child View
```swift
struct ChildView: View {
    @Binding var userName: String    // receives the binding from parent

    var body: some View {
        TextField("Enter name", text: $userName)
            .textFieldStyle(RoundedBorderTextFieldStyle())
            .padding()
    }
}

```
### 💡 Definition of @ObservedObject

@ObservedObject is used in SwiftUI to observe data stored in a separate class (called a data model).
When any value in that model changes, the SwiftUI view automatically updates.

🧠 Data Model
```swift
import SwiftUI
import Combine

class CounterModel: ObservableObject {
    @Published var count = 0   // tracked property
}


```
📱 View Using @ObservedObject
```swift
struct CounterView: View {
    @ObservedObject var counter = CounterModel()   // observing the model

    var body: some View {
        VStack {
            Text("Count: \(counter.count)")
                .font(.largeTitle)
            Button("Increase") {
                counter.count += 1   // updates model
            }
            .padding()
        }
    }
}

```
⚙️ Steps to Use

👉 Create a data model class using ObservableObject.

👉 Mark variables you want to track with @Published.

👉 Use that model in your view with @ObservedObject.

| Property           | Purpose                                                  |
| ------------------ | -------------------------------------------------------- |
| `@ObservedObject`  | Used in the view to watch an external data model.        |
| `@Published`       | Used in the model to mark data that triggers UI updates. |
| `ObservableObject` | Protocol that lets SwiftUI observe the class.            |


### 🧩@StateObject

@StateObject is used in SwiftUI to create and own an instance of a data model (ObservableObject) inside a view.

It makes sure the model stays alive as long as the view exists.

```swift
🧠 Data Model
import SwiftUI
import Combine

class CounterModel: ObservableObject {
    @Published var count = 0   // tracked property
}

📱 View Using @StateObject
struct CounterView: View {
    @StateObject var counter = CounterModel()         // view owns the model

    var body: some View {
        VStack {
            Text("Count: \(counter.count)")
                .font(.largeTitle)
            Button("Increase") {
                counter.count += 1
            }
            .padding()
        }
    }
}
```
### 🧩@EnvironmentObject

@EnvironmentObject is used to share data easily across many views in a SwiftUI app — without passing it manually through every view.

It’s like a global data connection for SwiftUI views.
⚙️ When to Use

👉 Use @EnvironmentObject when:

👉 You need the same data (like user settings, login info, or theme) available in multiple screens.

👉 You don’t want to keep passing data with parameters.

1️⃣ Create a Shared Data Model
```swift
import SwiftUI

class UserSettings: ObservableObject {
    @Published var username = "Guest"
}

```

2️⃣ Provide It in the App Entry Point


```swift
@main
struct MyApp: App {
    @StateObject var settings = UserSettings()

    var body: some Scene {
        WindowGroup {
            HomeView()
                .environmentObject(settings) // make it available everywhere
        }
    }
}

```
3️⃣ Access It in Any View
```swift
struct HomeView: View {
    @EnvironmentObject var settings: UserSettings   // access shared data

    var body: some View {
        VStack {
            Text("Welcome, \(settings.username)")
            NavigationLink("Go to Profile", destination: ProfileView())
        }
    }
}

struct ProfileView: View {
    @EnvironmentObject var settings: UserSettings

    var body: some View {
        VStack {
            Text("Edit Name:")
            TextField("Username", text: $settings.username)
                .textFieldStyle(RoundedBorderTextFieldStyle())
                .padding()
        }
    }
}

```
---
### 💡 1. What is a Protocol?

A protocol in Swift is like a blueprint for methods and properties.
It defines what should be done, but not how to do it.

Think of it like a contract — if a class or struct adopts a protocol, it must follow the rules (implement those methods).

```swift
✅ Example: Simple Protocol
protocol GreetingDelegate {
    func sayHello()
}
```

Here, GreetingDelegate is a protocol that says:
➡️ “Any class adopting me must have a sayHello() function.”

---


### 💡 2. What is a Delegate?

A delegate is an object that acts on behalf of another object.
It follows a protocol to perform some task when told to do so.

👉 In simple words:
Delegation = one object gives responsibility to another object to do some work.

---
### 🧩 Basic Views and Controls in iOS (SwiftUI)

In SwiftUI, views are the building blocks of your app’s user interface.
A control is a view that allows the user to interact (like buttons, sliders, toggles, etc.).

| Control            | Purpose                 | Example        | Example                                                                    |
| ------------------ | ----------------------- | -------------- |--------------------------------------------------------------------------- |
| **Label**          | Text + Image            | Menu items     |  Label("Profile", systemImage: "person.circle")                            |
| **TextEditor**     | Multi-line text input   | Notes          |  TextEditor(text: $notes)                                                  |
| **Text**           | Display static text     | Titles         |  Text("Hello, SwiftUI!")                                                   |
| **TextField**      | Single-line input       | Forms          |  TextField("Enter name", text: $name)                                      |
| **SecureField**    | Password input          | Login          |  SecureField("Enter password", text: $password)                            |
| **Image**          | Show image              | Logo           |  Image("profilePic")                                                       |
| **AsyncImage**     | Load image from web     | Profile        |  AsyncImage(url: URL(string: "https://example.com/image.jpg"))             |
| **Button**         | Perform action          | Submit         |  Button("Tap Me") { print("Button tapped!")}                               |
| **Link**           | Open URL                | Website        |  Link("Visit Apple", destination: URL(string: "https://apple.com")!)       |
| **NavigationLink** | Go to another view      | Details page   |  NavigationLink("Go to Details", destination: DetailView())                |
| **ToolbarItem**    | Add toolbar button      | Navigation bar |  .toolbar { ToolbarItem(placement: .navigationBarTrailing) {..             |
| **Toggle**         | On/Off switch           | Settings       |  Toggle("Enable Notifications", isOn: $isOn)                               |
| **Map**            | Display location        | GPS            |                                                                            |
| **Picker**         | Select option           | Dropdown       |  Picker("Select Fruit", selection: $choice) { text()..                     |
| **DatePicker**     | Choose date/time        | Schedule       |  DatePicker("Select Date", selection: $date, displayedComponents: .date)   |                  
| **ProgressView**   | Show progress           | Loading        | ProgressView("Loading...")                                                 |
| **Slider**         | Adjust continuous value | Volume         | Slider(value: $volume, in: 0...1) Text("Volume: \(volume)")                |
| **Stepper**        | Adjust discrete value   | Quantity       | Stepper("Count: \(count)", value: $count, in: 0...10)                      |
| **Chart**          | Data visualization      | Graph          |                                                                            |
| **Shape**          | Draw geometric figure   | UI design      | Circle()                                                                   |

---
### 🎯 1. Touches and Gestures

In iOS, when you touch the screen, the system recognizes it as a touch event.

A gesture is a specific pattern of touches that the system interprets as an action (like tap, swipe, or pinch).

➡️ Touches

Definition:
A touch is a physical contact with the touchscreen.
The iOS system tracks each touch and reports details like:

👉 Location (x, y position on screen)

👉 Time of touch

👉 Movement (dragging, swiping, etc.)

👉 Number of touches (1 finger, 2 fingers, etc.)

➡️ Gestures

Definition:
A gesture is a recognized pattern of one or more touches (like tap, pinch, rotate).
Instead of manually tracking touches, you can use Gesture Recognizers.

Common Gestures:

👉 Tap → single or double tap

👉 Swipe → move finger in a direction

👉 Pinch → zoom in/out (2 fingers)

👉 Rotate → rotate object (2 fingers)

👉 Long Press → hold finger on screen

---

➡️ Multi-Touch Gesture Recognition

Definition:
Multi-touch means using more than one finger at the same time.
For example:

👉 Pinch to zoom (2 fingers)

👉 Rotate gesture (2 fingers turning)

👉 Two-finger tap

🎯 What is Gesture Recognition in SwiftUI?

In SwiftUI, gesture recognition is done using gesture modifiers.
You can attach gestures like tap, long press, drag, pinch (zoom), or rotation to any view.


1️⃣ Tap Gesture
```swift
Text("Tap Me")
    .padding()
    .background(Color.blue)
    .foregroundColor(.white)
    .gesture(
        TapGesture(count: 1)
            .onEnded {
                print("Tapped once!")
            }
    )

```

2️⃣ Long Press Gesture
 

```swift
.gesture(
        LongPressGesture(minimumDuration: 1.0)
            .onEnded { _ in
                print("Long press detected!")
            }
    )

```

3️⃣ Drag Gesture
```swift
.gesture(
        DragGesture()
            .onChanged { value in
                position = value.translation
            }
            .onEnded { _ in
                position = .zero
            }
    )
```

4️⃣ Magnification (Pinch/Zoom) Gesture
```swift
 .gesture(
        MagnificationGesture()
            .onChanged { value in
                scale = value
            }
            .onEnded { _ in
                scale = 1.0
            }
    )
```

5️⃣ Rotation Gesture
```swift
.gesture(
        RotationGesture()
            .onChanged { value in
                angle = value
            }
            .onEnded { _ in
                angle = .zero
            }
    )
```


6️⃣ Combining Gestures
```swift
 .gesture(
        MagnificationGesture()
            .onChanged { value in print("Zooming: \(value)") }
    )
    .simultaneousGesture(
        RotationGesture()
            .onChanged { value in print("Rotating: \(value.degrees)") }
    )
```
---
## 3️⃣ Define the Picker component in SwiftUI and describe its various styles. Explain how it can be used to allow users to select from a list of options, providing an example of its implementation in a form or settings screen.

Explanation:
Picker in SwiftUI is a UI control that allows users to choose a value from a list of options.

Syntax Example:
```swift
@State private var choice = "Apple"

Picker("Select Fruit", selection: $choice) {
    Text("Apple")
    Text("Banana")
    Text("Mango")
}
.pickerStyle(.menu)

```


Picker Styles:

👉 DefaultPickerStyle() – Basic wheel style (used in forms).

👉 WheelPickerStyle() – Scroll wheel, common on iPhone.

👉 SegmentedPickerStyle() – Horizontal segments like tabs.

👉 MenuPickerStyle() – Dropdown-style menu.

---
## 4️⃣ Describe the differences between TextField and SecureField in SwiftUI and explain when to use each in a user interface.

| **Feature**    | **TextField**                 | **SecureField**                       |
| -------------- | ----------------------------- | ------------------------------------- |
| **Purpose**    | Used for normal text input.   | Used for password or sensitive input. |
| **Visibility** | Displays entered text openly. | Hides input with dots or asterisks.   |
| **Example**    | Username, Email, Name         | Password, PIN                         |


```swift
@State private var username = ""
@State private var password = ""

TextField("Enter username", text: $username)
SecureField("Enter password", text: $password)

```
✅ When to Use:

👉 TextField: For general data input.

👉 SecureField: When entering confidential data.

---

## 1️⃣ You are tasked with creating a responsive user interface for an iOS app that should adapt seamlessly to different screen sizes and orientations. Describe how you would use Stack Views to achieve this goal.

Explanation:

In SwiftUI, Stack Views (HStack, VStack, and ZStack) are used to arrange views responsively.

✅ Types of Stack Views:

👉 VStack – Arranges elements vertically.

👉 HStack – Arranges elements horizontally.

👉 ZStack – Overlaps elements (for layering).

How it helps responsiveness:

👉 Automatically adjusts layout based on device screen size and orientation (portrait/landscape).

👉 Works with Spacer() and padding() to make views flexible.

👉 Supports alignment and frame modifiers for adaptive layouts.

```swift
VStack {
    Text("Welcome")
        .font(.title)
    HStack {
        Button("Login") { }
        Button("Signup") { }
    }
}
.padding()


import SwiftUI

struct ContentView: View {
    var body: some View {
        ZStack {
            // Background color
            Color.blue
                .ignoresSafeArea()
            
            // Circle in the middle
            Circle()
                .fill(Color.white)
                .frame(width: 200, height: 200)
            
            // Text on top of the circle
            Text("Hello ZStack!")
                .font(.title)
                .fontWeight(.bold)
                .foregroundColor(.blue)
        }
    }
}


```
Result:

👉 Adapts automatically to iPhone, iPad, and orientation changes.

👉 Simplifies creating flexible UIs.

## 2️⃣ Explain the steps to implement a simple gesture recognizer in SwiftUI to respond to user gestures and update the user interface accordingly.

Explanation:

In SwiftUI, gestures (like tap, drag, long press) are handled using gesture modifiers.

Steps:

Create a State variable to store UI changes.

Attach a gesture (e.g., .onTapGesture, .gesture()) to a view.

Update the State variable inside the gesture handler.

SwiftUI automatically updates the UI when the state changes.

Example (Tap Gesture):

```swift
@State private var colorChanged = false

Circle()
    .fill(colorChanged ? .green : .blue)
    .frame(width: 100, height: 100)
    .onTapGesture {
        colorChanged.toggle()
    }

```
## 3️⃣ Using an example, explain the purpose of NavigationLink in SwiftUI and how it enables navigation between views in an iOS application.

Explanation:

NavigationLink is used in SwiftUI to move from one view to another, just like pushing screens in iOS navigation.

Steps:

Wrap your main view inside a NavigationView.

Use NavigationLink to define the destination view.

Example:
```swift
NavigationView {
    VStack {
        Text("Home Screen")
        NavigationLink(destination: DetailView()) {
            Text("Go to Details")
        }
    }
}

```
Destination View:

```swift
struct DetailView: View {
    var body: some View {
        Text("This is the Detail Screen")
    }
}

```
👉 Provides smooth navigation between screens.

👉 Maintains a navigation bar automatically.

👉 Works well in forms, lists, and menus.

```swift
```
