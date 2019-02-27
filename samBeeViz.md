# Dev-Des Notes on Samantha Bee Viz project

## 2/27/29
I had to completely rewrite my code to make this cute little effect happen. But I wanted it to make the blazers look more fun, and less rigid. After all, if I'm going to use colorful blazers in a graph, I might as well have fun with it.

What was a difficulty? It all comes down to how svg paths behave if they come from an external file (external to the javascript). 

After much research and coding experiments...I decided to go with an in-line svg element instead. I had the original svg, and cloned it for each instance. Then I set the original svg visibility to 'hidden'.   It's not what I wanted to do, but it works.

For some reason, which I don't yet understand, I could not apply a rotate transform to an externally loaded svg. 

Getting the rotate and positional transform to work on a custom svg shape had it's own challenges, but I was finally able to get it to work. 

As a side benefit, I massively simplified my code.

It's still an early in the experiment, but I'm already finding  differences between how firefox and chrome render the same code. I'll have to handle these, eventually.

The main visual difference is the spacing of the svg elements (jackets). Chrome places them much closer together.

These are the svg elements rendered in firefox: 
 
And here they are in chrome:
 
There's a rational explanation for this, but I'll have to come back to it later.