
In this module, we will dig deeper into flutter widgets and we'll learn with that some basic usages of Dart language. by the end of this module, you'll be able to create dynamic applications using Dart language that can do calculations and some functionalities. 





In this lesson, we will create a profile page app.



We will learn how to use these new Widgets:

 - **Image.asset**
 - **Column**
 - **Row**
 - **Container**



**![screenshot](https://lh3.googleusercontent.com/bMdRK6Oi9Im6VUexQhh9OmblbdvFM6af2CI0qClG9eRpYlsdGfiI7YQg-uZluPfpqJAJSTRyakJD-E0hP8BIn28aszVhZ2rjxov-jBdOXr6OMEATSp46xP75lckrlZqUps8j0cJX)**





1. We need to create a new flutter project called "**profile_page_app**"

> Note: to create a new flutter project, review flutter_m1_intro_to_flutter/02_run_first_app/**01_Create_new_Flutter_project**



2. After that, we will remove the code that is inside the **main.dart**, then we will copy the code down, and paste it inside the **main.dart** file.

   ```dart
   import 'package:flutter/material.dart';
   ​
   void main() {
    runApp(MyApp());
   }
   ​
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

   > Note: to run the app, review flutter_m1_intro_to_flutter/02_run_first_app/**03_Run_the_application**



4. To change the background color for our home screen. We will use the **backgroundColor** named argument that inside **the Scaffold** widget.

   ```dart
   Scaffold(
        backgroundColor: Colors.orange,
     );
   ```

   

![screenshot](https://lh4.googleusercontent.com/XrRHQChoKH7yiGvlvgXqTlAIA5mYgpmMsumiklq4Rd-D4oCEk0ugTwo9p7vw04fg6OyqfryCrHKk-dAsBg1PZLfuEQ0RlW0tZQfZzLzvtKCWHXMsTLPX-QC6NyGRfldnBfWashAX)










































