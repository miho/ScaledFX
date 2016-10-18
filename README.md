# ScaledFX
[![Build Status](https://travis-ci.org/miho/ScaledFX.svg?branch=master)](https://travis-ci.org/miho/ScaledFX) [ ![Download](https://api.bintray.com/packages/miho/ScaledFX/ScaledFX/images/download.svg) ](https://bintray.com/miho/ScaledFX/ScaledFX/_latestVersion)

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
        ScalableContentPane scp = new ScalableContentPane();
        scp.setContent(new Button("Scaled Button"));
        
        Scene scene = new Scene(scp);
        
        primaryStage.setScene(scene);
        primaryStage.setTitle("Scalable Content Pane Demo");
        primaryStage.show();
    }
}
```

