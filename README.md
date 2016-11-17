## Summary

This visualization explores the common traits of survivors of the RMC Titanic sinking happened in 1912

Survivors were mostly female, young (according to the code of conduct "Women and children first") but also rich people

We want to convey this message by telling a story about the Titanic and the "Women and children first" code of conduct 
 
## Design

I started thinking at which kind of informations to display and building a story around them

4 graphs indicate:

- the number of survivors/non survivors (this graph was added after a feedback)
- the percentage of survivors/non survivors by gender
- the percentage of survivors/non survivors by age
- the percentage of survivors/non survivors by cabin class

It is possible to make a single graph with multiple informations, reducing the number of graphs to be made, but I decided to convey one information at a time to help reader to follow the story

The biggest challenge was the low experience with Javascript, but it has been quite funny learning and writing some code

About Dimple, I found it very useful and quick but sometimes a little hard to customize

I used bar charts because I found they better illustrate data; I also tried using different and mixed chart types, but it distracts and comprehension is not immediate

I used just two color, a green one - usually associated with safety - for survivors and a gray for non survivors

I tried to keep coherence for the whole story using the same kind of graph, same colors and layout

## Feedback

### First feedback

The initial visualization can be seen [here](http://rawgit.com/vverde/Udacity-Data-Analyst-Nanodegree-P6/master/titanic.html)

In the first version there was no interaction and the focus was kept on the graphs

The first feedback came from Udacity Forum and comments were about:

##### Color usage
In first version I used a light gray (well, much lighter) to focus more on the survivors. But, because in any case I was showing an information (the number of non survivors) it was more appropriate to use a darker color
In a first moment, color was changed using d3 and changing color attribute of rects. Later (and after a feedback) I used a different way to keep coherence between bar color and tooltip color

##### Legends
There was no legend in the initial visualization because I thought the graph was quite clear and self-explanatory; but we cannot force the readers to understand how we decided to use colors
So I added legend to all graphs except the first (just because the bars' labels already describe the data)

##### Layout
Graphs had no title and context information
I reviewed the layout and I added titles and better information on the axis

##### Tooltips
Dimple's standard tooltips display a limited number of information and bounded to the values in data. I made them more explanatory and added some extra information

### Second feedback

The second feedback came from a colleague and was related to the tooltip colors that didn't match the graph colors

##### Tooltips colors

This was quite a little pain to fix, because when I used d3 to change the colors of the rects in plot, Dimple still used the standard color to display the tooltips

After looking the documentation we find that dimple.color can resolve the problem and we don't need to change the rect color via d3

### Third feedback

The third feedback came from my wife and was about the story

In particular I didn't introduce the Titanic story and draw any conclusion, and she spent few time to figure out what I was talking about

Intro text and conclusion were rewritten based on these considerations and a new graph added (the first one) to better explain the Titanic story

Final visualization can be seen [here](http://rawgit.com/vverde/Udacity-Data-Analyst-Nanodegree-P6/master/titanic%20v2.html)

## Resources
- [Dimple homepage](http://dimplejs.org/)
- [Dimple Wiki](https://github.com/PMSI-AlignAlytics/dimple/wiki)
- [Stackoverflow](http://stackoverflow.com/)
	- [Tooltip custom text](http://stackoverflow.com/questions/38204790/dimple-tooltip-add-custom-text)
	- [Number rounding](http://stackoverflow.com/questions/15762768/javascript-math-round-to-two-decimal-places)
	- and more on javascript
- [Udacity forum](https://discussions.udacity.com/c/nd002-p6-data-visualization-with-d3-js)
- [Mike Bostock’s Blocks](http://bl.ocks.org/mbostock)
- [Google fonts](https://developers.google.com/fonts/docs/getting_started)


## Data
I used data from Udacity Project 2 about Titanic Survivors

The data was cleaned, removing unused fields and renaming some value to display more explanatory labels