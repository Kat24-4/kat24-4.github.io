# Assignment 1 - Shader Live Coding Explanations

## Technical 

Coming into this assignment, I really wanted to play with what transformations and variations I could do to one shape. I started with a circle. I used clamp() to animate the circle appearing to my desired size. I also utilized the length() and smoothstep() functions to create a nicely shaped circle. Next, I used the sin() and fma() functions to add a pulse to the circle and I used min() to help me stop  the circle at my desired position along the y axis. Once I was happy with that, I played around with tan() and cos() to move the circle around the screen on multiple axes. By using feedback, I was able to play around with color. I tried decreasing the blue value through the saturate() function. I also tried slowly increasing red by combining the fract() and asin() functions. The end of my animation utilized the techniques I used at the beginning just in reverse. 

**List of Functions Used**: sin(), length(), smoothstep(), tan(), cos(), distance(), step(), min(), saturate(), fract(), asin(), fma(), clamp()

## Aesthetic 

My aesthetic goal for this project was to try and visualize what it feels like to panic or overthink things. It starts with the shape appearing and slowly starting to pulse faster and faster which is to mimic hyperventilation or the idea of thoughts starting to race. Then it moves to a brief moment of calm when the circle moves up which mirrors this idea of a brief calm before the storm. Next, the circle starts to move more sporadically and begins to drag a trail of color behind it. The color starts more mild but slowly becomes redder and redder. This is meant to symbolize this idea of racing thoughts  that get darker or more dreadful (think of what people describe as spiraling).  Lastly, the racing white circles are replaced by a pulsing black circle on the red background. This demonstrates the idea of the final through that then truly consumes all else just how the animation ends with the black circle growing and taking over. 

## Feedback
