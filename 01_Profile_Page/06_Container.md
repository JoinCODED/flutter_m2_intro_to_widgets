A **`Container`** widget acts as a box for storing one widget or more, resizing and positioning them as the user wishes on the screen. There are many usages for the **`Container`**, don't hesitate to take a look at them 😉. But for now, you will go through two of its usages:

1. Aligning the widgets:
 You can use the **`Container`** to align the widget inside the layout widget such as **`Column`** and **`Row`**. In your case, you will align your image widget to be in the center of the home screen by using the **`alignment`** named argument inside the Container widget, and this named argument takes the **`Alignment`** object.

```dart
Container(
          alignment: Alignment.center,  // <- here
          child: Image.asset(
            'assets/images/profile.png',
            width: 200,
            height: 200,
          ),
        )
```

![screenshot](https://user-images.githubusercontent.com/24327781/119666042-9b4e3680-bdfa-11eb-95f1-1d6ed3b60f51.gif)

You are going to apply the same named argument to **`Text`** widgets to align them to the left of the screen.

```dart
 Column(
          mainAxisAlignment: MainAxisAlignment.start,
          children: [
            Container(
              alignment: Alignment.center,
              child: Image.asset(
                'assets/images/profile.png',
                width: 200,
                height: 200,
              ),
            ),
            Container(
              alignment: Alignment.centerLeft,      // <- here
              child: Text(
                'Name: Cat Show',
              ),
            ),
            Container(
              alignment: Alignment.centerLeft,      // <- here
              child: Text(
                'Gender: Male',
              ),
            ),
            Container(
              alignment: Alignment.centerLeft,     // <- here
              child: Text(
                'Hobbies: Acting and Fencing',
              ),
            ),
          ],
        ),
```

The final result:

![screenshot](https://user-images.githubusercontent.com/24327781/119666521-10217080-bdfb-11eb-87aa-9e037fff762d.png)

2. Adding space around the container and between the border and its content:
 The other usage of the **`Container`** widget is to add a **`margin`** to create an empty space around the **`Container`**, and **`padding`** to give space between the border and the child.

![screenshot](https://user-images.githubusercontent.com/24327781/119667023-86be6e00-bdfb-11eb-96e0-43c32f132a7e.png)

In your case, you will add a margin for your image, and padding for the text widgets.

> Note: if you want to add a margin, you need to use the **`margin`** named argument inside the **`Container`** widget, and if you want to add padding, use the **`padding`** named argument inside the **`Container`** widget. Both of these named arguments take **`EdgeInsets`** object.

```dart
Column(
          mainAxisAlignment: MainAxisAlignment.start,
          children: [
            Container(
              alignment: Alignment.center,
              margin: EdgeInsets.only(bottom: 40),      // <- here
              child: Image.asset(
                'assets/images/profile.png',
                width: 200,
                height: 200,
              ),
            ),
            Container(
              alignment: Alignment.centerLeft,
              padding: EdgeInsets.only(left: 20, bottom: 15),  // <- here
              child: Text(
                'Name: Cat Show',
              ),
            ),
            Container(
              alignment: Alignment.centerLeft,
              padding: EdgeInsets.only(left: 20, bottom: 15),  // <- here
              child: Text(
                'Gender: Male',
              ),
            ),
            Container(
              alignment: Alignment.centerLeft,
              padding: EdgeInsets.only(left: 20),   // <- here
              child: Text(
                'Hobbies: Acting and Fencing',
              ),
            ),
          ],
        ),
```

The style of your text widgets looks ugly. 🙂

![screenshot](https://media.giphy.com/media/67SXeoc8RLwvqCwn2F/giphy.gif)

You can change them by using the **`TextStyle`** object inside **`Text`** widget.

```dart
Scaffold(
      backgroundColor: Colors.orangeAccent[200],
      body: SafeArea(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.start,
          children: [
            Container(
              alignment: Alignment.center,
              margin: EdgeInsets.only(bottom: 40),
              child: Image.asset(
                'assets/images/profile.png',
                width: 200,
                height: 200,
              ),
            ),
            Container(
              alignment: Alignment.centerLeft,
              padding: EdgeInsets.only(left: 20, bottom: 15),
              child: Text(
                'Name: Cat Show',
                style: TextStyle(            // <- here
                  color: Colors.white,
                  fontSize: 24,
                  fontWeight: FontWeight.bold,
                ),
              ),
            ),
            Container(
              alignment: Alignment.centerLeft,
              padding: EdgeInsets.only(left: 20, bottom: 15),
              child: Text(
                'Gender: Male',
                style: TextStyle(           // <- here
                  color: Colors.white,
                  fontSize: 24,
                  fontWeight: FontWeight.bold,
                ),
              ),
            ),
            Container(
              alignment: Alignment.centerLeft,
              padding: EdgeInsets.only(left: 20),
              child: Text(
                'Hobbies: Acting and Fencing',
                style: TextStyle(       // <- here
                  color: Colors.white,
                  fontSize: 24,
                  fontWeight: FontWeight.bold,
                ),
              ),
            ),
          ],
        ),
      ),
    )
```

The final result :

![screenshot](https://user-images.githubusercontent.com/24327781/119668114-7f4b9480-bdfc-11eb-92d5-46a9eb56bc0c.png)

Finally,

![screenshot](https://media.giphy.com/media/XbxZ41fWLeRECPsGIJ/giphy.gif)

> **Note: You can find the full source code [here](https://github.com/JoinCODED/flutter_profile_page_app).**
