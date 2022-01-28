In this lesson, we will create a Calculator UI that you can see below!

![screenshot](https://user-images.githubusercontent.com/24327781/133928283-eab43fd9-056a-40a6-9890-f61221d12c92.png)

To do that, we we'll have to learn these 2 main things:

- **Box Decoration**
- **Layout**

1. We need to create a new flutter project called "**calculator_ui_app**"

2. After that, we will remove all codes that inside **main.dart**, then we will copy the code below, and paste it inside **main.dart** file.

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

3. After that run the app, you will see a white screen.

4. First, we will learn how to design the button for our calculator. So, we will use **`Container`** widget to design our button. This is another use case of Container, it will help us to design and control the width and height of other widgets. Also, it will help us to add decoration for the widget that we wrapped with the `Container`.

> **Note**: in this lesson, we just focus on the user interface. So, we will use Container to design buttons, but in the future lesson, we will learn how to use buttons.

​ So, inside Scaffold, we will use **`body`** named arguments, to add our **`Container`** widget. After we add it, we will not see anything because we did not use the named arguments inside the **`Container`** widget.

```dart
Scaffold(
      body: Container(

      ),
    );
```

5. We will use **`width`** and **`height`** named arguments inside **`Container`** to give a limit to our **`Container`** to not take all space of the screen. Because we need a Square container for our calculator button, we will keep the height and width equal. In our cause, we will assign 75 for height and width.

```dart
Container(
        height: 75,
        width: 75,
      ),
```
