Now, add as many buttons as you need, but before that, you need to study the layout, and to do that, you need to design a grid. A grid in flutter consists of a single big column, and multiple rows inside.

![Layout columns and rows](https://user-images.githubusercontent.com/8784343/151617633-4789cfc6-1722-409a-a488-c2e3ed098d6f.gif)

The column should consist of 5 rows, and each of them should have 4 buttons inside.

10. Wrap the button `Container` with a **`Row`** widget

- Center the buttons inside the row using the property `mainAxisAlignment` as follows:

```dart
Row(
  mainAxisAlignment: MainAxisAlignment.center,
 // ...
 )
```

11. Wrap that `Row` in a `Column`.

- Center the rows inside the column using the property `mainAxisAlignment` as follows:

```dart
 Column(
  mainAxisAlignment: MainAxisAlignment.center,
 // ...
 )
```

> ![chrome_iRITD3ou2k](https://user-images.githubusercontent.com/24327781/119711925-ad919a00-be25-11eb-82b4-d9ef6903a126.png)

12. Add **`SafeArea`** widget to avoid intrusions on the top of our **`Column`** widget.
13. Duplicate the `Container` inside the Row 4 times:

```dart
  Row(
    children: [
     Container(/*...*/),
     Container(/*...*/),
     Container(/*...*/),
     Container(/*...*/),
    ]
  )
```

14. Duplicate the `Row`s 5 times. Make sure you are inside `Column`:

```dart
  Column(
    children: [
      Row(/*...*/),
      Row(/*...*/),
      Row(/*...*/),
      Row(/*...*/),
      Row(/*...*/),
    ]
  )
```

15. Change the color and the text of the other buttons.

> Note: if you do not find these characters you can copy them from here:
>
> `C` `+/-` `%` `÷` `x`

16. Remove one `Container`, and resize the width of the zero `Container` widget as follows:

```dart
Container(
        margin: EdgeInsets.all(8),
        width: 165,      // <- here
        height: 75,
        decoration: BoxDecoration(
          color: Colors.grey[200],
          borderRadius: BorderRadius.circular(14),
        ),
        alignment: Alignment.center,
        child: Text(
          '0',
          style: TextStyle(
            fontSize: 24,
          ),
        ),
      ),
```

![screenshot](https://user-images.githubusercontent.com/24327781/118665352-daa3d400-b7b7-11eb-9ecb-b4d8e3091a62.png)
