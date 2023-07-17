# Flutter_doc_CokBK_Des_Display_snackbar
 https://docs.flutter.dev/cookbook/design/snackbars
Display a snackbar
==================

1.  [Cookbook](https://docs.flutter.dev/cookbook)
2.  [Design](https://docs.flutter.dev/cookbook/design)
3.  [Display a snackbar](https://docs.flutter.dev/cookbook/design/snackbars)

It can be useful to briefly inform your users when certain actions take place. For example, when a user swipes away a message in a list, you might want to inform them that the message has been deleted. You might even want to give them an option to undo the action.

In Material Design, this is the job of a [`SnackBar`](https://api.flutter.dev/flutter/material/SnackBar-class.html). This recipe implements a snackbar using the following steps:

1.  Create a `Scaffold`.
2.  Display a `SnackBar`.
3.  Provide an optional action.

[](https://docs.flutter.dev/cookbook/design/snackbars#1-create-a-scaffold)1\. Create a `Scaffold`
-------------------------------------------------------------------------------------------------

When creating apps that follow the Material Design guidelines, give your apps a consistent visual structure. In this example, display the `SnackBar` at the bottom of the screen, without overlapping other important widgets, such as the `FloatingActionButton`.

The [`Scaffold`](https://api.flutter.dev/flutter/material/Scaffold-class.html) widget, from the [material library](https://api.flutter.dev/flutter/material/material-library.html), creates this visual structure and ensures that important widgets don't overlap.

content_copy

```
return MaterialApp(
  title: 'SnackBar Demo',
  home: Scaffold(
    appBar: AppBar(
      title: const Text('SnackBar Demo'),
    ),
    body: const SnackBarPage(),
  ),
);
```

[](https://docs.flutter.dev/cookbook/design/snackbars#2-display-a-snackbar)2\. Display a `SnackBar`
---------------------------------------------------------------------------------------------------

With the `Scaffold` in place, display a `SnackBar`. First, create a `SnackBar`, then display it using `ScaffoldMessenger`.

content_copy

```
const snackBar = SnackBar(
  content: Text('Yay! A SnackBar!'),
);

// Find the ScaffoldMessenger in the widget tree
// and use it to show a SnackBar.
ScaffoldMessenger.of(context).showSnackBar(snackBar);
```Display a snackbar
Cookbook
Design
Display a snackbar
It can be useful to briefly inform your users when certain actions take place. For example, when a user swipes away a message in a list, you might want to inform them that the message has been deleted. You might even want to give them an option to undo the action.

In Material Design, this is the job of a SnackBar. This recipe implements a snackbar using the following steps:

Create a Scaffold.
Display a SnackBar.
Provide an optional action.
1. Create a Scaffold
When creating apps that follow the Material Design guidelines, give your apps a consistent visual structure. In this example, display the SnackBar at the bottom of the screen, without overlapping other important widgets, such as the FloatingActionButton.

The Scaffold widget, from the material library, creates this visual structure and ensures that important widgets don’t overlap.

content_copy
return MaterialApp(
  title: 'SnackBar Demo',
  home: Scaffold(
    appBar: AppBar(
      title: const Text('SnackBar Demo'),
    ),
    body: const SnackBarPage(),
  ),
);
2. Display a SnackBar
With the Scaffold in place, display a SnackBar. First, create a SnackBar, then display it using ScaffoldMessenger.

content_copy
const snackBar = SnackBar(
  content: Text('Yay! A SnackBar!'),
);

// Find the ScaffoldMessenger in the widget tree
// and use it to show a SnackBar.
ScaffoldMessenger.of(context).showSnackBar(snackBar);
