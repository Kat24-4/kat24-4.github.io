# Assignment 1 Code 

## Directions
Copy and paste the corresponding code sections into TheSchwartz at each transition movement to display the next section of the animation (ensure you re-load the program to active the new code snippet)

Note: only the first section has in code edits that need to be made 

## Code Sections 
### Fade in circle to circle pulse
Additional Step: delete clamp function and un-comment fma function to start the pulse once the circle is at the smallest size

    var p = uvN( pos.xy );
    p -= vec2(0.5);
  
    let rate = 1 * seconds();

    let radius = clamp(0.4 + seconds() * 0.5, 0.5, 0.9); //fma(0.025, sin(seconds() * rate), 0.875;
    let dist = length(p);

    let circle = smoothstep(radius, radius + 0.003, 1.0 - dist);
    return vec4(1.0, 1.0, 1.0, circle);

### Circle that pulses and moves up on the y-axix
    var p = uvN( pos.xy );
    p -= vec2(0.5);
  
    p.y += min(0.25, seconds() * 0.1);

    let radius = 0.025 * sin(seconds() * 15.0) + 0.875;
    let dist = length(p);

    let circle = smoothstep(radius, radius + 0.003, 1.0 - dist);
    return vec4(1.0, 1.0, 1.0, circle);

### Evil red takes over
    var p = uvN( pos.xy );
    p.x += tan( seconds() ) * .25;
    p.y += cos( seconds() ) * .25;
  
    let circle = 1-step(.1, distance( p, vec2(.5, .5)));
    let feedback = lastframe( rotate( uvN( pos.xy ), seconds()/8 ) );
    var out = circle + feedback * .925;
  
    out.b = saturate(1.0 - seconds() * 0.1) ;
    out.r += fract(asin( seconds() ));

    return out;
### Red backgrund w/ black circle pulsing 
    var p = uvN( pos.xy );
    p -= vec2(0.5);

    let radius = fma(0.025, sin(seconds() * 15.0), 0.875);
    let dist = length(p);

    let circle = smoothstep(radius, radius + 0.003, 1.0 - dist);
    return vec4(1.0, 0.0, 0.0, 1-circle);

### Circle expands to black 
    var p = uvN( pos.xy );
    p -= vec2(0.5);

    let radius = 0.9 - seconds() * 0.5;
    let dist = length(p);

    let circle = smoothstep(radius, radius + 0.003, 1.0 - dist);
    return vec4(1.0, 0.0, 0.0, 1-circle);
