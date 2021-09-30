# Infinity Scroll
JS Web Project Infinity Scroll

## About
The goal of this project is to implement the infinity scroll functionality seen on many social media applications as a user scrolls towards the bottom of the page, another network request is made, before the user reaches the bottom, so you don't see it and it feels as if you're seamlessly scrolling forever. The images we are using for our project are from the Unsplash API, and we track the moment all the images are loaded in order to dynamically hide our loading animation. 

This application displays one long column of images with a margin on the left and right. As a user continues scrolling towards the bottom of the page, we should expect to see the scroll bar on the side jump up as you reach the bottom of the page, signifying another network request has been made. When hovering over an image, we can see the description of the image provided by Unsplash. When an image is clicked on, you will be taken directly to the image on the Unsplash website. Here, you will see all information about the image, the author, and you are presented with the option to download the photo if desired. 

The infinity scroll application created will be mobile responsive as well, narrowing the margins to allow for a better mobile experience. 

## Built With

### Front End
 - HTML5
 - CSS3
 - JavaScript

### APIs
 - Unsplash API

## Functionality
The functionality for fetching data from the Unsplash API using JS, creating elements to display the photo data, and passing the data to those displayed elements is described in Figure 1. 
![Figure 1](/images/Unsplash_API_Flowchart.png) 

For implementing infinite scrolling, we can think of the window as the parent of the document and the grandparent of the body (where our event listener is attached), represents the entire browser window. We need 'window.innerHeight', which represents the total height of the browser window, and we need 'window.scrollY' which tracks the distance from top of page the user has scrolled. (All values are in pixels). We will add these two values together and compare it to the 'document.body.offsetHeight', which represents the height of everything in the body, including what is not within view (combined height of all images). However, we can't have just the documment.body.offsetHeight, we will need to modify it a little bit by subtracting a pixel amount (1000 pixels but can be any value), this way we can trigger an event to request to load more images before the bottom of page is reached. 
![Figure 2](/images/Infinite+Scroll+Functionality.png)

## Resources
 - https://loading.io: create custom animated SVG loader icon
 - https://unsplash.com/documentation: Unsplash image API

## Contributors
 - [**Alexander Sung**](https://github.com/alsung) - Creator