This is a **Snack Bar** (with a space between each word)

![screenshot](https://lh6.googleusercontent.com/ftGxvA6qwZd3OBkYPwIppox_FO1VOGPeQZrJ6tuX95naDCcM-l6Gi_Sn0XqPGuNUICParM7YChRSE1rTk_Fml51UzbdILe-vlfAlKSrnfPvrxZPKdsGL2pCwt6V0BaXx1fXq419j)

And this is a `Snackbar` (with no space between each word)

![screenshot](https://lh3.googleusercontent.com/JXkJKPz2bTfeDIyotbe8071bUCf92mWOIT_0CVNDWxRcaCRl4Em0eATgdcmbDvzUstwGOJWS2y7L4Dfapp_lEZYeGCccCWxo69eucj7JlvdY-gjrF-DE_-1cl0VzQ56RGVZ3dSgF)

A **snackbar** is a useful way to briefly inform your users when certain action take place. For example, when a user swipes away a message in a list, you might want to inform them that the message has been deleted. You might even want to give them an option to undo the action.

To launch a snackbar:

1. Make sure you have a **`Scaffold`**.
2. Display a **`SnackBar`**.

Now, instead of printing in the debug console, let's use the function that will fire a **`snackbar`**.

```dart
ScaffoldMessenger
  .of(context)
  .showSnackBar(SnackBar(content: Text("Hello")));
```

You can place any widget in the `content` inside the `SnackBar` widget. In this case we used a `Text` widget that displays the word `"Hello"`.

Now, the home page should look like this:

```dart
class MyHomePage extends StatelessWidget {
 @override
 Widget build(BuildContext context) {
   return Scaffold(
     body: Center(
       child: TextButton(
         onPressed: () {
           ScaffoldMessenger.of(context)
               .showSnackBar(SnackBar(content: Text("Hello")));
         },
         child: Text("Click me!"),
       ),
     ),
   );
 }
}
```

Save now. Voilà!

![screenshot](https://lh6.googleusercontent.com/r9LWmxCWEJMsqffram4OLMNaDFarVONoLmjasFtB9RQHRt4iX6LNYQBv-xha9lESZbejptYltrtO_BlbeI99DmTWiLps8KkqRlA5rlaQxb2nbY3nvwNbN5IpIR2KglG_OzRYAQGC)
