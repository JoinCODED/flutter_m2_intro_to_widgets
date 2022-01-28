If you see the text style for some of the **`Text`** widgets, you will note that we are repeating the code many times; the best practice is to make one variable that has the **`TextStyle`** object and use it inside our Text widgets multiple times.

This practice has two advantages:

- Will make your code shorter.
- When you want to change the size of text, you will change it one time in one place.

1. Create a variable with the name `greenTextStyle` and give it the value of the styling that you are going to reuse for most of the buttons. To do that, write the following:

```dart

class HomeScreen extends StatelessWidget {
  // Here, and before everything👇🏻
  final TextStyle greenTextStyle = TextStyle(fontSize: 24, color: Colors.green);
```

This line of code stores the styling `TextStyle(fontSize: 24, color: Colors.green)` under a variable name, and we called it `greenTextStyle`. Now every time you want to apply a styling like the above, just insert the name `greenTextStyle` that we created!

2. Change every container that has a green styling and replace the styling with the variable we created.

```dart
// Old
  Container(
    style: TextStyle(fontSize: 24, color: Colors.green) // Replace this
  )

// New
  Container(
    style: greenTextStyle // <-- with this!
  )
```

3. Now let's create the other styling and box decorations variables under the previous variable, and repeat the same steps for all the buttons

```dart
 final TextStyle whiteTextStyle = TextStyle(
    fontSize: 24,
    color: Colors.grey
  );
 final TextStyle redTextStyle = TextStyle(
    fontSize: 24,
    color: Colors.red
  );

  final BoxDecoration greyDecoration = BoxDecoration(
    color: Colors.grey[200],
    borderRadius: BorderRadius.circular(14),
  ),
  final BoxDecoration greenDecoration = BoxDecoration(
    color: Colors.green[200],
    borderRadius: BorderRadius.circular(14),
  ),
  final BoxDecoration redDecoration = BoxDecoration(
    color: Colors.red[100],
    borderRadius: BorderRadius.circular(14),
  ),

```

> **Note:** What we just did is called **Refactoring**, which results with the same result, but a better code. Now if you change the variable value of the greenTextStyle, it will change for all the buttons. You don't need to go over button by button to change their stylings! 😉

1. Now let's add the text container that holds the values of the pressed numbers. This should look like the following. To do that, go to the column, and add this container as the first child.

![screenshot](https://user-images.githubusercontent.com/24327781/133928283-eab43fd9-056a-40a6-9890-f61221d12c92.png)

```dart
// Text holder
Container(
            width: 350,
            height: 50,
            margin: EdgeInsets.all(20),
            // 1
            alignment: Alignment.center,
            decoration: BoxDecoration(
              color: Colors.grey[200],
              borderRadius: BorderRadius.circular(14),
            ),
            child: Text(
              '923',
              style: TextStyle(
                fontSize: 24,
                fontWeight: FontWeight.bold,
              ),
            ),
          ),
```

> **Note: You can find the full source code [here](https://github.com/Northwest-content/flutter_calculator_ui_app).**
