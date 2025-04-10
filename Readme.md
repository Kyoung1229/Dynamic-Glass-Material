# Dynamic Glass Material is glassy, translucent material(view), written in SwiftUI.

## Key features
- Dynamic lighting based on device's orientation
- Color temperature adjustment based on real time
- Automatic adjustments of radius for lighting and shadows based on it's size
- Automatic adaption for 4 types of screen directions(Portrait, Portrait Upside Down, Landscape Left, Landscape Right) with no stuttering.

## Parameters
- cornerRadius
- width
- height

- gyro: input for GyroManager. (see GyroManager.swift)

- edgeMode: the type of lighting. 
    - .automatic: strongly recommended. automatically adjusts lighting and strokes based on the size of the rectangle.
    - .fixed: depreciated. fixes both lighting and stroke.
    - .dynamic: depreciated. acts like .automatic, but scale of lighting and stroke may not be consistant for different sizes. it also could have broken details.

- xoffset(-1.0 ~ 1.0): offset for lighting of x directions. negative for left, positive for right.
- yoffset(-1.0 ~ 1.0): offset for lighting of y directions. negative for down, positive for up.

- movementIntensity(> 1, default: 1.0): how much will lighting react for movements.
- lightingIntensity_edge(> 1, default: 1.0): Intensity(or brightness) of edge lighting.
- lightingIntendify_surface(> 1, default: 1.0): Intensity(or brightness) of surface lighting.

- hour(default: current time, Double): hour for the color temperature adjustments. 