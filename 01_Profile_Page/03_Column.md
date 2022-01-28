1. Now, we want to show other information such as Name, Gender, and Hobbies. As you know, this information will be a text, so we will use the Text widget.

2. To add these Widgets (Image widget, Name widget, Gender widget, Hobbies widget) from top to down, we will use a layout widget, called **Column**; This widget will help us to add any widgets from top to down.

![screenshot](https://lh4.googleusercontent.com/DPzKxyPdRA8SzxucTXXFo7hdRDQtod3MDF2Pw-1cbb50-2Mk_fHzaU2rA_Ilo62K8cP_TjufEyEGlXQKyFjMIWKe-uYH-4aMCfN63hYZ6V27cAIO7JbCZmyhGHGHt3aYHuPWjp-M)

3. So, we will wrap our cat **image** widget with a Column widget.

   > Note: you can use the shortcut (Mac): `CMD + .` or (Windows): `Control + .` that is inside VSCode to wrap the widget.

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

> Note: **Column** widget takes **`children`** named argument, and inside children, we will add the widgets that we want to show it from top to bottom. So, the first widget inside the `children` will be at the top, and the last one will be at the bottom.
