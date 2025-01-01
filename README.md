
# Metal Angle backend for libGDX

A Google [Angle](https://github.com/google/angle) based LWJGL3 backend for libGDX with metal rendering.

## Supported operating systems:

| Operating system | Supported? |
|------------------|------------|
| Windows (x64)    | No[*1]     |
| Linux (x64)      | No[^1]     |
| Mac OS X (x64)   | Yes        |

[^1]: Windows and Linux don't support Metal

## Usage:

Add dependency to your lwjgl3 project:

```groovy
implementation "org.lwjgl:lwjgl-opengles:3.3.4:natives-windows"

api 'com.github.Dgzt:gdx-lwjgl3-metal-angle:1.1.0'
```

Use `Lwjgl3MetalApplication` application in your LWJGL3 launcher class:

```java
import dev.ultreon.gdx.lwjgl3.Lwjgl3ApplicationConfiguration;  
import dev.ultreon.gdx.lwjgl3.Lwjgl3MetalApplication;

...

public class Lwjgl3Launcher {  
    public static void main (String[] arg) {  
       Lwjgl3ApplicationConfiguration config = new Lwjgl3ApplicationConfiguration();
       ...
       config.setOpenGLEmulation(Lwjgl3ApplicationConfiguration.GLEmulation.ANGLE_GLES32, 0, 0);  
       new Lwjgl3MetalApplication(new YourMainClass(), config);
    }
}
```

