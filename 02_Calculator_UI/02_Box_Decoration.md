6. Use the **`decoration`** named argument inside the **`Container`** widget, to add some styling to it such as **background color** and **border radius**.

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

> Note: The **`decoration`** named argument takes **`BoxDecoration`** object. Inside **`BoxDecoration`**, use `color` named argument to give the `Container` widget a color. Finally, use **`borderRadius`** named argument to keep the border semi-circular.

![screenshot](https://user-images.githubusercontent.com/24327781/119705628-9ac79700-be1e-11eb-80e8-3a6ed548415b.gif)

7. Add **`Text`** widget to the child named argument inside the **`Container`** widget.

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

8. Add a style to the **`Text`** widget

```dart
Text(
  '+',
  style: TextStyle(         // <- here
    fontSize: 24,
    color: Colors.green,
  ),
),
```

9. Give the **`container`** a margin, and center the text inside the button.

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
