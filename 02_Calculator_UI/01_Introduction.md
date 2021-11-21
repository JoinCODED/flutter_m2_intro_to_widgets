# Calculator UI 

In this lesson, we will create a Calculator UI. 

We will learn how to use these: 

- **Box Decoration**

- **Layout**



![screenshot](https://user-images.githubusercontent.com/24327781/133928283-eab43fd9-056a-40a6-9890-f61221d12c92.png)



1. We need to create a new flutter project called "**calculator_ui_app**"

> Note: to create a new flutter project, review `01_Create_new_Flutter_project



2. After that, we will remove all codes that inside **main.dart**, then we will copy the code down, and paste it inside **main.dart** file.



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
      
    );
  }
}
```



3. After that run the app, you will see a white screen.

> Note: to run the app, review `03_Run_the_application`



4. First, we will learn how to design the button for our calculator. So, we will use **Container** widget to design our button. This is another use case of Container, it will help us to design and control the width and height of other widgets. Also, it will help us to add decoration for the widget that we wrap with Container.

> **Note**:  in this lesson, we just focus on the user interface. So, we will use Container to design buttons, but in the future lesson, we will learn how to use buttons.



​	So, inside Scaffold, we will use **body** named arguments, to add our **Container** widget. After we add it, we will not see anything because we did not use the named arguments inside the **Container** widget.

```dart
Scaffold(
      body: Container(
        
      ),
    );
```





5. We will use **width** and **height** named arguments inside **Container** to give a limit to our **Container** to not take all space of the screen. So, because we need a Square container for our calculator button, we will keep the height and width equal. So, in our cause we will put 75 for height and width.

```dart
Container(
        height: 75,
        width: 75,
      ),
```



















