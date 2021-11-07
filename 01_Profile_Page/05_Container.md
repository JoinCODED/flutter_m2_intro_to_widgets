# **Container**

There are many use cases for **Container** widget. We will get to know them in future lessons. But now we will learn about two cases of use.



18. We can use the **Container** widget, to align the widget inside the layout widget such as **Column** and **Row** widgets. In our case, we will align our image widget to be in the center of the home screen. So, we will **alignment** named argument inside the Container widget, and this named argument takes the **Alignment** object.

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







