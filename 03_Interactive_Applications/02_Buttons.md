
You can see buttons everywhere: a button to send a message, to call a friend, and to share an Instagram story with a friend. After you press the button, you expect the application to respond with some sort of action, like navigating you to another screen or doing something on the screen. We call this action a function, and in this module, we're going to learn how to create functions.

In Flutter, there are various types of buttons, and the most important ones are:

1. **Elevated button**
2. **Text button**
3. **Outlined button**

All these buttons have a different design but a common behavior. Since they all require two arguments: `onPressed`, and `child`.
Now, Let's start with the second one, **`TextButton`**:

```dart
@override
 Widget build(BuildContext context) {
   return Center(
     child: TextButton(onPressed: onPressed, child: child),
   );
 }
```

We have to pass a Widget to the `child`, typically a `Text` widget or an `Icon` widget. Let's go with the `Text` widget, which displays the label of the button:

```dart
@override
 Widget build(BuildContext context) {
   return Center(
     child: TextButton(onPressed: onPressed, child: Text("Press me!")),
   );
 }
```

Now, if you try to run the app, it would not work, because you have to pass a proper value to `onPressed`. For now, just add this `(){}`. Calm down, I know, it looks weird, just hang in there, we are going to explain what this is, just let the app work!

```dart
class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: TextButton(
          onPressed: () {},
          child: Text("Text Button"),
        ),
      ),
    );
  }
}
```

Now save, YUPPPEEE it's wooooorrkiiiing! 🤩

We have an amazing beautiful button!

You can check the following links to get more information about buttons in flutter:

- [Flutter Buttons](https://www.javatpoint.com/flutter-buttons).
- [Flutter Button Types with Examples](https://medium.com/app-dev-community/flutter-button-types-with-examples-10ae487621a3).
- [Flutter - Working with Material Button](https://www.geeksforgeeks.org/flutter-working-with-material-button/).
- [Top 3 Ways to Create A Button with Icon and Text in Flutter](https://www.flutterbeads.com/button-with-icon-and-text-flutter/).
