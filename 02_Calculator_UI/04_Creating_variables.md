If you see the **`TextStyle`** for some of the **`Text`** widgets, you will note that you are repeating the same code multiple times, and repetitive code is the worst thing the programmer does, so the best practice is to make a variable that stores the **`TextStyle`** object and use it inside the Text widgets as many times as you want.

Why not repeat the code? Because of two main reasons:

- The code will get bigger as the project gets bigger.
- A big and unorganized code requires more time and effort when it comes to fixing tiny or big bugs.

Storing the repetitive code in a variable allows you to clean, organize, and understand the code when you get back to it after a long time, you will forget what you wrote and it will not make sense to you.

Now, let's move to the next step and start cleaning the code a bit.

1. Create a variable named `greenTextStyle` and give it the value of the styling object that you are going to reuse for most of the buttons, just like the code below:

```dart

class HomeScreen extends StatelessWidget {
  // Here, and before everything👇🏻
  final TextStyle greenTextStyle = TextStyle(fontSize: 24, color: Colors.green);
```

This line of code stores the styling `TextStyle(fontSize: 24, color: Colors.green)` inside a variable named **`greenTextStyle`**. Now, whenever you need to use this styling, you can just call the variable **`greenTextStyle`**

2. Replace every **`TextStyle`** object in the container that has a green styling with the variable **`greenTextStyle`**.

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

3. Create the other styling and box decoration variables and place them below the previous variable **`greenTextStyle`**, then repeat the same steps for replacing all **`TextStyle`** objects in the other buttons.

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
  );
  final BoxDecoration greenDecoration = BoxDecoration(
    color: Colors.green[200],
    borderRadius: BorderRadius.circular(14),
  );
  final BoxDecoration redDecoration = BoxDecoration(
    color: Colors.red[100],
    borderRadius: BorderRadius.circular(14),
  );

```

> **Note:** What you just did is called **Refactoring**, which leads to the same result, but creates a better code. Now, if you change the variable value of the greenTextStyle, it will change in all the buttons. 😉

4. Add the text container that holds the values of the pressed numbers. This should look like the picture below. To do that, go to the column, and add the container below as the first child.

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

> **Note: You can find the full source code [here](https://github.com/JoinCODED/flutter_bmi_calculator_starter).**
