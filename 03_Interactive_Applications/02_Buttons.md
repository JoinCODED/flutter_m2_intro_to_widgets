# Buttons



![screenshot](https://lh3.googleusercontent.com/fYHrszVlofKouua7Oy3Wsa3CujcWI0l_PuqPlDXmLvCrZeCNRpQ70xNYTklZFh1MJfOeBe4xKV3tRnLSrt6kVsRjMQxFBwCzs8FjuwPGswCEtpoIL-8U7-6qvZQCqLlNQbkcHrq_)



You can see buttons everywhere, button to send a message, and a button to call a friend, and a button to share an instagram story with a friend. After you tap the button you expect the application to repsond with some sort of actions, like navigate you to another screen, or does something in the screen. We call this action a `function`, and we're going to learn in this module how to create functions. 



We have different types of buttons, and the most important ones are:

		1. **Elevated button**
		1. **Text button**
		1. **Outlined button**



```dart
@override
 Widget build(BuildContext context) {
   return Center(
     child: TextButton(onPressed: onPressed, child: child),
   );
 }
```



Now you need to fill 2 things, **onPressed**, and child. let's start with the child. Add a simple **Text** widget. 

```dart
@override
 Widget build(BuildContext context) {
   return Center(
     child: TextButton(onPressed: onPressed, child: Text("Press me!")),
   );
 }
```



Now if you try to run the app, it wouldn't work. You need to give `onPressed` a proper value. For now just add this `(){}`. Calm down, calm down! I know, I know, it looks weird. But just hang on there. We're gonna explain what this is, just let the app work! 

class MyHomePage extends StatelessWidget {

```dart
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: TextButton(
          onPressed: () {},
          child: Text("Text Button"),
        ),
      ),
    );
  }
}
```



Now save, YUPPPEEE it's wooooorrkiiiing!              



We have an amazing beautiful button!

 
