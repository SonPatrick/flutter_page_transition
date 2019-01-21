# Flutter Page Transition Package

This package gives you beautiful page transitions.
<br/><br/>

[![flutter platform](https://img.shields.io/badge/Platform-Flutter-yellow.svg)](https://flutter.io) 
[![pub package](https://img.shields.io/pub/v/page_transition.svg)](https://pub.dartlang.org/packages/page_transition) 
[![BSD-2-Clause](https://img.shields.io/badge/BSD-2-Clause.svg?style=flat-square)](https://opensource.org/licenses/) 

## Demo
<img src="http://www.yasinilhan.com/page_transition/transition.gif" width="320" height="600" title="Screen Shoot">

## Usage
It is really easy to use!
You should ensure that you add the `page_transition` as a dependency in your flutter project.

```yaml
dependencies:
  page_transition: '^1.0.7'
```
Than you can use it with below examples.

```dart 
Navigator.push(context, PageTransition(type: PageTransitionType.fade, child: DetailScreen()));

Navigator.push(context, PageTransition(type: PageTransitionType.leftToRight, child: DetailScreen()));

Navigator.push(context, PageTransition(type: PageTransitionType.rightToLeft, child: DetailScreen()));

Navigator.push(context, PageTransition(type: PageTransitionType.upToDown, child: DetailScreen()));

Navigator.push(context, PageTransition(type: PageTransitionType.downToUp, child: DetailScreen()));

Navigator.push(context, PageTransition(type: PageTransitionType.scale, alignment: Alignment.bottomCenter, child: DetailScreen()));

Navigator.push(context, PageTransition(type: PageTransitionType.size, alignment: Alignment.bottomCenter, child: DetailScreen()));

Navigator.push(context, PageTransition(type: PageTransitionType.rotate, duration: Duration(second: 1), child: DetailScreen()));

Navigator.push(context, PageTransition(type: PageTransitionType.rightToLeftWithFade, child: DetailScreen()));

Navigator.push(context, PageTransition(type: PageTransitionType.leftToRightWithFade, child: DetailScreen()));
```

## Usage for predefined routes
First, define the `onGenerateRoute` property in the `MaterialApp` widget like below and in switch cases you can transition to your new routes:

```dart 
  onGenerateRoute: (settings) {
    switch (settings.name) {
      case '/second':
        return PageTransition(child: SecondPage(), type: PageTransitionType.scale);
        break;
      default:
        return null;
    }
  },
```

After that you can use your new route like this:

```dart 
Navigator.pushNamed(context, '/second'); 
```


## Types of transitions
* fade
* rightToLeft
* leftToRight
* upToDown
* downToUp
* scale (with alignment)
* rotate (with alignment)
* size (with alignment)
* rightToLeftWithFade,
* leftToRightWithFade,

## Curves 
You can use any type of CurvedAnimation [curves](https://docs.flutter.io/flutter/animation/Curves-class.html). 

## Alignments 
You can use size, scale and rotate transform [alignment](https://docs.flutter.io/flutter/painting/Alignment-class.html)

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
The MIT License (MIT) Copyright © 2018 YasinIlhan
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


