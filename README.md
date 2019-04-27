# Dynamic-Loading

This is a class exercise created by our coach [Lambelin Rafael](https://github.com/rafaello104)


I follow this exercises during my training as JuniorWeb Developer at BeCode in April 2019.
This is our initiation exercise in using AJAX.

## Objectives

- Learn about AJAX
- Make a simple load request with AJAX

## Instructions

- Create three different pages with content (a bit more than a screen-full) for a site
- Make an additional page with a navbar with links to the different pages, and a div in which you will place the content of each of the first three pages, depending on which link is clicked 
- Make the navbar sticky (fixed)
- Once done with the basic setup of the site:
    - Use AJAX to load thecontent from the different pages, depending on which link is clicked
    - Show a loading icon while you load a page in
    - When you click a different link on the navbar, first scroll up to the top of the window (animated) before loading the new content

## My solution

In the navigation bar every link has a attribute `data-source`. The value of data-source is the source of the page. I create an XMLHttpRequest object. When a link is clicked, a request is opened with `open` and pass the HTTP method name and value of data-source as parameters. Then the request is sent with `sent` method. An anonymous function will handle the response of the request. It will check the request's state, and if it is done, it will change the content of  the div in to the content of the request response.

When the a link is clicked, the function `scroll(top)` is called, wich will take us on top of the page and a loading icon is appended to the body, an it's removed when the request state is completed. To make the scroll smooth, in the css file, the html element has  the ` scroll-behavior` property set to `smooth`

You can see the results [here](https://alexandramadalina.github.io/Dynamic-Loading/). warning: the pages are not  responsive.

## Documentation

https://developer.mozilla.org/en-US/docs/Web/Guide/AJAX/Getting_Started
https://openclassrooms.com/en/courses/3523261-use-javascript-in-your-web-projects/3759261-make-your-first-ajax-request
https://codepen.io/blimpage/pen/obWdgp