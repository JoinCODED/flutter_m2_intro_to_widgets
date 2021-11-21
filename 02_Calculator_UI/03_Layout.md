# Layout





8. Now, let add as many as buttons we need. In our case, we will need 19 buttons. But before we add them, we need to study our layout. Because we will use Column and Row widgets to combine them in order to give them good look.



Here, we have one **Column** that takes four **Row** widgets, and the **Column** will lay out these Row widgets from top to down.

![screenshot](https://user-images.githubusercontent.com/24327781/119707322-a5832b80-be20-11eb-8738-43c0ce862592.png)

![screenshot](C:\Users\DHA\Documents\ShareX\Screenshots\2021-05\2AtOg6WzPq.png)



Also, inside the **Row** widgets, we will have four **Container** widget, and the **Row** widget will lay out these **Container** widgets from left to right. Here we just explain the first row, but we will repeat these steps for other rows. 

 ![dSxkFfkKYa](https://user-images.githubusercontent.com/24327781/119708028-73be9480-be21-11eb-8699-a0988739ce2f.png)



9. Now after we understand how to layout  our widgets. we will start design our first Row. So, we will wrap our container with **Row** widget. 

> Note: Use the shortcut [here]() to wrap the widget easily.



![screenshot](https://user-images.githubusercontent.com/24327781/119709234-98ffd280-be22-11eb-83c3-a4305644ac29.gif)





10. After that, we will copy our **Container**, and repeat it four times inside the **Row** widget.

```dart
Container(
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



![screenshot](https://user-images.githubusercontent.com/24327781/119709531-ee3be400-be22-11eb-8fe2-9b52f505c8cf.gif)



11. We will use the **Column** widget to add other rows for our buttons. So, we need to wrap our **Row** widget with **Column** widget.

![screenshot](https://user-images.githubusercontent.com/24327781/119709894-57bbf280-be23-11eb-916b-a567535266fd.gif)



12. Also, we will use **SafeArea** widget to avoid intrusions. So, we will add **SafeArea** widget on the top of our **Column** widget.

![screenshot](https://user-images.githubusercontent.com/24327781/119710125-a073ab80-be23-11eb-996b-710fb8e3d866.gif)



13. Now let keep the **child** that inside the Container center of our **Container** widget. To do this, we will use the **alignment** named argument inside the **Container** widget, and we will use **Alignment.center** object to keep the child of Container center.

```dart
 Container(
                  height: 75,
                  width: 75,
                  alignment: Alignment.center,  // <- here
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



14. We will repeat this step for other **Container** widgets.



15. Also, we will add a margin for all **Container** widgets. To do this, we will use the margin named argument inside the **Container** widget.

```dart
 Container(
                  margin: EdgeInsets.all(8),  // <- here
                  height: 75,
                  width: 75,
                  alignment: Alignment.center,
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



16. We will repeat this step for other **Container** widgets.



17. Use the **mainAxisAlignment** named arguments that inside the **Column** widget, and inside **Row** widget to keep our widget center of the app screen.



> Note: the **mainAxisAlignment** for the **Row** widget is different from the **Column** widget because in the **Row** widget the main axis alignment will start from left to right, not from top to bottom.
>
> ![chrome_iRITD3ou2k](https://user-images.githubusercontent.com/24327781/119711925-ad919a00-be25-11eb-82b4-d9ef6903a126.png)





18. After that we will change the text that inside the **Container** widgets. So, keep it same as this picture. You will just need to change each **Text** widget.  



> Note: if you did not find these characters you can copy them from here
>
> `C` `+/-` `%` `÷`



![screenshot](https://user-images.githubusercontent.com/24327781/119712196-f77a8000-be25-11eb-85a7-7c944c458f62.png)





19. After that copy all our **Row** widget.

```dart
Row(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Container(
                  margin: EdgeInsets.all(8),
                  height: 75,
                  width: 75,
                  alignment: Alignment.center,
                  decoration: BoxDecoration(
                    color: Colors.greenAccent[100],
                    borderRadius: BorderRadius.circular(14),
                  ),
                  child: Text(
                    'C',
                    style: TextStyle(
                      fontSize: 24,
                      color: Colors.green,
                    ),
                  ),
                ),
                Container(
                  margin: EdgeInsets.all(8),
                  height: 75,
                  width: 75,
                  alignment: Alignment.center,
                  decoration: BoxDecoration(
                    color: Colors.greenAccent[100],
                    borderRadius: BorderRadius.circular(14),
                  ),
                  child: Text(
                    '+/-',
                    style: TextStyle(
                      fontSize: 24,
                      color: Colors.green,
                    ),
                  ),
                ),
                Container(
                  margin: EdgeInsets.all(8),
                  height: 75,
                  width: 75,
                  alignment: Alignment.center,
                  decoration: BoxDecoration(
                    color: Colors.greenAccent[100],
                    borderRadius: BorderRadius.circular(14),
                  ),
                  child: Text(
                    '%',
                    style: TextStyle(
                      fontSize: 24,
                      color: Colors.green,
                    ),
                  ),
                ),
                Container(
                  margin: EdgeInsets.all(8),
                  height: 75,
                  width: 75,
                  alignment: Alignment.center,
                  decoration: BoxDecoration(
                    color: Colors.greenAccent[100],
                    borderRadius: BorderRadius.circular(14),
                  ),
                  child: Text(
                    '÷',
                    style: TextStyle(
                      fontSize: 24,
                      color: Colors.green,
                    ),
                  ),
                ),
              ],
            ),
```



20. Then, repeat it inside the **Column** widget four times. 

![screenshot](https://user-images.githubusercontent.com/24327781/119712867-adde6500-be26-11eb-9dff-62202fd36661.gif)

![screenshot](https://media.giphy.com/media/XbxZ41fWLeRECPsGIJ/giphy.gif)







21. Now, you just need to change the color of the other **Container**, and the text inside it. 



So, the final result:



![screenshot](https://user-images.githubusercontent.com/24327781/118665352-daa3d400-b7b7-11eb-9ecb-b4d8e3091a62.png)





![screenshot](https://media.giphy.com/media/xC2xDbvyN0tkT7EcPM/giphy.gif)



> **Important**: for the last **Row** widget, we remove one **Container**, and we resize the width for the zero container widget.

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





Final Code: 

```dart
Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Row(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.greenAccent[100],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  'C',
                  style: TextStyle(
                    color: Colors.green,
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.greenAccent[100],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '+/-',
                  style: TextStyle(
                    color: Colors.green,
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.greenAccent[100],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '%',
                  style: TextStyle(
                    color: Colors.green,
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.greenAccent[100],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '÷',
                  style: TextStyle(
                    fontSize: 24,
                    color: Colors.green,
                  ),
                ),
              ),
            ],
          ),
          Row(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '7',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '8',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '9',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.greenAccent[100],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  'X',
                  style: TextStyle(
                    fontSize: 24,
                    color: Colors.green,
                  ),
                ),
              ),
            ],
          ),
          Row(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '4',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '5',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '6',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.greenAccent[100],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '-',
                  style: TextStyle(
                    fontSize: 24,
                    color: Colors.green,
                  ),
                ),
              ),
            ],
          ),
          Row(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '1',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '2',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '3',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.greenAccent[100],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '+',
                  style: TextStyle(
                    fontSize: 24,
                    color: Colors.green,
                  ),
                ),
              ),
            ],
          ),
          Row(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              Container(
                margin: EdgeInsets.all(8),
                width: 165,
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
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.grey[200],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '.',
                  style: TextStyle(
                    fontSize: 24,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.all(8),
                width: 75,
                height: 75,
                decoration: BoxDecoration(
                  color: Colors.red[100],
                  borderRadius: BorderRadius.circular(14),
                ),
                alignment: Alignment.center,
                child: Text(
                  '=',
                  style: TextStyle(
                    fontSize: 24,
                    color: Colors.red,
                  ),
                ),
              ),
            ],
          ),
        ],
      ),
```







