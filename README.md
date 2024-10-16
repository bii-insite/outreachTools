# Modifying 'Spin The Wheel'

## Basic Structure
spinTheWheel.md is a markdown file - it accepts HTML as well as shortcuts that make HTML coding easier. There can be three overarching sections in html/md generally, and those three sections show up in this file particularly: 

1. the css section, where you can add in styling information, marked by the &lt;style&gt; &lt;/style&gt; tags,
2. the HTML section, where the elements of the page are actually specified (in spinTheWheel, this section is all contained within &lt;div&gt; &lt;/div&gt; tags), and
3. the JavaScript (JS) section, where you can program the page to interact dynamically with users, marked by &lt;script&gt; &lt;/script&gt; tags.

## the JS section

The JS section specifies a function to be executed whenever the "Send" button is pressed. The function modifies the css of the wheel in order for it to start spinning for 2 seconds and generates a variable called rando, which is assigned the value Math.random(). This is a random value between 0 and 1. After two seconds, the function replaces the wheel image with a different image and changes a blank textbox beneath it to display some text, depending on the value of rando. After five seconds, the image reverts to the wheel, and the form information is set to blank.

### Modifying probabilities

Part of the JS code is a set of if statements. The if statements instruct the page on what to do if rando falls within certain values. These should span the entire range of possible values for Math.random() (that is, they should span 0 to 1), and they shoud not overlap each other. As of October 2024, these values are set to divide the range evenly among seven outcomes (0 to 0.1428, 0.1428 to 0.2856, etc). But you can modify them to favor certain outcomes. For example, if you want the notepad to have 50% probability of occurring, you can change that if statement to be (rando > 0 && rando <= 0.5), and then modify the other if statements as necessary. If you wanted the other six possibilities to be equally probable, then they would have if statements like (rando > 0.5 && rando <= 0.583333), (rando > 0.58333 && rando <= 0.67777), etc.

### Modifying images

In order to change the options in the wheel, you can add and remove if statements. You can also substitute in new information for existing if statements. If you wanted to substitute a t-shirt for the waterbottle, it's easy to change the innerHTML currently set to "A water bottle!" to say "a t-shirt!" instead. It's also easy to change the image associated with it, but this involves one extra step. First, you need to upload a new image to the [images](https://github.com/bii-insite/outreachTools/tree/main/images) folder of the outreachTools repository. Then you update image.src to equal a relative path that names the file, following the example of the other if statements.

## Reverting to an earlier version
GitHub is a versioning software - that means it keeps track of earlier versions of all your files. If you made a change and you don't like it, and if you forget what the script had looked like previously, it's easy to revert to an earlier version. One way to do this is to click on the ```blame``` tab, and you'll see a list of updates made to the file. You could, if you like, click on one of these earlier versions and copy-paste it into your current file in order to revert your code to that earlier version.


## Resources for debugging, learning more
1. chatGPT
2. W3 schools
3. console.log() / chrome developer tools
