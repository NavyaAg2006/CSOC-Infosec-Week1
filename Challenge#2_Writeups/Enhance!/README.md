# Enhance!
## Challenge Description
_Download this image file and find the flag._
## Walkthrough
So we have been given an svg image file which is plain text. So let's run the strings command. We see some text appearing to be like flag within `<tspan>`. Hence, let's run-
```bash
strings drawing.flag.svg | grep tspan
```
We get the result
```js
id="text3723"><tspan
         id="tspan3748">p </tspan><tspan
         id="tspan3754">i </tspan><tspan
         id="tspan3756">c </tspan><tspan
         id="tspan3758">o </tspan><tspan
         id="tspan3760">C </tspan><tspan
         id="tspan3762">T </tspan><tspan
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         id="tspan3752">c 3 d _ a a b 7 2 9 d d }</tspan></text>
```
## Flag
**picoCTF{3nh4nc3d_aab729dd}**
