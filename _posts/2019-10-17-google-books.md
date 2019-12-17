---
layout: post
title: Using the Google Books API
---

I created a webpage that would pull data from my personal “Library” on Google Books and display the book information on the screen through the Google Books API. In my project, I used a combination of HTML, CSS, JavaScript, and the Mustache template system to achieve this.

![_config.yml]({{ site.baseurl }}/images/google-books.png){: .center-image }

{% include media-link.html url=”http://brittneymiller.com/library.html" text=”SEE THE FINAL VERSION OF MY GOOGLE BOOKS LIBRARY.” target=”_blank” %}

The first thing I needed to do was create a basic container for my booklist data to live in. To do so, I created a basic HTML document with a header and description, and some basic inline styling. Another thing I did was generate my personal Google Books API key.

<p class="codepen" data-height="265" data-theme-id="default" data-default-tab="html,result" data-user="brittney092289" data-slug-hash="GRRqXKV" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Library HTML ">
  <span>See the Pen <a href="https://codepen.io/brittney092289/pen/GRRqXKV">
  Library HTML </a> by Brittney Miller (<a href="https://codepen.io/brittney092289">@brittney092289</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
<hr class="divider">

Next, I needed to add the JavaScript so I could pull the data from the Google Books API. The data was then able to be populated inside the div with the ID ‘booklist’.

First of all, I use jQuery because it takes common JavaScript tasks and turns them into methods that can then be easily called with simple lines of code. Similarly, I use Mustache as a template to provide the information to display in the HTML container by placing the data properties inside tags (the curly braces…get it? They look like tiny mustaches).

So, the first block of code is creating a template for displaying the books on the page by pulling the book ID, the book thumbnail and the book title from my Google Books library. I then added a class called “bookdetails” which generates from the next Mustache template I created. I have the book details div hidden until the user triggers the onClick function.

<script src="https://gist.github.com/brittney092289/317eed7de9687268d29381b724a8ee69.js"></script>
<hr class="divider">

The book details template generates the data and is applied to the “booklisttemplate” template. As a result, this template includes the all of the fine details of the individual book.

<script src="https://gist.github.com/brittney092289/17932edd8c6f51bdfad2357aa22b7f79.js"></script>
<hr class="divider">

Now on to the fun stuff, because this is where the previous templates come into play. I created functions that use my specific Google Books ID to show the books I have saved in my library by adding the templates into the original “booklist” div in the HTML. Also, I added a slide toggle function to show and hide the book details on click.

<script src="https://gist.github.com/brittney092289/a1dec62b497b73c235200e67c71a4689.js"></script>
<hr class="divider">

Finally, I added some CSS styling to style the booklist container.

<p class="codepen" data-height="265" data-theme-id="default" data-default-tab="html,result" data-user="brittney092289" data-slug-hash="PooGGoM" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Library HTML full">
  <span>See the Pen <a href="https://codepen.io/brittney092289/pen/PooGGoM">
  Library HTML full</a> by Brittney Miller (<a href="https://codepen.io/brittney092289">@brittney092289</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
<hr class="divider">

<p align="center">Now, that’s just like magic!⚡️</p>

{% include media-link.html url=”http://brittneymiller.com/library.html" text=”SEE THE FINAL VERSION OF MY GOOGLE BOOKS LIBRARY.” target=”_blank” %}

