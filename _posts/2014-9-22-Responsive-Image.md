---
layout: post 
title: Responsive Image
---

## Why we need to use responsive images and why using them can be so difficult

It is important to have images that matched with specific screen size. 
Not only because larger image requires more time and memory to load. 
Faster loading of page is crucial to keep audiences on site. 
Using them can be difficult because we need to specify different images to users based on their screen size. 
The options for creating responsive image are CSS and JavaSript. 
One major problem to the approach of using CSS class for every image is that - we're forcing mobile users to download huge images. 


.site-banner {   width: 300px;   background-image: url('images/site-banner.jpg'); }

.site-banner {   width: 300px;   height: 100px;   background-image: url('images/site-banner-mobile.jpg'); }  @media (min-width: 480px) {   .site-banner {     width: 440px;     height: 200px;     background-image: url('images/site-banner-mobile-wide.jpg');   } }  @media (min-width: 768px) {   .site-banner {     width: 720px;     height: 250px;     background-image: url('images/site-banner-tablet.jpg');   } }  @media (min-width: 1024px) {   .site-banner {     width: 1000px;     height: 300px;     background-image: url('images/site-banner-desktop.jpg');   } }

The <picture> element acts as a wrapper around many different choices for images

<picture>   <source media="(min-width: 1024px)" srcset="images/site-banner-desktop.jpg, images/site-banner-desktop@2x.jpg 2x"></source>   <source media="(min-width: 768px)" srcset="images/site-banner-tablet.jpg, fimages/site-banner-tablet@2x.jpg 2x"></source>   <img srcset="images/site-banner-mobile.jpg, images/site-banner-mobile@2x.jpg 2x" alt="Good dog!"> </picture>

