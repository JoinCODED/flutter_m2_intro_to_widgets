
This is a layout widget, and you can use the **Row** widget to add your widgets from left to right.



For example, 

```dart
Row(children: [
        Text(
          'Text1',
        ),
        Text(
          'Text2',
        ),
        Text(
          'Text3',
        ),
      ],
    )
```



That will show these text widgets from left to right, same as the picture down

![screenshot](https://lh5.googleusercontent.com/os-d_wqbv1zHz_bvOfCDCdMHN06Am6MShgsBK0jHnl9YkEEYC21_M7yGK3ShrjHbbbwzwORvNB7aPF9cCrKz0YHdWoV9wIhW54pqrfimVz_HaigFKLd98-7K2Z54hc29xLjfTNVy)



15. In our case we will use the **Column** widget, so we will add the text widgets (name, gender, and hobbies) inside the **Column**

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



![screenshot](https://lh5.googleusercontent.com/QZEzYmQFrm308dmIIUTGsMzknU-WsGngcNywz3f2-SUnW9tT-1f3eEP55uw4V-ByfaEtb_sieFSVHOCJrgnvxRSxa3HYi3kPJKTJQJ2QoGAkxJKGb0OqPczIBy0Y0YuLgqa9Z9F3)







16. To change the alignment of our widgets, we can use **mainAxisAlignment** named arguments inside the **Column** widget. The **mainAxisAlignment** named argument tales **MainAxisAlignment** object. In our case, we will use the start one **MainAxisAlignment.start**.
![screenshot](https://lh5.googleusercontent.com/xwkK3tUDTEF8oSsQ5VLngVu-6lUQWy60XoopIIBOMVsgnbjrF1yJt-h5DfFyIkjcGPbNulL9Ixw623Nl9WTBuhPjECVXdSHt73CmuApNqV9K3Ayp9w5y5zRzOLOvro7Jtk0dv5OZ)



```dart
Column(
        mainAxisAlignment: MainAxisAlignment.start, // <- Here
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



17. We will use the SafeArea widget to avoid intrusions. So, we will add the **SafeArea** widget on the top of our **Column** widget.

    > Note: Use the shortcut [here](https://github.com/Northwest-content/flutter_m1_intro_to_flutter/blob/master/02_run_first_app/02_VSCode_guide.md) to wrap the widget easily.

























