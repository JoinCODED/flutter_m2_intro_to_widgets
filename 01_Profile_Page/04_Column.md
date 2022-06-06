What if you want to display other information such as Name, Gender, and Hobbies? As you know, these pieces of information will be represented as texts, so you need to use the **Text** widget.

1. In order to display these Widgets (Image, Text) from top to bottom, you need to use a layout widget called **Column**, which allows you to display widgets in a vertical array.

![screenshot](https://lh4.googleusercontent.com/DPzKxyPdRA8SzxucTXXFo7hdRDQtod3MDF2Pw-1cbb50-2Mk_fHzaU2rA_Ilo62K8cP_TjufEyEGlXQKyFjMIWKe-uYH-4aMCfN63hYZ6V27cAIO7JbCZmyhGHGHt3aYHuPWjp-M)

2. To use the **Column** widget, you have to wrap the cat **image** widget with a **Column** widget.

  <!-- The below note needs a gif to be clearer -->
   > Note: you can use the shortcut (Mac): `CMD + .` or (Windows): `Control + .` inside VSCode to wrap the widget.


<!-- flan named argument => الargument الي نمسيه كذا -->
 The **Column** widget requires a property called *children*, which is basically an array that takes a list of widgets to be rendered, these widgets are separated by commas and displayed vertically on the screen according to the order listed in the *children* array.

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

3. To change the alignment of the widgets, you can use **`mainAxisAlignment`** and **`crossAxisAlignment`** named arguments inside the **`Column`** widget. 
   
  - The **`mainAxisAlignment`** named argument is used to arrange children widgets into a vertical format according to the given axis. 
  - The **`crossAxisAlignment`** named argument is used to arrange children widgets into a horizontal format according to a given axis. 
   <!-- It would be great if you add a link that takes you to these properties docs, so the students can have a full understanding of what do they do -->


   ![screenshot](https://lh5.googleusercontent.com/xwkK3tUDTEF8oSsQ5VLngVu-6lUQWy60XoopIIBOMVsgnbjrF1yJt-h5DfFyIkjcGPbNulL9Ixw623Nl9WTBuhPjECVXdSHt73CmuApNqV9K3Ayp9w5y5zRzOLOvro7Jtk0dv5OZ)

   In your case, you are going to use **`mainAxisAlignment`** and give it **`MainAxisAlignment.start`**. This will place *children* at the start point of the main axis.
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

4. You will notice when you use `MainAxis.start`, everything moves to the top of the screen, and the content on mobile is going to be cropped because of the mobile safe area. If you use an iPhone X and higher, you have the notch. In order to avoid the notch area (safe area), use the **`SafeArea`** widget at the top of the **`Column`** widget.

```dart
SafeArea(
  child: Column(
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
      ),)
```