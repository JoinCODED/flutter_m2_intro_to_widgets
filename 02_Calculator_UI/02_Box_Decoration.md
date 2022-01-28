# Box Decoration

1. We will use **`decoration`** named argument inside the **`Container`**, which will help us to add some styling for the **`Container`** widget such as **background color** and **border radius**.

```dart
Container(
        height: 75,
        width: 75,
        decoration: BoxDecoration(
          color: Colors.greenAccent[100],
          borderRadius: BorderRadius.circular(14),
        ),
      ),
```

> Note: **`decoration`** named argument takes **`BoxDecoration`** object, and inside **`BoxDecoration`**, we use `color` argument to give a color for our `Container` widget. Also, we use **`borderRadius`** argument to keep our border semi-circular.

![screenshot](https://user-images.githubusercontent.com/24327781/119705628-9ac79700-be1e-11eb-80e8-3a6ed548415b.gif)

2. After that we will add **`Text`** widgets inside the child that inside the **`Container`** widget.

```dart
Container(
        height: 75,
        width: 75,
        decoration: BoxDecoration(
          color: Colors.greenAccent[100],
          borderRadius: BorderRadius.circular(14),
        ),
        child: Text('+'), // <- here
      ),
```

Also, we will add a style for our **`Text`** widget

```dart
Text(
  '+',
  style: TextStyle(         // <- here
    fontSize: 24,
    color: Colors.green,
  ),
),
```

Now, let's fix the styling of the container, so we give it a margin, and we center the text inside the button.

```dart
// This container represents a button
Container(
   margin: EdgeInsets.all(8),   // <--- Here
   alignment: Alignment.center, // <--- Here
   height: 75,
   width: 75,
   decoration: BoxDecoration(
     color: Colors.greenAccent[100],
     borderRadius: BorderRadius.circular(14),
   ),
   child: Text(
     '+',
     style: TextStyle(
       fontSize: 24,
       color: Colors.green,
     ),
   ),
 ),
```
