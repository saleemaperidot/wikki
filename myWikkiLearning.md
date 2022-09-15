# Dart (programming language)

From Wikipedia, the free encyclopedia

*For the advertising application formerly called Google Dart, see DoubleClick for Publishers by Google.*

**Dart** is a programming language designed for client development, [[8]](https://dart.dev/overview)[[9]](https://dart.dev/) such as for the web and mobile apps. It is developed by Google and can also be used to build server and desktop applications.

It is an [object-oriented](),[ class-based](), [garbage-collected]()language with C-style syntax.[[10]]() It can [compile]() to either [native code]() or [JavaScript](), and supports [interfaces](), [mixins](), [abstract classes](),[reified generics]() and [type inference].[[11]]()

>#### contents
    >1. [History](https://en.wikipedia.org/wiki/Dart_(programming_language)#History)
    >
    >2. [Usage]()
    >
    >3.	[Isolates]()
    >
    >4.	[Snapshots]()
    >
    >5.	[Native mobile apps]()
    >
    >6.	[Compiling to JavaScript]()
    >
    >7. [Editors]()
    >
    >    7.1. [Chrome Dev Editor]()
    >
    >    7.2. [DartPad]() 
    >
    >8.	[SIMD]()
    >
    >9. [Example]()
    >
    >10. [Influences from other languages]()
    >
    >11.	[See also]()
    >
    >12.	[References]()
    >
    >13.	[Bibliography]()
    >
    >14.	[External links]()


# History

Dart was unveiled at the GOTO conference in [Aarhus](), Denmark, October 10–12, 2011.[[12]]() The project was founded by [Lars Bak ]()and Kasper Lund.[[13]]() Dart 1.0 was released on November 14, 2013.[[14]]()

Dart initially had a mixed reception and the Dart initiative has been criticized by some for fragmenting the web, due to the original plans to include a Dart VM in Chrome. Those plans were dropped in 2015 with the 1.9 release of Dart to focus instead on compiling Dart to JavaScript.[[15]]()



Dart 2.0 was released in August 2018, with language changes including a sound type system.[16]

Dart 2.6 introduced a new extension, dart2native, which extends native compilation to the Linux, macOS, and Windows desktop platforms. Earlier developers could create new tools using only Android or iOS devices. With this extension it also becomes possible to compose a program into self-contained executables. According to company representatives, it’s no longer necessary to have the Dart SDK installed, as the self-contained executables can now start running in a few seconds. The new extension is also integrated with the [Flutter]() toolkit, making it possible to use the compiler on small services (for example, backend support).[[17]]()[[18]]()

## Standardization
Ecma International has formed technical committee TC52[19] to work on standardizing Dart, and inasmuch as Dart can be compiled to standard JavaScript, it works effectively in any modern browser. EI approved the first version of the Dart language specification in July 2014 at its 107th General Assembly,[20] and a second edition in December 2014.[21] The latest specification is available here.

# Usage
There are four ways to run Dart code:

## Web
To run in mainstream web browsers, Dart relies on a source-to-source compiler to JavaScript. According to the project site, Dart was "designed to be easy to write development tools for, well-suited to modern app development, and capable of high-performance implementations."[22] In a web browser, the code is precompiled into JavaScript using the dart2js compiler, making it compatible with all major browsers with no need for browsers to adopt it. By optimizing the compiled JavaScript output to avoid expensive checks and operations, code written in Dart can, in some cases, run faster than equivalent code handwritten in JavaScript idioms.[23]

## Stand-alone
The Dart software development kit (SDK) ships with a stand-alone Dart VM, allowing Dart code to run in a command-line interface environment. As the language tools included in the SDK are written mostly in Dart, the Dart VM is a critical part of it. These tools include the dart2js compiler and a package manager called pub. Dart ships with a complete standard library allowing users to write fully working system apps, such as custom web servers.[24]

## Ahead-of-time compiled
Dart code can be AOT-compiled into machine code (native instruction sets). Apps built with Flutter, a mobile app SDK built with Dart, are deployed to app stores as AOT-compiled Dart code.[25]
## Native
Dart 2.6 includes the dart2native compiler to compile to self-contained, native executable code. Before Dart 2.6, this feature exposed this capability only on iOS and Android mobile devices via Flutter.[26]

# Isolates

To achieve concurrency, Dart uses isolates, independent workers that do not share memory, but use message passing,[27] similarly to Erlang processes (also see actor model). Every Dart program uses at least one isolate, which is the main isolate. Since Dart 2, the Dart web platform no longer supports isolates, and suggests developers use Web Workers instead.[28]

# Snapshots

Snapshots, a core part of the Dart VM, are files that store objects and other runtime data.[27]

## Script snapshots
Dart programs can be compiled into snapshot files containing all of the program code and dependencies preparsed and ready to execute, allowing fast startups.
## Full snapshots
The Dart core libraries can be compiled into a snapshot file that allows fast loading of the libraries. Most standard distributions of the main Dart VM have a prebuilt snapshot for the core libraries that is loaded at runtime.
## Object snapshots
Dart is a very asynchronous language, using isolates for concurrency. Since these are workers that pass messages, it needs a way to serialize messages. This is done using a snapshot, which is generated from a given object, then transferred to another isolate for deserializing.

# Native mobile apps

Google has introduced Flutter for native mobile app development on Android, iOS and Windows.[29] Flutter is a mobile app SDK, complete with framework, widgets, and tools, that gives developers a way to build and deploy mobile apps, written in Dart.[30] Flutter works with Firebase[31] and other mobile app SDKs, and is open source.

# Compiling to JavaScript

The Dart SDK contains two Dart-to-JavaScript compilers. During development, dartdevc supports quick refresh cycles. For the final version of an app, dart2js produces deployable JavaScript.[32]

The first compiler to generate JavaScript from Dart code was dartc, but it was deprecated. The second Dart-to-JavaScript compiler was Frog. It was written in Dart, but never implemented the full semantics of the language. The third Dart-to-JavaScript compiler was dart2js. An evolution of earlier compilers, dart2js is written in Dart and intended to implement the full Dart language specification and semantics.

On March 28, 2013, the Dart team posted an update on their blog addressing Dart code compiled to JavaScript with the dart2js compiler,[33] stating that it now runs faster than handwritten JavaScript on Chrome's V8 JavaScript engine for the DeltaBlue benchmark.[34]

# Editors
On November 18, 2011, Google released Dart Editor, an open-source program based on Eclipse components, for macOS, Windows, and Linux-based operating systems.[35] The editor supports syntax highlighting, code completion, JavaScript compiling, running web and server Dart applications, and debugging.

On August 13, 2012, Google announced the release of an Eclipse plugin for Dart development.[36]

On April 18, 2015, Google announced that the Dart Editor would be retired in favor of the JetBrains integrated development environment (IDE),[37] which is now the recommended IDE for the language. The Dart plugin[38] is available for IntelliJ IDEA, PyCharm, PhpStorm and WebStorm. This plugin supports many features such as syntax highlighting, code completion, analysis, refactoring, debugging, and more. Other plugins are available for editors like Sublime Text, Atom, Emacs, Vim and Visual Studio Code.[39]

## Chrome Dev Editor
In 2013, the Chromium team began work on an open source, Chrome App-based development environment with a reusable library of GUI widgets, codenamed Spark.[40] The project was later renamed as Chrome Dev Editor.[41] It was built in Dart, and contained Spark which is powered by Polymer.[42]

In June 2015, Google transferred the CDE project to GitHub as a free software project and ceased active investment in CDE.[43] As of April 2019 Chrome Dev Editor is no longer in active development.[44]

## DartPad
The Dart team created DartPad at the start of 2015, to provide an easier way to start using Dart. It is a fully online editor from which users can experiment with Dart application programming interfaces (APIs), and run Dart code. It provides syntax highlighting, code analysis, code completion, documentation, and HTML and CSS editing.[45]

# SIMD

In 2013, John McCutchan announced[46][non-primary source needed] that he had created a performant interface to single instruction, multiple data (SIMD) instruction sets for Dart.

The interface consists of two types:

* Float32×4, 4× single precision floating point values

* Uint32×4, 4× 32-bit unsigned integer values

Instances of these types are immutable and in optimized code are mapped directly to SIMD registers. Operations expressed in Dart typically are compiled into one instruction with no overhead. This is similar to C and C++ intrinsics. Benchmarks for 4×4 matrix multiplication, 3D vertex transformation, and Mandelbrot set visualization show near 400% speedup compared to scalar code written in Dart.

# Example
A Hello, World! example:

```Dart
void main() {
  print('Hello, World!');
}
```

A function to calculate the nth Fibonacci number:

```Dart
int fib(int n) => (n > 2) ? (fib(n - 1) + fib(n - 2)) : 1;
// A Fibonacci function implementation with a conditional operator in Dart
// This code is read as:
//  given an integer n,
//  if n > 2, return fib(n - 1) + fib(n - 2); 
//  otherwise, return the integer 1 as result

void main() {
  print('fib(20) = ${fib(20)}');
}
```

A simple class:

```Dart
// Import the math library to get access to the sqrt function.
// Imported with `math` as name, so accesses need to use `math.` as prefix.
import 'dart:math' as math;

// Create a class for Point.
class Point {

  // Final variables cannot be changed once they are assigned.
  // Declare two instance variables.
  final num x, y;

  // A constructor, with syntactic sugar for setting instance variables.
  // The constructor has two mandatory parameters.
  Point(this.x, this.y);

  // A named constructor with an initializer list.
  Point.origin()
      : x = 0,
        y = 0;

  // A method.
  num distanceTo(Point other) {
    var dx = x - other.x;
    var dy = y - other.y;
    return math.sqrt(dx * dx + dy * dy);
  }
  
  // Example of a "getter".
  // Acts the same as a final variable, but is computed on each access.
  num get magnitude => math.sqrt(x * x + y * y);

  // Example of operator overloading
  Point operator +(Point other) => Point(x + other.x, y + other.y);
  // When you instantiate a class such as Point in Dart 2+, new is 
  // an optional word
}

// All Dart programs start with main().
void main() {
  // Instantiate point objects.
  var p1 = Point(10, 10);
  print(p1.magnitude);
  var p2 = Point.origin();
  var distance = p1.distanceTo(p2);
  print(distance);
}
```

# Influences from other languages
Dart is a descendant of the ALGOL language family,[47] alongside C, Java, C#, JavaScript, and others.

The method cascade syntax, which provides a syntactic shortcut for invoking several methods one after another on the same object, is adopted from Smalltalk.

Dart's mixins were influenced by Strongtalk[citation needed][48] and Ruby.

Dart makes use of isolates as a concurrency and security unit when structuring applications.[49] The Isolate concept builds upon the Actor model, which is most famously implemented in Erlang.

The Mirror API for performing controlled and secure reflection was first proposed in a paper[50] by Gilad Bracha (who was a member of the Dart team) and David Ungar and originally implemented in Self.

# See also

* Google Web Toolkit
* TypeScript, a strongly-typed programming language that transpiles to JavaScript

# References

