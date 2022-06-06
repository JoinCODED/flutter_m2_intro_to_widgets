In this lesson, you will create a Calculator UI that you can see below!

![screenshot](https://user-images.githubusercontent.com/24327781/133928283-eab43fd9-056a-40a6-9890-f61221d12c92.png)

To do that, you have to learn the following:

- **Box Decoration**
- **Layout**

1. Create a new flutter project called "**calculator_ui_app**"

2. Replace all the code in the **`main.dart`** file, with the code below:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: HomeScreen(),
    );
  }
}

class HomeScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      // ---> Your code here
    );
  }
}
```

3. Run the app, a white screen will appear. 

4. Use the **`Container`** widget to design the button. This is another usage of **`Container`**, it allows you to design and control the width and height of other widgets, and helps you to add decoration to the widget that you wrapped with the `Container`.

> **Note**: In this lesson, you will focus only on the user interface, so you will design the buttons only. However, in future lessons, you will learn how to use them.

​  Inside **`Scaffold`**, use **`body`** named argument to add the **`Container`** widget. After you add it, you will not see anything because you did not use the named arguments inside the **`Container`** widget:

```dart
Scaffold(
      body: Container(

      ),
    );
```

5. Use **`width`** and **`height`** named arguments inside **`Container`** to size it so it does not take up all the space of the screen. Since you need a square container for the calculator button, keep the height and width equal and assign them both to 75.

```dart
Container(
        height: 75,
        width: 75,
      ),
```
