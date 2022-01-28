Now, let's add as many buttons as we need. But before we add them, we need to study our layout. We're going to design a grid. A grid in flutter consists of a single big column, and multiple rows inside it.

![Layout columns and rows](https://user-images.githubusercontent.com/8784343/151617633-4789cfc6-1722-409a-a488-c2e3ed098d6f.gif)

So every row should consist of 4 buttons, and the column would have 4 rows.

1. First, let's wrap our button `container` with a **`Row`** widget

   - Let's center the buttons inside the row using the named argument `mainAxisAlignment` as follows:

   ```dart
   Row(
     mainAxisAlignment: MainAxisAlignment.center`
    // ...
    )
   ```

1. And now, let's wrap that `Row` in a `Column`.

   - Let's center the rows inside the column using the named argument `mainAxisAlignment` as follows:

   ```dart
    Column(
     mainAxisAlignment: MainAxisAlignment.center`
    // ...
    )
   ```

> Note: the **mainAxisAlignment** for the **Row** widget is different from the **Column** widget because in the **Row** widget the main axis alignment will start from left to right, and the column main axis alignment will start from top to bottom.
>
> ![chrome_iRITD3ou2k](https://user-images.githubusercontent.com/24327781/119711925-ad919a00-be25-11eb-82b4-d9ef6903a126.png)

3. Add **`SafeArea`** widget to avoid intrusions on the top of our **`Column`** widget.

4. Now, duplicate the rows 4 times. Make sure you are inside `Column` as follows:

```dart
  Column(
    children: [
      Row(/*...*/),
      Row(/*...*/),
      Row(/*...*/),
      Row(/*...*/),
    ]
  )
```

![screenshot](https://media.giphy.com/media/XbxZ41fWLeRECPsGIJ/giphy.gif)

5. Now, you just need to change the color of the other buttons, and the text inside them.

> Note: if you did not find these characters you can copy them from here
>
> `C` `+/-` `%` `÷` `x`

6.  The `0` button from the final result screenshot below is bigger in size. So we'll to remove one **Container**, and we resize the width for the zero container widget as follows.

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
