# **Image**



5. Now, we will add a cat image inside our app ^_^.



6. To display an image inside our app, first, we need to create a new folder called **assets**, and inside this folder, we will create another folder called **images**; this folder will have all images that we will use it in our app. So, we will add the cat image inside the images folder.

   >  Download the image from this [link](https://raw.githubusercontent.com/Northwest-content/flutter_profile_page_app/main/assets/images/profile.png?token=AFZTMZMPTZSYHKF6DP5JOK3AVY5JY)

![screenshot](https://lh3.googleusercontent.com/q9z8pe0FK5HetzPBcSQfPC82p4DqgT2oQkpiapuLsz88XMTmBH_f0fX8arjJ8E7ChEzEStoS9hme-i6U4NoMGLvx5Lrunl-2fgIb6fYBv8Ds1hnlAnWk5rpJX1fr-OzvphlML1Pf)






7. After adding the image, we must tell the Flutter where the path of the cat image is. So, to do that we will edit the **pubspec.yaml** file. Inside this file, we will add the path for our cat image.

   > Note: when you add another new image, you will need to add its path down other image paths.

   ```yaml
     assets:
     - assets/images/profile.png
   ```

   

8. Then, we will save the changes inside **pubspec.yaml** file by clicking.
   - Windows: **Ctrl + S**
   - Mac: **Command + S**

> Note: if save **pubspec.yaml**, the vscode will pop up this dialog


![screenshot](https://lh5.googleusercontent.com/279IAwnenB5NeEEXtFDFdHocHr_EGSds8cEP7Tg95gPqXKTYQ14O0Kw_bUHDmUXci4alRV-HmXHH4IcThXy-6aaFRCZI4Tulbv0bzPultstu4x76RfaFuoUM4SUVNUHFcXz7oX_K)





9. **Important**: when you are editing **pubspec.yaml** file, you will need to rerun the app.



10. To display the cat image, we will use the Image.asset widget, this widget will help us to show the image inside our app. Inside this widget, we will add our cat image path.

```dart
Scaffold(
     backgroundColor: Colors.orange,
     body: Image.asset(
       'assets/images/profile.png',
    ),
  );
```


![screenshot](https://lh3.googleusercontent.com/8YTTYo04fZZA-yzSqj_axwZ2nlinSXjtGGdY6MoALcLZROdwWxbzU_zPzzK-wKWGSzBHwnPkAU25403KhFaDhExgVlfevfP-stNvT9QBOdcn6OwnXZZUCmN6DO7gfjPRQDXFcp4x)




11. To resize our image, we will use **widget** and **height** named arguments inside the image.asset widget.

    ```dart
    Image.asset(
           'assets/images/profile.png',
           width: 200,   // <- here
           height: 200,  // <- here
        )
    ```

    



















