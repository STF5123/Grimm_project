## Grimm Brothers Analysis: Review

* Site publication: <https://stf5123.github.io/Grimm_project/>
* GitHub: <https://github.com/STF5123/Grimm_project/>
* Developers: Natalya Myers, Sheridan Fassett, Emily Levi
* Date of Evaluation: 2021-05-11
* Evaluated by: @ebeshero

### Project introduction and research questions
You introduce your visitors to the Grimm Brothers and something of their cultural significance. But you could say more on the main page about your project and its appraoch to the tales. What *kinds* of analysis did you apply and what were some of the more striking findings of your work? 


### Visualizations and analysis

Your SVG bar graphs of most-mentioned animals, colors, and numbers were drawn by hand, which almost certainly limited the scope of what you could easily display (only top 3, not top 10 or 20). But your readers would certainly want to learn more than what you've displayed here. Writing XQuery to output these SVG graphs would have helped you to make larger plots and show more data to look at and discuss.

**Discussion** of your visualizations is lacking, especially for the NLP graphs. Based on your work with and knowledge of Grimms' fairy tales, do you see any significance in the verb choices you chose to feature? Why do we only see results for verbs and not, say, for nouns or adjectives? The point of text analysis is to learn about your texts—so what did you learn from this view that you could not have understood from just reading them without a computer? 

We don’t just make graphs to make them, but to explore and interpret and raise questions. The significance of your findings is not clear: we’re missing thoughtful discussion, explanation, and speculation. 


### Website design and user experience
I admire the lovely presentation of the text on the Grimm project site. It's easy to read and navigate the tales and the display is elegantly framed with historic book illustrations. You should be citing the sources for those images, almost certainly a woodcut illustrator for the title page of the Complete First edition (who was that? give a credit line in a caption somewhere on the site). Where did that second image come from, and which story does it illustrate?

The works2.html page is very wide though, so you probably want to look for ways to control the proportional width of the three side by side divs. Let’s look at the structure: You have a body element wrapping around two sections and an `<article>` element. 
In your CSS, set the width of the body to be 100% and it will fill the available screen (instead of taking up more space). Then set rules for the sections and article:
```
section.indent 2 
```
(You shouldn’t use a space in a class like that, as it indicates two *different* class properties. Just call it `section.indent` insstead.

You should give the central section a class attribute so it’s different from other section elements on your site. Maybe designate it as `section.center `
Write CSS rules to set their widths:

```
section.indent{width: 20%)   /* This means, take up 10% of the available space *?
section.center {width: 60%} 
article {width: 20%}
```

Make sure all those values add up to 100% and you’ll have organized your layout to eliminate that over-wide side-to-side scrolling.

I notice you still have CSS set in a `<style>` element on an HTML page and MORE style rules in your separate linked CSS file. This makes editing the CSS inherently confusing: you really should combine all the styling into one central location (the associated CSS file). One thing you could set consistently across the website is whether you intend center aligment or left alignment of the text. NOTE: Designers generally agree that left alignment looks more professional and is easier to read  because the reader's eyes always return to the same place on the screen: it looks more cleanly blocked and defined. 

### Concluding remarks
The team gained experience in document analysis, SVG visualization, natural language processing, and web design. The write-up on your site could use much more development, but you designed an interesting project and created a resource worthy of continued development. 
