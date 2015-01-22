#### What this is

This is my take on Dave Winer's generalized <a href="http://scripting.com/2015/01/13/listicleOListicle.html">listicle</a>, which uses JSON for all configuration and holding the list of items. While I like JSON, because it's a simple file format to use, I know many people who might not grok it.

This version uses a published Google 

Forked from Dave Winer's [listicle project](https://github.com/scripting/listicle).

#### How it works

There's a <a href="https://docs.google.com/spreadsheets/d/1bv0YIPi9cDb3rLML6fKFrQnzVZnpiw8GlUF85WOWpBc/edit?usp=sharing">published Google spreadsheet</a> that configures the app. You can make a copy of the spreadsheet and modify it for your own listicle.

When the page loads, it uses tabletop.js to read the data from the Google spreadsheet, and shows you the first item in the list. If you click the right arrow, you go to the next item, click the left arrow you go to the previous one. The Home icon takes you to the first item. On a mobile device, you can swipe right or left to move between items.

If you click on the label you get a permalink for the item. If you click the twitter icon at the top of the page you get a dialog that sets up a tweet with the content of the item you're looking at. 

Click on the Info icon to see the About box.

#### Using the spreadsheet

* Make a copy of the <a href="https://docs.google.com/spreadsheets/d/1bv0YIPi9cDb3rLML6fKFrQnzVZnpiw8GlUF85WOWpBc/edit?usp=sharing">published Google spreadsheet</a>. (You need to be logged in to Google Drive to make a copy.
* Use the first sheet (Set Preferences) to change the listicle settings
* Use the second sheet (listicleItems) to add items - Don't delete or change the first row (item). Each cell below 'item' will become an item in the listicle. HTML a tags are okay to use.
* Go to File > Publish to web and publish the entire document. Copy the key for the published document: e.g., htt<span>ps</span>://docs.google.com/spreadsheets/d/**_1bv0YIPi9cDb3rLML6fKFrQnzVZnpiw8GlUF85WOWpBc_**/pubhtml
* Browse to where you setup the index.html file and add ?sheetKey=**_key_** to the end of the url.
  * If you want to test without installing on a server, you can try ht<span>tp</span>://mylisticle.appspot.com/?sheetKey=**_key_**
 
Because it's a Google spreadsheet, you can invite other collaborators to add items to the list!

#### Updates

v.0.01a - Initial work on integrating tabletop.js and Google Sheets

#### Demo

Here's the <a href="http://mylisticle.appspot.com/">demo listicle</a>.

Here's <a href="http://mylisticle.appspot.com/?sheetKey=1av8bBCCrYYnKQCuI3rXqdND3vspWQ3gvr6ggdEcfe78">another demo</a>, showing that you can just pass in the key of published Google Sheet 

#### Credits

Dave Winer is the creator of the listicle software used to power this.

Tabletop.js - [Jonathan Soma](http://twitter.com/dangerscarf) is the creator of tabletop, which is the javascript used to get the data from Google Sheets.
