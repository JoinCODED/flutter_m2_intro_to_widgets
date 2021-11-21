# Box Decoration 





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



![screenshot](https://user-images.githubusercontent.com/24327781/119705628-9ac79700-be1e-11eb-80e8-3a6ed548415b.gif)



7. After that we will add **Text** widgets inside the child that inside the **Container** widget. 

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



> Also, we will add a style for our **Text** widget
>
> ```dart
> Text(
>          '+',
>          style: TextStyle(         // <- here
>            fontSize: 24,
>            color: Colors.green, 
>          ),
>        ),
> ```









































