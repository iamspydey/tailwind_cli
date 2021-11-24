# Tailwind CLI
A simple yet awesome flutter package to generate and use TailwindCSS like
styling in your flutter projects.

### Inspiration
* [Tailwind CSS](https://tailwindcss.com/)
* [VelocityX](https://velocityx.dev)

**Note: Actually ```VelocityX``` has the similar feature and has more feature than just UI but we have something which ```VelocityX``` don't have.**

#### How ```Tailwind CLI``` is different than ```VelocityX```
* Firstly ```Tailwind CLI``` is not a styling itself. Rather it is a tool to generate tailwind styles in your project.
* Also ```VelocityX``` provides a lot of features including ```Kind of tailwind``` styling but not fully featured.
* In ```Tailwind CLI``` you can use your own configuration to get more custom styling as ```Tailwind``` itself provide you to extend the framework. So by using ```Tailwind CLI``` you can have that freedom. But as i personally used and checked ```VelocityX``` they don't have this feature.
* Also in ```VelocityX``` you can not provide individual spacing for Horizontal and Vertical Axis. Because it overrides the previously provided spacing.
* But in ```Tailwind CLI``` you can provide individual spacing Horizontaly and Verticaly or even all side individually.
*



#### Highlights
This will provide basic styling just like Tailwind provides in which
it is providing you ```Colors```, ```Gradient Colors```, Sizing ```(Padding, Margins)```,
```Roundness```, ```Shadows```, ```Font Sizes```, ```Font styling``` Etc.

## Getting Started

Install package
```bash
flutter pub add tailwind_cli
```

Now publish the ```tailwind.config.json``` file
```bash
flutter pub run tailwind_cli:init
```
Publishing ```tailwind.config.json``` file will create a config file for Tailwind styles.


Build / Generate tailwind styling
```bash
flutter pub run tailwind_cli:build
```

Add tailwind in your project's ```pubspec.yaml``` file under ```dependencies``` section
```yaml
dependencies:
  flutter:
    sdk: flutter
    
  # Tailwind
+  tailwind:
+    path: tailwind
```

Now install generated tailwind styles in your project
```bash
flutter pub get
```

***Now your project is ready to use Tailwind stylings***

## Features
This is mainly focused to provide you an easy way to style your pages and UI in your flutter projects because as everyone knows that it takes developer to write a lot of code to achieve just a small UI. So we are here to rescue you and provides you a lighning speed to build beautiful UI withour writing a lot of code.

## Here what you can do with the tailwind package

### Containers and Boxes

```TwContainer``` provides you a ```Container``` Widget as a wraper your UI and will provide all the ```Tailwind``` styling.

| Tw Container  | Flutter Container |
| ------------- | ------------- |
| TwContainer()  | Container()  |

You can directly use ```TwCotainer``` or ```Container``` with ```twContainer``` extension to be able to use extension for styling your container as ```Tailwind``` use classes. Extensions on the flutter will feel similar as ```Tailwind``` utility classes.

#### Example

```dart
    TwContainer(
        child: Text("I am a Tailwind styled Container.")
            .twText /// Will return as TwText Widget to apply tailwind styles
            .white /// sets font color to white
            .render(), /// Renders the Text Widget in page
    ).py8 /// Apply 32px / 2rem (4 * 8 = 32px) padding Vertically
    .px4 /// Apply 16px / 1rem (4 * 4 = 16px)padding Horizontally
    .render(),
```







