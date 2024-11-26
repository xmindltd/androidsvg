# AndroidSVG

AndroidSVG is a SVG parser and renderer for Android.  It has almost complete support for the static
visual elements of the SVG 1.1 and SVG 1.2 Tiny specifications (except for filters).

*AndroidSVG is licensed under the [Apache License v2.0](http://www.apache.org/licenses/LICENSE-2.0)*.

[More information, including downloads and documentation, is available at the main AndroidSVG site.](http://bigbadaboom.github.io/androidsvg/)


### Find a bug?

Please file a [bug report](https://github.com/BigBadaboom/androidsvg/issues) and include as much detail as you can.
If possible, please include a sample SVG file showing the error.

If you wish to contact the author with feedback on this project, you can email me at
[androidsvgfeedback@gmail.com](mailto:androidsvgfeedback@gmail.com).


### Using AndroidSVG in your app?

If you have found AndroidSVG useful and are using it in your project, please let me know. I'd love to hear about it!

### Install

1. Download latest aar at [Github Release](https://github.com/xmindltd/androidsvg/releases)
2. Move aar into libs folder
```
app/
├── libs/
│   └── androidsvg-aar-1.6.aar
```
3. Add the following to your `app/build.gradle` file:
```gradle
repositories {
    flatDir {
        dirs 'libs'
    }
}
dependencies {
    implementation(name:'androidsvg-aar-1.6', ext:'aar')
}
```

If you use `coil-svg` to parse svg file, remember to exclude the `com.caverock` package
because it will conflict with our aar dependency:
```gradle
api(libs.coil.svg) {
    exclude(group="com.caverock")
}
```