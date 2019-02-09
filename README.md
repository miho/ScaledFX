# ScaledFX
[![Build Status](https://travis-ci.org/miho/ScaledFX.svg?branch=master)](https://travis-ci.org/miho/ScaledFX) [ ![Download](https://api.bintray.com/packages/miho/ScaledFX/ScaledFX/images/download.svg) ](https://bintray.com/miho/ScaledFX/ScaledFX/_latestVersion) [![Javadocs](https://www.javadoc.io/badge/eu.mihosoft.jfx.scaledfx/scaledfx.svg?color=blue)](https://www.javadoc.io/doc/eu.mihosoft.jfx.scaledfx/scaledfx)


JavaFX pane for scaling arbitrary content nodes (used in Vworkflows) by applying scale transformations. The `ScalableContentPane` scales its content to always fit the container bounds.  

![Sample 1](https://media.giphy.com/media/l3vR99nMoId6DEOeA/giphy.gif)

![Sample 2](https://media.giphy.com/media/XvKr0mGNGtP8I/giphy.gif)

**Sample Code:**

```java

public class Main extends Application {
    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        launch(args);
    }

    @Override
    public void start(Stage primaryStage) throws Exception {
        ScalableContentPane scp = 
            new ScalableContentPane(new Button("Scaled Button"));
        
        primaryStage.setScene(new Scene(scp));
        primaryStage.setTitle("Scalable Content Pane Demo");
        primaryStage.show();
    }
}
```

## Notes on JDK >=11

Version `>= 0.5` is compatible with JDK >= 11. Just use the [JavaFx Gradle plugin](https://openjfx.io/openjfx-docs/#gradle) via

```gradle
plugins {
  id 'org.openjfx.javafxplugin' version '0.0.7' // use latest version
}
```

and declare the dependency to the `controls` module.

```gradle
javafx {
    modules = [ 'javafx.controls' ]
}
```

## Notes on JDK 8

Version `<= 0.4` is compatible with JDK 8 (probably also 9 and 10)
