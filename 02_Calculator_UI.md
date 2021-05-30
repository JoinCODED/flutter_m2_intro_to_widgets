# Calculator UI



In this lesson, we will create a Calculator UI. 

We will learn how to use these: 

- **Box Decoration**

- **Layout**

  

<img src="https://user-images.githubusercontent.com/24327781/118665352-daa3d400-b7b7-11eb-9ecb-b4d8e3091a62.png" alt="img" style="zoom:33%;" />





1.  We need to create a new flutter project called "**calculator_ui_app**"

> Note: to create a new flutter project, review `01_Create_new_Flutter_project

2. After that, we will remove all codes that inside **main.dart**, then we will copy the code down, and paste it inside **main.dart** file.

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: HomeScreen(),
    );
  }
}

class HomeScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      
    );
  }
}

```





3. After that run the app, you will see a white screen.

> Note: to run the app, review `03_Run_the_application`







4. First, we will learn how to design the button for our calculator. So, we will use **Container** widget to design our button. This is another use case of Container, it will help us to design and control the width and height of other widgets. Also, it will help us to add decoration for the widget that we wrap with Container.

> **Note**:  in this lesson, we just focus on the user interface. So, we will use Container to design buttons, but in the future lesson, we will learn how to use buttons.

​	

​	So, inside Scaffold, we will use **body** named arguments, to add our **Container** widget. After we add it, we will not see anything because we did not use the named arguments inside the **Container** widget.

```dart
Scaffold(
      body: Container(
        
      ),
    );
```



5. We will use **width** and **height** named arguments inside **Container** to give a limit to our **Container** to not take all space of the screen. So, because we need a Square container for our calculator button, we will keep the height and width equal. So, in our cause we will put 75 for height and width.

```dart
Container(
        height: 75,
        width: 75,
      ),
```





6. We will use **decoration** named argument inside the **Container**, which will help us to add some style for the **Container** widget such as background color and border radius.

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

> Note: **decoration** named argument take **BoxDecoration** object, and inside **BoxDecoration**, we use color argument to give a color for our Container widget. Also, we use **borderRadius** argument to keep our border semi-circular.



<img src="https://user-images.githubusercontent.com/24327781/119705628-9ac79700-be1e-11eb-80e8-3a6ed548415b.gif" alt="FZ1GAQyKXe" style="zoom:50%;" />





7. After that we will add Text widgets inside the child that inside the Container widget. 



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



> Also, we will add a style for our Text widget
>
>    	Text(
>    	         '+',
>    	         style: TextStyle(         // <- here
>    	           fontSize: 24,
>    	           color: Colors.green, 
>    	         ),
>    	       ),



8. Now, let add as many as buttons we need. In our case, we will need 19 buttons. But before we add them, we need to study our layout. Because we will use Column and Row widgets to combine them in order to give them good look.

   

Here, we have one **Column** that takes four **Row** widgets, and the **Column** will lay out these Row widgets from top to down.





<img src="https://user-images.githubusercontent.com/24327781/119707322-a5832b80-be20-11eb-8738-43c0ce862592.png" alt="sMyG54cjeZ" style="zoom:50%;" />

<img src="C:\Users\DHA\Documents\ShareX\Screenshots\2021-05\2AtOg6WzPq.png" alt="2AtOg6WzPq" style="zoom:50%;" />







Also, inside the **Row** widgets, we will have four **Container** widget, and the **Row** widget will lay out these **Container** widgets from left to right. Here we just explain the first row, but we will repeat these steps for other rows. 







 ![dSxkFfkKYa](https://user-images.githubusercontent.com/24327781/119708028-73be9480-be21-11eb-8699-a0988739ce2f.png)



9. Now after we understand how to layout  our widgets. we will start design our first Row. So, we will wrap our container with Row widget. 

   > Note: Use the shortcut [here]() to wrap the widget easily.

<img src="https://user-images.githubusercontent.com/24327781/119709234-98ffd280-be22-11eb-83c3-a4305644ac29.gif" alt="J7QS02BfCf" style="zoom:50%;" />



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

<img src="https://user-images.githubusercontent.com/24327781/119709531-ee3be400-be22-11eb-8fe2-9b52f505c8cf.gif" alt="aDa4h5UPFr" style="zoom:50%;" />





11. We will use the **Column** widget to add other rows for our buttons. So, we need to wrap our **Row** widget with **Column** widget.

<img src="https://user-images.githubusercontent.com/24327781/119709894-57bbf280-be23-11eb-916b-a567535266fd.gif" alt="sFphUz0oOe" style="zoom:50%;" />





12. Also, we will use **SafeArea** widget to avoid intrusions. So, we will add **SafeArea** widget on the top of our **Column** widget.

<img src="https://user-images.githubusercontent.com/24327781/119710125-a073ab80-be23-11eb-996b-710fb8e3d866.gif" alt="l0roVko4rL" style="zoom:50%;" />











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







17.  Use the **mainAxisAlignment** named arguments that inside the **Column** widget, and inside **Row** widget to keep our widget center of the app screen.



<img src="https://user-images.githubusercontent.com/24327781/119711554-496ed600-be25-11eb-97c2-5c88845e3fc3.gif" alt="7VDEPb126g" style="zoom:50%;" />





> Note: the **mainAxisAlignment** for the **Row** widget is different from the **Column** widget because in the **Row** widget the main axis alignment will start from left to right, not from top to bottom.
>
> ![chrome_iRITD3ou2k](https://user-images.githubusercontent.com/24327781/119711925-ad919a00-be25-11eb-82b4-d9ef6903a126.png)









18. After that we will change the text that inside the **Container** widgets. So, keep it same as this picture. You will just need to change each **Text** widget.  

> Note: if you did not find these characters you can copy them from here
>
> `C` `+/-` `%` `÷`



<img src="https://user-images.githubusercontent.com/24327781/119712196-f77a8000-be25-11eb-85a7-7c944c458f62.png" alt="qemu-system-x86_64_rVedjCYZkP" style="zoom:50%;" />





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



<img src="https://user-images.githubusercontent.com/24327781/119712867-adde6500-be26-11eb-9dff-62202fd36661.gif" alt="TF0EB2b47z" style="zoom:50%;" />











<img src="https://media.giphy.com/media/XbxZ41fWLeRECPsGIJ/giphy.gif">





21. Now, you just need to change the color of the other Container, and the text inside it. 

    > So, the final result:

    <img src="https://user-images.githubusercontent.com/24327781/118665352-daa3d400-b7b7-11eb-9ecb-b4d8e3091a62.png" alt="img" style="zoom:33%;" />

    

    

    
    
    
    
    <img src="https://media.giphy.com/media/xC2xDbvyN0tkT7EcPM/giphy.gif" style="zoom:50%;" >
    
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
    
    
    
    
    
    
    
    > Code: 
    
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
    
    













> **Note: You can find the full source code [here](https://github.com/Northwest-content/flutter_calculator_ui_app).**



















































