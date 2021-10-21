## Animation
An animation is simply a way to interpolate values of properties in a finite interval of time. Useful information:

- To define an animation, you use the `animation` property, followed by some values.

The shorthand syntax is:

```
<single-animation>#
where 
<single-animation> = <time> || <easing-function> || <time> || <single-animation iteration-count> || <single-animation-direction> || <single-animation-fill-mode> || single-animation-play-state> || [ none | <keyframes-name> ]

where 
<easing-function> = linear | <cubic-bezier-timing-function> | <step-timing-function>
<single-animation-iteration-count> = infinite | <number>
<single-animation-direction> = normal | reverse | alternate | alternate-reverse
<single-animation-fill-mode> = none | forwards | backwards | both
<single-animation-play-state> = running | paused
<keyframes-name> = <custom-ident> | <string>

where 
<cubic-bezier-timing-function> = ease | ease-in | ease-out | ease-in-out | cubic-bezier(<number [0,1]>, <number>, <number [0,1]>, <number>)
<step-timing-function> = step-start | step-end | steps(<integer>[, <step-position>]?)

where 
<step-position> = jump-start | jump-end | jump-none | jump-both | start | end

```