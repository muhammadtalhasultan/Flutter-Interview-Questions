# Flutter Interview Questions and Answers
This repository provides a list of important/ frequently asked questions for flutter/dart language for mobile application development.

![image](https://user-images.githubusercontent.com/31367048/150833270-88996d8f-3c8c-4c9f-ac49-89331f9a176c.png)


1. What is `Flutter`?

   `Flutter` is an open-source UI software development kit created by Google. It is used to develop applications for Android, iOS, Linux, Mac, Windows, Google Fuchsia, and the web from a single codebase.
   Generally, Flutter is not a language; it is an SDK. Flutter apps use Dart programming language for creating an app. The first alpha version of Flutter was released in May 2017. Flutter is mainly optimized for 2D mobile apps that can run on both Android and iOS platforms. We can also use it to build full-featured apps, including camera, storage, geolocation, network, third-party SDKs, and more.


2. What is `Dart`?

    `Dart` is a general-purpose, object-oriented programming language with C-style syntax. It is open-source and developed by Google in 2011. The purpose of Dart programming is to create a frontend user interfaces for the web and mobile apps. It is an important language for creating Flutter apps. The Dart language can be compiled both AOT (Ahead-of-Time) and JIT (Just-in-Time).


3. Why `Flutter` uses `Dart` as Programming Language?

   Dart is an object-oriented, garbage-collected programming language that you use to develop Flutter apps. It is created by Google. Dart was chosen as the language of Flutter      for the following reason:
   
   i. ***Dart is AOT (Ahead Of Time) compiled*** to fast, predictable, native code, which allows almost all of Flutter to be written in Dart. This makes Flutter fast
   
   ii. ***Dart can also be JIT (Just In Time) compiled*** for exceptionally fast development cycles and game-changing workflow (hot reload).
   
   iii. ***Dart allows Flutter to avoid the need for a separate declarative layout language*** like XML, because Dart’s declarative, programmatic layout is easy to read and visualize. i.e we can do both UI and Buisness Logic using one language only which is ***"DART"***
   
   iv. ***Dart Team + Flutter Team*** As both Dart and Flutter is developed and maintained by Google, hence both Flutter Team and Dart Team work together to solve the problem.  


4. What are the `Flutter widgets`?

    A Flutter app is always considered as a tree of widgets. Whenever you are going to code for building anything in Flutter, it will be inside a widget. Widgets describe how your app view should look like with their current configuration and state. When you made any alteration in the code, the widget rebuilt its description by calculating the difference of previous and current widget to determine the minimal changes for rendering in the app's UI.
    
    Widgets are nested with each other to build the app. It means your app's root is itself a widget, and all the way down is a widget also. For example, a widget can display something, can define design, can handle interaction, etc.

5. What are the `different types of widgets in Flutter`?
   
    There are types of widgets present in the Flutter which are `Stateless` and `Stateful`.

    `Stateless` widgets do not require mutable state. As the name suggests the stateless widgets do not store any values that will change in future.  
    The stateless widgets don’t store any state. 
    For example : Icon, text widgets.

    `Stateful` widgets have mutable state. The stateful widgets have a state object to keep track of all the changes and updates happening in the UI. 
    These widgets are immutable but the state object is used to keep track of the changes. 
    For example : Checkbox and image widgets.
    
6. What is the difference between `Stateful` widget and `Stateless` widget?

    Stateless widgets cannot change their state during the runtime of the app, 
    which means the widgets cannot be redrawn while the app is in action. 
    
    Stateful Widgets are the ones that change its properties during run-time. 
    They are dynamic i.e. they are mutable and can be drawn multiple times within its lifetime.
    
7. What is `setState()` ?
   
  setState notifies the framework that the internal state of an object has changed in a way that might impact the user interface in this subtree, which causes the framework to schedule a build for this State object. If we just change the state directly without calling setState, the framework might not schedule a build and the user interface for this subtree might not be updated to reflect the new state.
  It is recommended that the setState method only be used to wrap the actual changes to the state, not any computation that might be associated with the change.


8. What is the use of `pubspec.yaml` file in Flutter?

    The `pubspec.yaml` file allows you to define the packages your app relies on, declare your assets like font, images, audio, video, etc. 
    For Android developers, this is roughly similar to a `build.gradle` file.
   

9: What is the difference between `main()` and `runApp()` functions in Flutter?

   The `main()` function came from Java-like languages so it's where all program started, without it, you can't write any program on Flutter even without UI.
   
   The `runApp()` function should return widget that would be attached to the screen as a root of the widget Tree that will be rendered.
   

10. What is `hot reload` in flutter?

   Flutter’s hot reload feature helps you quickly and easily experiment, build UIs, add features, and fix bugs. Hot reload works by injecting updated source code files into the running `Dart Virtual Machine (VM)`. After the VM updates classes with the new versions of fields and functions, the Flutter framework automatically rebuilds the widget tree, allowing you to quickly view the effects of your changes.


10. What’s the difference between `hot reload` and `hot restart`?
    
    Hot reload maintains the app state while updating the UI almost instantaneously whereas Hot restart resets the app state to its initial conditions before updating the UI.


11. What is an App State?

    State that is not *ephemeral*, that you want to share across many parts of your app, and that you want to keep between user sessions, is what we call **application state** (sometimes also called *shared state*).
          
    Examples of application state:
    *   User preferences
    *   Login info
    *   Notifications in a social networking app
    *   The shopping cart in an e-commerce app
    *   Read/unread state of articles in a news app
 
12. What are the different build modes in Flutter? 
    
    The Flutter tooling supports three modes when compiling your app, and a headless mode for testing. 
        You choose a compilation mode depending on where you are in the development cycle.
        The modes are:
    	* Debug
    	* Profile
    	* Release
    	
13. What is the difference between `NetworkImage` and `Image.network` in flutter?

   `NetworkImage` class creates an object the provides an image from the src URL passed to it. It is not a widget and does not output an image to the screen.
   `Image.network` creates a widget that displays an image on the screen. It is just a named constructor on the Image class (a stateful widget). It sets the image property using the NetworkImage . This image property is used finally to display the image.

14. What is use of `Navigation.push` and `Navigation.pop` function? 
   
    The `push` method is used to add a route to the stack of routes managed by the navigator. The `pop` method is used to remove the current route from the stack of routes managed by the navigator.

15. When do you use double.INFINITY?

    `double.INFINITY` is used to by the child widget to occupy the remaining height of the parent widget.
    
16. What is the difference between Expanded and Flexible widgets?

    `Expanded` is just a shorthand for `Flexible`

    Using expanded this way:
    ```dart
    Expanded(
        child: Foo(),
    );
    ```
    is strictly equivalent to:
    ```dart
    Flexible(
        fit: FlexFit.tight,
        child: Foo(),
    );
    ```
    
    You may want to use `Flexible` over `Expanded` when you want a different `fit`, useful in some responsive layouts.
    
    The difference between `FlexFit.tight` and `FlexFit.loose` is that loose will allow its child to have a maximum size while tight forces that child to fill all the available space.
    
       
17. What is Fat Arrow Notation in Dart and when do you use it?

    The fat arrow syntax is simply a short hand for returning an expression and is similar to `(){ return expression; }`.
    
    The fat arrow is for returning a single line, braces are for returning a code block.
    
    Only an expression—not a statement—can appear between the arrow (`=>`) and the semicolon (`;`). For example, you can’t put an *if* statement there, but you can use a *conditional* expression
    ```dart
    // Normal function
    void function1(int a) {
      if (a == 3) {
        print('arg was 3');
      } else {
        print('arg was not 3');
      }
    }
    
    // Arrow Function
    void function2(int a) => print('arg was ${a == 3 ? '' : 'not '}3');
    ```
    
18. What is ***ScopedModel/BLoC Pattern?***
    
    `ScopedModel` and `BLoC (Business Logic Components)` are common Flutter app architecture patterns to help separate business logic from UI code and using fewer Stateful Widgets.

    * `Scoped Model` is a third-party package that is not included into Flutter framework. It's a set of utilities that allow you to easily pass a data Model from a parent Widget down to its descendants. In addition, it also rebuilds all of the children that use the model when the model is updated. This library was originally extracted from the Fuchsia codebase.
   
    * `BLoC` stands for Business Logic Components. It helps in managing state and make access to data from a central place in your project. The gist of BLoC is that everything in the app should be represented as stream of events: widgets submit events; other widgets will respond. BLoC sits in the middle, managing the conversation.


19. What is `BuildContext` and how is it useful?

   BuildContext is actually the widget's element in the Element tree — so every widget has its own BuildContext.
   You usually use BuildContext to get a reference to the theme or to another widget. For example, if you want to show a material dialog, you need a reference to the scaffold. You can get it with Scaffold.of(context), where context is the build context. of() searches up the tree until it finds the nearest scaffold.


20. What is the difference between `WidgetsApp` and `MaterialApp`?
       
       `WidgetsApp` provides basic navigation. Together with the `widgets` library, it includes many of the foundational widgets that Flutter uses.
       `MaterialApp` and the corresponding `material` library is a layer built on top of `WidgetsApp` and the widgets library. It implements Material Design, which gives the app a unified look and feel on any platform or device. The `material` library has many additional widgets that come with it.
       You certainly aren’t required to use `MaterialApp` in your project. You can use `CupertinoApp` to make iOS users feel at home, or you can even build your own set of custom widgets to fit your brand.


21. Can you nest a `Scaffold`? Why or why not?

   Yes, you can absolutely nest a `Scaffold`. That’s the beauty of Flutter. You control the entire UI.
   `Scaffold` is just a widget, so you can put it anywhere a widget might go. By nesting a `Scaffold`, you can layer drawers, snack bars and bottom sheets.


22. What is the purpose of `SafeArea` in Flutter?

    `SafeArea` is an important and useful widget in Flutter which makes UI dynamic and adaptive to a wide variety of devices. While designing the layout of widgets, we consider different types of devices and their pre-occupied constraints of screen like status bar, notches, navigation bar, etc.


23. When is it appropriate to use packages, plugins or third-party dependencies?

   Packages and plugins are great for saving you time and work. There’s no need to solve a complex problem yourself when someone else has done it already, especially if the solution is highly rated.
   On the other hand, there’s also a danger of being too reliant on third party packages. They can break, have bugs or even be abandoned. When you need to switch to a new package down the road, you might have to make huge changes to your code.
   That’s why it’s important to isolate packages from your core business logic. You can do that by creating an abstract Dart class that acts as an interface for the package. Once you’ve set up that kind of architecture, all you have to do to switch packages is to rewrite the concrete wrapper class that implements your interface.

24. How do you `talk to native code` from within a Flutter app?

   One type of platform channel is a method channel. Data is serialized on the Dart side and then sent to the native side. You can write native code to interact with the platform before sending a serialized message back. That message might be written in Java or Kotlin on Android or Objective-C or Swift on iOS.
   The second type of platform channel is the event channel, which you use to send a stream of data from the native platform back to Flutter. This is useful for monitoring sensor data.

25. What is the use of having `Android and iOS folders` in the Flutter project?

   Android:  This folder is meant for holding an entire Android project.  This will come into usage when you want to build a Flutter application for the Android platform. When you compile a Flutter code into the native code, it will enter into the Android project and gives you a native Android application.
   
   iOS: This folder is meant for holding an entire Mac project. This will come into usage when you want to build a Flutter application for the iOS platform. It works similarly to the Android folder. When you compile a Flutter code into the native code, it will enter into the Android iOS project and gives you a native Android application. Building a Flutter application will only be possible when you work on Xcode IDE and macOS.

26. Explain `async`, `await`, `then` and `Future` in Dart?

   * Async means that this function is asynchronous and you might need to wait a bit to get its result. <br />
   * Await literally means - wait here until this function is finished and you will get its return value. <br />
   * .Then((value){…}) is a callback that’s called when future completes successfully(with a value). <br />
   * Future is a type that ‘comes from the future’ and returns value from your asynchronous function. It can complete with success(.then) or with an error(.catchError). <br />

27. What is `profile mode` and when do you use it?
   
   In profile mode, some debugging ability is maintained—enough to profile your app’s performance.
   Profile mode is used when you want to analyze performance.
   Profile mode is disabled on the emulator and simulator, because their behavior is not representative of real performance.
   On mobile, profile mode is similar to release mode, with the following differences: - Some service extensions, such as the one that enables the performance overlay, are enabled. - Tracing is enabled, and tools supporting source-level debugging (such as DevTools) can connect to the process.
   Profile mode for a web app means that: - The build is not minified but tree shaking has been performed. - The app is compiled with the dart2js compiler.
   The command flutter run --profile compiles to profile mode.
   
28. What types of `tests` can you perform?

   There are three main kinds of tests: unit tests, widget tests and integration tests. Unit tests are all about checking the validity of your business logic. Widget tests are for making sure UI widgets have the components that you expect them to. Integration tests check that your app is working as a whole.
   One additional type of test that is not as well known is a golden test. In a golden test, you have an image of a widget or screen and check to see that the actual widget matches it.


29. List some approaches for State management in Flutter.

    * setState()
    * Provider
    * BLoC / Rx
    * Redux
    * Fish-Redux
    * GetIt
    * MobX
    * GetX
    * Riverpod

30. What is the difference between debug mode, profile mode and release mode?

    * Use debug mode during development, when you want to use hot reload.
    * Use profile mode when you want to analyze performance.
    * Use release mode when you are ready to release your app.
    
31. What are mixins in `dart`?

    Mixins are used for a unique kind of inheritance, they allow other classes to inherit it's baked in methods for use, without actually being a child of the parent Mixin class. In simple words, Mixins are our usual normal classes from which we can borrow methods, without extending the class.
  
32. What are the two types of Streams available in `Flutter`?

    There are two types of Streams available in Flutter which are: .. *Single subscription streams* .. *Broadcast streams*. Single subscription streams : It is a popular and commom type of stream. It consist of series of events that are parts of a large whole. The events here have to be delivered in a defined order without even missing a single event.

    Broadcast streams : This stream is meant for the individual messages that can be handeled one at a time. Multiple listener can listen at a time and it also gives the user the chance to listen after the cancellation of the previous subscription.
    
33. What is a `Flutter` Inspector ?
    
    Flutter Inspector is a tool that helps in visualizing and exploring the widget trees. It also helps in understanding the present layout and rectify the layout issues.
    
33. What are Null-aware operators in Flutter ?
    
    Dart offers some handy operators for dealing with values that might be null.
    a. One is the ??= assignment operator, which assigns a value to a variable only if that variable is currently null.
    b.Another null-aware operator is ??, which returns the expression on its left unless that expression’s value is null, in which case it evaluates and returns the expression on its right
    

## Notes:

This repository is only for providing information on flutter interview questions. Please do not misuse it. 
This repository is under development. I will keep adding more questions to it. 

## Author:

* [Muhammad Talha Sultan](https://github.com/muhammadtalhasultan)
