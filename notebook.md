# My Coding Notebook

## Table of Contents
- [Flutter Notes](day-1)
  - [What is Flutter](#what-is-flutter)
  - [Practice](#practice)
- [Key Terms and Definitions](#key-terms-and-definitions)
-  [Code Definitions](#code-definitions)
[Notebook Style Guide](#markdown-style-guide-for-coding-notebooks)

## Flutter Notes

### What is Flutter?
- Definition: A framework made by Google for building apps that works on web, android, and IOS - with one codebase
- Why is it useful? Uses the Dart programming language 

---

### Key Terms and Definitions

| Term             | Definition                                      | Example / Notes                          |
|------------------|--------------------------------------------------|-------------------------------------------|
| Variable  | A named container used to store a value that may change.  ||  |      |
| Widget           | Basic building block of a Flutter app. Everything is a widget.             Text, Image, Container, Column       
| MaterialApp      |The root of the app. Sets up routes and themes.                             Found in main. dart                     |                                           |
| Scaffold         |Provides basic visual layout - like a header, body, floating button         Each screen uses it                                         |                                           |
| StatelessWidget  |A widget that doesn't change                                                Most of the screen files                                           |
| StatefulWidget   |A widget that can change over time                                          Used in MyHomePage ()        |                                           |
| Navigator        |Manages screen transitions                                                  Navigator.pushNamed(context, '/page2') ;                                           |
| AppBar           |Top navigation bar                                                  |       Title of each page appears here | |
| Column           |                                                  |                                           |
| Row              |                                                  |                                           |
| Container        |                                                  |                                           |
| Text             |                                                  |                                           |
| Image.network    |                                                  |                                           |
| Padding    |                    |                     |
| Center      |                    |                     |

---

### Layout and Design Widgets
- How do you center a widget?
- How do you align something to the left or right?
- What widget adds space around content?



[Flutter Definitions](#flutter_definitions)

 

## Flutter Definitions

| Term | Definition and Description | Base Structure | Real Life Example | App Example |
|------|----------------------------|----------------|-------------------|-------------|
| main()     | A function that runs when your app starts. It tells Flutter what app to show. | `void main() => runApp(MyApp());` |Like turning on a TV and choosing which channel (app) to watch.  |in main.dart, void main() => runApp (MyPortfolioApp());  |
|MaterialApp      | The widget that sets up your whole app’s look and navigation. | `MaterialApp(...)` |Like the frame or theme for a building.  |return MaterialApp(home: HomeScreen());  |
|Scaffold      | A widget that gives you the basic layout: background, navigation bar, floating button, etc. | `Scaffold(...)` |Like the structure of a house with rooms and floors.  | return Scaffold( body: Center(  |
|Column      | A widget that holds and displays your content in a straight line from top to bottom. | `Column(...)` |A stack of boxes or books.  |Column(children: [Text("One"), Text("Two")])  |
|Row      | A widget that shows things side-by-side. | `Row(...)` |A row of chairs.  |Row(children: [Icon(Icons.star), Text("Star")])  |
|Container      | A box that holds other widgets. You can add color, padding, borders, or size. | `Container(...)` |A box you decorate and put things inside.  |Container(padding: EdgeInsets.all(10), color: Colors.blue)  |
|Text      | A widget to display text on the screen. | `Text('Hello')` |A sign or label.  |Text("Welcome to my app")  |
|Image.network      | A widget to show an image using a link from the internet. | `Image.network('https://...')` |A digital photo frame that loads images from online.  |Image.network('https://example.com/photo.jpg')  |
|ElevatedButton      | A clickable button that floats above content. You choose what happens when it's clicked. | `ElevatedButton(onPressed: ..., child: ...)` |A doorbell – when you press it, something happens.  |ElevatedButton(onPressed: () {}, child: Text("Click Me"))  |
|onPressed      | The code that gets run when a button is tapped or something happens. | `onPressed: () => doSomething()` |Pressing a button to play music.  |ElevatedButton(onPressed: () => print("Hello"), child: Text("Tap"))  |
|StatelessWidget      | A class that creates widgets that never change. Good for static screens. | `class HomeScreen extends StatelessWidget` |A poster on a wall – doesn’t change.  |class AboutPage extends StatelessWidget { ... }  |
|StatefulWidget      | A class for widgets that can change while the app is running. | `class MyWidget extends StatefulWidget` |A remote control – its state (channel/volume) changes.  |class CounterApp extends StatefulWidget { ... }  |
|Navigator.pushNamed      | Lets you move from one screen to another using route names. | `Navigator.pushNamed(context, '/about')` |Going into a different room in a house.  |Navigator.pushNamed(context, '/settings')  |
|Padding      | Makes space around a widget inside its container. | `Padding(padding: EdgeInsets.all(8.0), child: ...)` |Bubble wrap around a gift.  |Padding(padding: EdgeInsets.all(16), child: Text("Padded text"))  |
|Center      | Aligns content in the center of the screen or container. | `Center(child: ...)` |Placing a photo frame exactly in the center of a wall.  |Center(child: Text("Centered"))  |
|Wrap      | Automatically puts widgets onto a new line when there's no space. | `Wrap(children: [...])` |Wrapping presents into multiple rows if one is full.  |Wrap(children: [Chip(label: Text("Tag1")), Chip(label: Text("Tag2"))])  |
|@override      | This marks a method as one that’s replacing a method in a parent class. | `@override` |Customizing a recipe to make your own version.  |@override Widget build(BuildContext context) {...}  |
|build()      | The special function in every widget that describes what gets drawn on the screen. | `Widget build(BuildContext context) {...}` |A blueprint for a room layout.  |Widget build(BuildContext context) { return Text("Hello"); }  |
|build      | Required in every widget class to describe what to show. | `build` |A recipe that tells how to prepare a dish.  |@override build(BuildContext context) => ...  |
|BuildContext      | A variable that helps the widget know where it is and lets it communicate with the app. | `BuildContext context` |A map that tells where you are in a mall.  | Used in: build(BuildContext context) |
|super.key      | A keyword used to pass a value to the parent widget. | `super.key` |Giving your name tag when entering a building.  |const MyHomePage({super.key});  |
|const      | A keyword that means the value won't change and is set once. | `const` |A permanent label on a product.  |const Text("This won’t change")  |



## Code Definitions 

| Term | Definition | Base Structure / Syntax | Real Life Example | App Example |
|------|------------|--------------------------|-------------------|-------------|
| Variable | A named container used to store a value that may change. | `var x = 5;` |A labeled jar that you can put different things into.  | Storing the number of items in a shopping cart. |
|   Constant   | A fixed value that cannot change once set. | `const PI = 3.14;` |The number of hours in a day (24).  |Defining the max number of login attempts.  |
|   Data Type   | The kind of value a variable holds, like numbers or text. | `int`, `String`, `bool` |Labels like “fruit” or “tool” that define item categories.  |Choosing between storing user name (String) or age (int).  |
|    String  | A sequence of characters used to represent words or text. | `"Hello World"` |A sentence written on a sign.  |Displaying a welcome message on the home screen.  |
|   Integer   | Whole number values. | `int age = 16;` |Counting the number of books on a shelf.  |Tracking user’s steps in a fitness app.  |
| Double     | Number values with decimals. | `double age = 16.2;` |Measuring weight like 65.5 kg.  |Storing product price in an e-commerce app.  |
|     Boolean | A value that can be true or false. | `bool isLoggedIn = false;` |Light switch (on/off).  |Checking if user is logged in to enable features.  |
|  List    | A collection of values in a specific order. | `List<String> names = [];` |Grocery shopping list.  |A list of chat messages or contacts in a messaging app.  |
|  Null    | A special value that means “nothing.” | `String? name = null;` |An empty parking spot.  |A user who hasn't set a profile picture (null image).  |
| Function     | A reusable block of code that performs an action. | `void sayHi() { print("Hi"); }` |A microwave that always heats food when used.  |A function that sends an email when a user signs up.  |
| Parameter     | The information passed into a function to change how it works. | `greet(String name)` |Telling a barista your name for the coffee cup.  |Passing a user’s name into a greeting message function.  |
| Return     | The result a function gives back. | `return total;` |Asking for the total cost and getting the amount.  |A function that returns the result of a quiz.  |
|  Scope    | Where a variable or function can be used. | (No set syntax — concept-based) |Tools in a toolbox can only be used where it’s carried.  |A variable that exists only inside a button’s click function.  |
| Class     | Blueprint for creating objects with specific structure and behavior. | `class Dog {}` |A blueprint for building houses.  |A User class with properties like name, email, and methods like login().  |
|Object      | A specific version of a class. | `Dog myDog = Dog();` |A specific house built from the blueprint.  |A user named “John” created from the User class.  |
|Property      | A variable that belongs to a class/object. | `String name;` |A car’s color or engine size.  |A user’s email or profilePicture stored as properties.  |
|Method      | A function that belongs to a class. | `void bark() {}` |A car’s “start” or “stop” button.  |A User class method like logOut().  |
|Constructor      | A special function used to set up a class when it’s created. | `Dog(this.name);` |Filling in a form to create a new ID card.  |Initializing a User with name and email during sign-up.  |
|Abstraction      | Hiding the inner workings of code so users only interact with what they need. | (Concept — not specific code) |Driving a car without knowing how the engine works.  |Using a payment method without seeing its backend implementation.  |
|Override      | Changing how a built-in or inherited function behaves. | `@override` |Customizing a uniform to fit your style.  |Overriding a button’s onPressed() function to show a custom alert.  |
|Void      | A function that does not return a value. | `void printMessage() {}` |Turning off the lights — you don’t expect a result.  |A function that shows a toast message when a task is complete.  |








## Markdown Style Guide for Coding Notebooks

Follow this guide to keep your coding notebook **clear, consistent, and professional**.  
This ensures your notes are easy for you (and others) to read later.

---

## 🔹 Headings
**When to use:** Organize your notebook into sections (like days, topics, or projects).  
- `#` for the notebook title (use once at the top).  
- `##` for each day or major topic.  
- `###` for subsections (like "Notes", "Practice", "Reflections").  

✅ Example:


# My Coding Notebook
## Day 1
### Notes
### Practice

🔡 Text Formatting
When to use: Highlight important ideas or add emphasis.

Use bold for key terms or definitions.

Use italic for emphasis or side comments.

Use inline code for keywords, functions, or commands.

 

✅ Example:

**Class** = a blueprint for objects  
*Remember:* always test your code  
Use `System.out.println()` to print

 

💻 Code Blocks
When to use: Anytime you write multiple lines of code.

Inline code for short snippets.

Fenced code blocks with language for full examples.

✅ Example:

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

🧾 Lists
When to use: Organize steps, notes, or key points.

Numbered lists for sequences or steps.

Bulleted lists for unordered ideas.

✅ Example:

1. Define the class
2. Write the main method
3. Test your program

Variables
- Loops
- Conditionals
 

✅ Checklists
When to use: Track progress on assignments or tasks.

✅ Example:

[x] Complete coding warm-up
- [ ] Finish project draft
- [ ] Reflect on learning

 

➡️ Blockquotes
When to use: Call out notes, reminders, or teacher comments.

✅ Example:

> 💡 Remember: Loops repeat code until a condition is false.

 

📊 Tables
When to use: Compare values, track progress, or organize data neatly.

✅ Example:

| Task        | Status   | Notes          |
|-------------|----------|----------------|
| Homework 1  | Done ✅  | Submitted      |
| Homework 2  | Pending  | Needs review   |

 

🔗 Links & Images
When to use: Add references, resources, or visuals.

✅ Example:

[Java Docs](https://docs.oracle.com/javase/8/docs/api/)  
![Markdown Logo](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)

 

📂 Collapsible Sections
When to use: Hide solutions, extended notes, or extra details.

✅ Example:

<details>
  <summary>Click to reveal solution</summary>
  
System.out.println("Answer: 42");

</details>

 

📝 Footnotes
When to use: Add references or side notes without cluttering the page.

✅ Example:

This concept is related to object-oriented programming.[^1]

[^1]: See "Objects and Classes" in your textbook.

 

🎯 Style Rules
Consistency matters more than creativity

Always use headings to structure your notes.

Always use code blocks for multi-line code.

Clarity first

Bold key terms.

Use lists instead of long sentences when outlining steps.

Professional tone

Don’t mix casual notes with formal work in the same section.

Use blockquotes for reflections or teacher feedback.

Track your learning

Use checklists to mark what’s done.

Use collapsible sections if you want to hide answers until review time.

 

✅ Bottom Line:

Headings = Structure

Bold/Italic = Emphasis

Code blocks = Code

Lists = Steps/Ideas

Tables = Organization

Checklists = Progress

Blockquotes = Notes/Tips

Collapsible = Hide/Show detail

Keep it simple, consistent, and clear.
