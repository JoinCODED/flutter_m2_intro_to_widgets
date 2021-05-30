# Profile Page

In this lesson, we will create a profile page app. 

We will learn how to use these new Widgets: 

**Image.asset**
**Column**
**Row**
**Container**

<img src="https://user-images.githubusercontent.com/24327781/118644950-f00f0300-b7a3-11eb-8093-b97eb2819a3f.png" alt="img" width="250" />





1.  We need to create a new flutter project called "**profile_page_app**"

> Note: to create a new flutter project, review `01_Create_new_Flutter_project`



2. After that, we will remove the code that is inside **main.dart**, then we will copy the code down, and paste it inside **main.dart** file.

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



4. To change the background color for our home screen. We will use the **backgroundColor** named argument that inside the **Scaffold** widget.

```dart
Scaffold(
      backgroundColor: Colors.orange,
    );
```

<img src="https://user-images.githubusercontent.com/24327781/119657008-00049380-bdf1-11eb-8f83-97f0c759da5d.gif" alt="kV7tt8uisA"width="300" />



## Image



5. Now, we will add a cat image inside our app ^_^.



6. In order to display an image inside our app, first we need to create a new folder called **assets**, and inside this folder, we will create another folder called **images**; this folder will have all images that we will use it in our app. So, we will add the cat image inside the **images** folder. 

   > Download the image from this [link](https://raw.githubusercontent.com/Northwest-content/flutter_profile_page_app/main/assets/images/profile.png?token=AFZTMZMPTZSYHKF6DP5JOK3AVY5JY)



<img src="https://user-images.githubusercontent.com/24327781/119657755-ec0d6180-bdf1-11eb-886e-66fb29913e61.gif" alt="Yqcpk8BMiB" width="600" />





7. After adding the image, we must tell the Flutter where the path of the cat image is. So, to do that we will edit the **pubspec.yaml** file. Inside this file, we will add the path for our cat image.

   > Note: when you add another new image, you will need to add its path down other image paths.

   ```ruby
     assets:
     - assets/images/profile.png
   ```

   <img src="https://user-images.githubusercontent.com/24327781/119658500-d3ea1200-bdf2-11eb-8b7f-c14e9c6562b1.png" alt="qmdhqrsmxo" width="600" />





8. Then, we will save the changes inside **pubspec.yaml** file by clicking 
   - Windows: **Ctrl + S**
   - Mac: **Command + S**



> Note:  if save **pubspec.yaml**, the vscode will pop up this dialog 
>
> ![Code_lnAMt3lPcE](https://user-images.githubusercontent.com/24327781/119659084-71dddc80-bdf3-11eb-8b56-bc99e034b4fb.png)



9. **Important**: when you are editing **pubspec.yaml** file, you will need to rerun the app.





10. To display the cat image, we will use the **Image.asset** widget, this widget will help us to show the image inside our app. Inside this widget, we will add our cat image path.

```dart
Scaffold(
      backgroundColor: Colors.orange,
      body: Image.asset(
        'assets/images/profile.png',
      ),
    );
```



<img src="https://user-images.githubusercontent.com/24327781/119659652-fd576d80-bdf3-11eb-961e-35b61e86d385.gif" alt="J54xFIO8Zo" width="600" />







11. To resize our image, we will use **widget** and **height** named arguments inside the image.asset widget.

```dart
Image.asset(
        'assets/images/profile.png',
        width: 200,   // <- here
        height: 200,  // <- here
      )
```











## Column



12. Now, we want to show other information such as Name, Gender, and Hobbies.  As you know, this information will be a text, so we will use the **Text** widget.





13. To add these Widgets (Image widget, Name widget, Gender widget, Hobbies widget) from top to down, we will use a layout widget, called **Column**; This widget will help us to add any widgets from top to down.

<img src="https://user-images.githubusercontent.com/24327781/119660674-21677e80-bdf5-11eb-940e-07c6d5bd05d1.png" alt="2EooCicdkK" width="400" />



14. So, we will wrap our cat **image** widget with **Column** widget. Easily, you can use the shortcut [here]() that inside VSCode to wrap the widget.

```dart
Column(
        children: [
          Image.asset(
            'assets/images/profile.png',
            width: 200,
            height: 200,
          ),
        ],
      )
```

> Note: Column widget takes **children** named argument, and inside children, we will add our widgets that we want to show it from top to bottom. So, the first widget inside the children will be at the top, and the last one will be at the bottom. 

### Row

This is a layout widget, and you can use **Row** widget to add your widgets from left to right.

> For example,  
>
> ```dart
> Row(children: [
>             Text(
>               'Text1',
>             ),
>             Text(
>               'Text2',
>             ),
>             Text(
>               'Text3',
>             ),
>           ],
>         )
> ```
>
> That will show these text widgets from left to right, same as the picture down
>
> ![qemu-system-x86_64_xL1p9zEch5](https://user-images.githubusercontent.com/24327781/119663780-4c9f9d00-bdf8-11eb-8a73-273299bdb543.png)
>
> 



15. In our case we will use the **Column** widget, so we will add the text widgets (name, gender, and hobbies) inside the Column. 

```dart
Column(
        children: [
          Image.asset(
            'assets/images/profile.png',
            width: 200,
            height: 200,
          ),
          Text(
            'Name: Cat Show',
          ),
          Text(
            'Gender: Male',
          ),
          Text(
            'Hobbies: Acting and Fencing',
          ),
        ],
      ),
```

<img src="https://user-images.githubusercontent.com/24327781/119661642-1c56ff00-bdf6-11eb-9080-7c3ad11240da.png" alt="qemu-system-x86_64_CC2EZ4L7L4" width="200" />



16. To change the alignment of our widgets, we can use **mainAxisAlignment** named arguments that inside the **Column** widget. The **mainAxisAlignment** named argument tales **MainAxisAlignment** object. In our case, we will use the start one `MainAxisAlignment.start`

    ![chrome_Ar7aXkDVvg](https://user-images.githubusercontent.com/24327781/119662226-c59df500-bdf6-11eb-8b21-0e646b7b3a45.png)

    ```dart
    Column(
            mainAxisAlignment: MainAxisAlignment.start,      // <- Here
            children: [
              Image.asset(
                'assets/images/profile.png',
                width: 200,
                height: 200,
              ),
              Text(
                'Name: Cat Show',
              ),
              Text(
                'Gender: Male',
              ),
              Text(
                'Hobbies: Acting and Fencing',
              ),
            ],
          ),
    ```

    

17. We will use the **SafeArea** widget to avoid intrusions. So, we will add **SafeArea** widget on the top of our **Column** widget.

    > Note: Use the shortcut [here]() to wrap the widget easily.

```dart
Scaffold(
      backgroundColor: Colors.orange,
      body: SafeArea(      // <- Here
        child: Column(
          mainAxisAlignment: MainAxisAlignment.start,
          children: [
            Image.asset(
              'assets/images/profile.png',
              width: 200,
              height: 200,
            ),
            Text(
              'Name: Cat Show',
            ),
            Text(
              'Gender: Male',
            ),
            Text(
              'Hobbies: Acting and Fencing',
            ),
          ],
        ),
      ),
    );
```









## Container



There are many use cases for Container widget. We will get to know them in future lessons. But now we will learn about two cases of use. 





18. We can use the **Container** widget, to align the widget inside the layout widget such as **Column** and **Row** widgets.  In our case, we will align our image widget to be in the center of the home screen. So, we will **alignment** named argument inside the **Container** widget, and this named argument takes the **Alignment** object.

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

<img src="https://user-images.githubusercontent.com/24327781/119666042-9b4e3680-bdfa-11eb-95f1-1d6ed3b60f51.gif" alt="J3WzhOtVz1" width="600" />







19. Also, we will use the **Container** widget to align other text widgets, and we will keep them on left screen.

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

<img src="https://user-images.githubusercontent.com/24327781/119666521-10217080-bdfb-11eb-87aa-9e037fff762d.png" alt="qemu-system-x86_64_8qQwX6Jr0X" width="250" />







20. The other use case for the **Container** widget is to add a **margin** and **padding** between the Container widget and its child.

![chrome_8MS83Z9ofk](https://user-images.githubusercontent.com/24327781/119667023-86be6e00-bdfb-11eb-96e0-43c32f132a7e.png)

So, in our case we will add margin for our image, and padding for the text widgets.

> Note: if you want to add margin, you need to use **margin** named argument inside the **Container** widget, and if you want to add padding you will use **padding** named argument inside the **Container** widget. Both of these named arguments take **EdgeInsets** object.



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









21. The last thing, we don't like the style of our text widgets. 

<img src="https://media.giphy.com/media/67SXeoc8RLwvqCwn2F/giphy.gif">

    

    

    So, we will change them by using the **TextStyle** object inside **Text** widget. 



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





The final result  :

<img src="https://user-images.githubusercontent.com/24327781/119668114-7f4b9480-bdfc-11eb-92d5-46a9eb56bc0c.png" alt="qemu-system-x86_64_ePpJIkLnbV" width="200" />





Finally, 

<img src="https://media.giphy.com/media/XbxZ41fWLeRECPsGIJ/giphy.gif">









> **Note: You can find the full source code [here](https://github.com/Northwest-content/flutter_profile_page_app).**
