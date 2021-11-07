# Creating variables

If you see the text style for some of the **Text** widgets, you will note that we were repeating the code many times; the best practice is to make one variable that has the **TextStyle** object and use it inside our Text widgets.  



This practice has two advantages:

​	1.  Will make your code shorter.

​	2. when you want to change the size of text, you will change it one time in one place.





22. Under the 

```dart
class HomeScreen extends StatelessWidget {
```



Create this variable

```dart
 final TextStyle greenTextStyle = TextStyle(
    color: Colors.green,
    fontSize: 24,
  );
```

> Here we created a new variable
> 	its name is **greenTextStyle**
> 	its type is **TextStyle**
>
> Also, we assigned the **TextStyle** object to this variable



23. After that you just need to call this variable, inside your widget tree. 

Replace the **TextStyle** object which has a green color.



For example, replace the **TextStyle** object for the first widget that has the letter **C**





Before: 

```dart
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
                  style: TextStyle(          // <- Here
                    color: Colors.green,
                    fontSize: 24,
                  ),
                ),
              ),
```



After:

```dart
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
                  style: greenTextStyle,  // <- Here
                ),
              ),
```





24. You will need to repeat this steps for other **TextStyle** that has a green color.



25. After that create another variable for the white button. Under the first variable, create this variable.

```dart
 final TextStyle whiteTextStyle = TextStyle(
    fontSize: 24,
  );
```



26. Then call this variable inside the white **Container** widgets. Same as **step 23**.

> Note: for the **Red Container**, you don't need to do this step because you have just one red **Container**. ^_^



27. Adding the Text field Container; Top the **Column** widget, add this **Container** widget.

```dart
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
                // 2
                fontWeight: FontWeight.bold,
              ),
            ),
          ),
```

			1. Here we align the [child] within the **Container** widget.
			1. Thickness (**bold**) the text. 







The final result: 

<img src="https://user-images.githubusercontent.com/24327781/133928283-eab43fd9-056a-40a6-9890-f61221d12c92.png" alt="img" width="250" />



> **Note: You can find the full source code [here](https://github.com/Northwest-content/flutter_calculator_ui_app).**











