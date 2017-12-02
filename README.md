[![Build Status](https://travis-ci.org/madjestic/Haskell-OpenGL-Tutorial.svg?branch=master)](https://travis-ci.org/madjestic/Haskell-OpenGL-Tutorial)

# Haskell-OpenGL-Tutorial
=======================
an attempt to create a concise modern Haskell OpenGL boilerplate with basic IO among other things...

## [MandelbrotYampa](https://github.com/madjestic/Haskell-OpenGL-Tutorial/tree/master/MandelbrotYampa)

### Output:
![](https://raw.github.com/madjestic/Haskell-OpenGL-Tutorial/master/MandelbrotYampa/output.png)

### Animated Output:
![](https://raw.github.com/madjestic/Haskell-OpenGL-Tutorial/master/MandelbrotYampa/output.gif)

## [Sugarising the interface with polymorphic functions.](https://github.com/madjestic/Haskell-OpenGL-Tutorial/tree/master/tutorial05)

![](https://raw.github.com/madjestic/Haskell-OpenGL-Tutorial/master/tutorial05/tutorial05.png)

```haskell
module Main where

import NGL.Shape
import NGL.Rendering

main :: IO ()
main = do
     let drawables = [toDrawable Red     $ Square (-0.5, -0.5) 1.0,
                      toDrawable Green   $ Circle (0.5, 0.5) 0.5 100,
                      toDrawable Blue    $ Rect (-1.0,0.33) (0.0,0.66),
                      toDrawable White   $ Polyline [ (0.0,-0.66)
                                                     ,(0.33,-0.33)
                                                     ,(0.66,-0.66)
                                                     ,(1.0,-0.33)] 
                                                       0.01 
                     ]

     window <- createWindow "NGL is Not GLoss" (512,512)
     drawIn Default window drawables
     closeWindow window
```


