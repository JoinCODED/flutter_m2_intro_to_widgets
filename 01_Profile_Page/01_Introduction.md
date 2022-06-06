
In this module, we will dig deeper into flutter widgets and we will learn some basic usages of Dart language. By the end of this module, you will be able to create dynamic applications, using Dart language, that can perform calculations and some functionalities. 





In this lesson, we will create a profile page app and learn how to use these new widgets:

 - **Image.asset**
 - **Column**
 - **Row**
 - **Container**



**![screenshot](https://lh3.googleusercontent.com/bMdRK6Oi9Im6VUexQhh9OmblbdvFM6af2CI0qClG9eRpYlsdGfiI7YQg-uZluPfpqJAJSTRyakJD-E0hP8BIn28aszVhZ2rjxov-jBdOXr6OMEATSp46xP75lckrlZqUps8j0cJX)**




You will need to:

1. Create a new flutter project called "**profile_page_app**"

> Note: to create a new flutter project, review flutter_m1_intro_to_flutter/02_run_first_app/**01_Create_new_Flutter_project**



2. Replace the code inside the **main.dart** with the code below.

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

   



3. Run the app, a white screen will appear.

   > Note: To run the app, review flutter_m1_intro_to_flutter/02_run_first_app/**03_Run_the_application**



4. Change the home screen background color by using the **backgroundColor** property inside **the Scaffold** widget.

   ```dart
   Scaffold(
        backgroundColor: Colors.orange,
     );
   ```

   

![screenshot](https://lh4.googleusercontent.com/XrRHQChoKH7yiGvlvgXqTlAIA5mYgpmMsumiklq4Rd-D4oCEk0ugTwo9p7vw04fg6OyqfryCrHKk-dAsBg1PZLfuEQ0RlW0tZQfZzLzvtKCWHXMsTLPX-QC6NyGRfldnBfWashAX)










































