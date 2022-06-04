Let's Add an `AppBar` to our `ProfilePage`.

The `AppBar` is a part of the `MaterialApp` and is used to display the title of the app and the navigation menu.

It's a property of the Scaffold widget.

To add an app bar to our `ProfilePage`, we need to add an `AppBar` to the `Scaffold` widget.

```dart
Scaffold(
  appBar: AppBar(
    title: Text('Profile Page'),
  ),
[...]
```

In Ios, the AppBar title will show in the middle, while in android, the title will show in the left.

However, we can change this behavior by using the `centerTitle` property.

```dart
Scaffold(
  appBar: AppBar(
    title: Text('Profile Page'),
    centerTitle: true,
  ),
[...]
```

There's a lot of properties that can be used with the `AppBar` widget.

Explore them in the [AppBar](https://docs.flutter.io/flutter/material/AppBar-class.html) documentation.
