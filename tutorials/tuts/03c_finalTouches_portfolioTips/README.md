
# Portfolio!!!
## More CSS/HTML & portfolio tips

 ◇─◇──◇────◇────◇────◇────◇────◇─◇─◇
<br />

*Recommended tutorials:*

* [W3 Schools](https://www.w3schools.com/) and [Mozilla Developers Network](https://developer.mozilla.org/en-US/docs/Learn/HTML) are great references with non-video tutorials
* [Kadenze Tutorial: Web Coding Fundamentals](https://www.kadenze.com/courses/web-coding-fundamentals-for-artists/info): This course is designed specifically for artists. If you create a Kadenze account, you can audit the course for free, only caveat is that you have to time it with the start of the course... Watch Session 1: Intro to the Web Landscape for familiarity with HTML/CSS


#### On this page:

1. [Adding favicons](#-favicons)
2. [Custom Domains](#-custom-domains)
3. [HTTPS Setting up secure SSL](#-https-setting-up-secure-ssl)
4. [Using frameworks and templates for your CSS styling](#-using-frameworks-and-templates-for-your-css-styling)



---
<br>



# ▼△▼△▼ Favicons


Favicons are the little symbol in the browser tab of your webpage. To make a custom favicon for your site:

1. Create a SQUARE image in photoshop/illustrator, I make them 500 x 500px so there's plenty of room to downsize. Export them as PNGs if you want transparency (recommended). Keep the image super simple because they will be so small!

2. Upload image to an online [favicon generator](https://realfavicongenerator.net/)

3. The favicon generator will create a bundle of favicon image files in different sizes/formats so your favicon will show in different browsers/devices. Download the zip and place files in the root directory of your website. The root directory is the main folder, where your homepage index.html lives.

4. The generator will also give you HTML — this goes in the <head> of your HTML (not the body).

That's it!


<br>
<br>

# ▼△▼△▼ Custom domains


You can purchase a custom domain from a domain name registrar. GoDaddy and NameCheap are two popular sites.

Once you have purchased your custom domain, connect the domain to your GitHub page. This way, whenever someone goes to www.yourName.com, your GitHub page will load.

* [General tutorial from GitHub help](https://help.github.com/articles/quick-start-setting-up-a-custom-domain/)
* [Tutorial specific to GoDaddy domains](https://medium.com/@LovettLovett/github-pages-godaddy-f0318c2f25a)
* [Tutorial specific to NameCheap domains](http://davidensinger.com/2013/03/setting-the-dns-for-github-pages-on-namecheap/)


<br>
<br>

# ▼△▼△▼ HTTPS Setting up secure SSL

Good news! As of May 1st 2018, GitHub added HTTPS support for custom domains using GitHub pages! [Here's a tutorial](https://blog.github.com/2018-05-01-github-pages-custom-domains-https/) to set it up.

<br>
<br>

# ▼△▼△▼ Using frameworks and templates for your CSS styling

You would have to learn a lot about modern CSS to get your website looking clean and mobile-responsive (so that it resizes for readability on mobile phone).

If you want to go this route, be sure to use media queries and (I would recommend) flexbox.

Adapting templates or using a library/framework like Twitter Bootstrap are great options.

### Adapting CSS templates

Templates are great! There are many resources online ---> [templated.co](https://templated.co/) has a LOT of free templates to use.

You can find a lot of sample code on [W3 schools](https://www.w3schools.com/css/default.asp).

*Warning*: Sometimes customizing templates can get sloppy if you have conflicting CSS rules.

Many of these templates use [Sass](https://sass-lang.com/) as a preprocessor, so you might want to familiarize yourself with Sass if you go deep into customizing a template.

### Twitter Bootstrap

Twitter Bootstrap is a framework that makes it EASY to create responsive websites that are designed for mobile-first.

In its simplest form, it is basically a CSS library that you can link to just like your custom css style sheet. To use bootstrap, add this line to your HTML head:

      <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">


Because of the was CSS cascades, you will want to link to bootstrap BEFORE you link to your  style sheet in the code, so be sure to have the bootstrap link on a line above the link to your css file.

Then grids are easy! You can just plug in Bootstrap class names to build out your site structure. Here is code for a 2 row grid. The top row has 3 columns and the bottom row has five.

    <div class="container">
        <div class="row">
          <div class="col"></div>
          <div class="col"></div>
          <div class="col"></div>
        </div>
        <div class="row">
          <div class="col"></div>
          <div class="col"></div>
          <div class="col"></div>
          <div class="col"></div>
          <div class="col"></div>
        </div>
    </div>

To make them responsive, you can get way more detailed. To learn more, check out the [Bootstrap documentation guides](https://getbootstrap.com/docs/4.1/layout/grid/) or check out the tutorials below.

Tutorials:
* [Lynda Bootstrap 4 Essential Training](https://www.lynda.com/Bootstrap-tutorials/Bootstrap-4-Essential-Training/372545-2.html). You can learn a lot in just the first 2 chapters (~1hr of tutorials)
* Or go through the [W3 schools tutorials](https://www.w3schools.com/bootstrap4/default.asp)

<br>
<br>
