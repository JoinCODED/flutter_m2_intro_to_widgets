Now, when you click the button, nothing happens. Why is that? because you didn't write any **Dart** code that does any command. Let's see if the button works by writing `print("Hello");` inside the **curly brackets** that come after `onPressed`.

```dart
class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: TextButton(
          onPressed: () {
            print("Press Me!");
          },
          child: Text("Text Button"),
        ),
      ),
    );
  }
}
```

Save and run the app. Nothing happens on the phone.

Go back to **Visual Studio Code**.

Check the debug console at the bottom of the **VSCode** screen.

![screenshot](https://lh5.googleusercontent.com/m5OWIGI3s-a2KkLTOnrvNTu_tiyc7qBxmEkhc_k8gVmMU8QUPcTfdHYgn1olDdSvntn-Kx88POk9GhZPwA14IuHXqqkKKks2muEO9NYJS7DLqKoaqo_J7LJx5tsovIG4vgLMma7p)

The number incrementing is just telling you that this line has been printed this number of times.

In case you cannot see the debug console:

1. Make sure you are running the app from the app top menu `Run > Run without debugging`
2. Make sure you opened the debug console window by going to`View > Debug Console`
