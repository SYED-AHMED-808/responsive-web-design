## Part- 1

HTML, which stands for Hypertext Markup Language, is a markup language for creating web pages. When you visit a website and see content like paragraphs, headings, links, images, and videos; that's HTML.

Here is a small example using HTML elements. Try editing some of the text in the editor and see the changes update in the preview window.

```
<h1>Main heading element</h1>

<p>I am a paragraph element.</p>
```

HTML represents the content and structure of a webpage through the use of elements. Most elements will have an opening tag and a closing tag. Sometimes those tags are referred to as start and end tags. In between those two tags, you will have the content. This content can be text or other HTML elements.

Here is another example of a paragraph element. Change the text in the editor to say I love coding! and see the results in the preview window.

```
<p>I am a paragraph element.</p>
```

Both opening and closing tags start with a left angle bracket (`<`), and end with a right angle bracket (`>`), with the tag name placed between these angle brackets. While HTML tag names are case-insensitive, it is a widely accepted convention and best practice to write them in lowercase.

Here is a closer look at just the opening and closing paragraph tags:

> `<p>`  
> `</p>`  

What distinguishes an opening tag from a closing tag is the forward slash (/) placed immediately after the left angle bracket in a closing tag. Some HTML elements do not have a closing tag. These are known as void elements.

Here is an example of an image element which is a void element:  

> `<img>`  

Notice that this image element does not have the closing tag and it does not have any content. Void elements cannot have any content and only have a start tag.

Sometimes you will see void elements that use a / before the > like this:
   

> `<img />`   

While many code formatters like Prettier, will choose to include the / in void elements, the HTML spec states that the presence of the / "does not mark the start tag as self-closing but instead is unnecessary and has no effect of any kind".

In real world development, you will see both forms so it is important to be familiar with both.

If you wanted to display an image, you will need to include a couple of attributes inside your image element. An attribute is a special value used to adjust the behavior for an HTML element.

Here is an example of an image element with a `src` attribute. Update the value of the `src` attribute to ***"https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg"*** and you will see the image change to two cats peacefully sleeping.

> `<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg" />`  

The `src` attribute is used to specify the location for that image. For image elements, it's good practice to include another attribute called the `alt` attribute. The `alt` attribute is used to provide short, descriptive text for the images.

Here's an example of an image element with the `src` and `alt` attributes. Try breaking the image by updating the `src` value to ***"https://.freecodecamp.org/curriculum/cat-photo-app/cats.jpg"***. You will see the image disappear and only the `alt` text show.

> `<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch." />`  

So, you might be wondering if HTML by itself is enough to build a website. Well, the answer is: it depends. If you're building a small practice project that only displays text and images, HTML alone might be sufficient. However, if you're creating a modern professional website, you will need to have HTML, CSS, and JavaScript.

HTML is for the content and structure. CSS is for styling. JavaScript is for adding interactivity to your web pages. A good analogy for this is to compare HTML, CSS, and JavaScript with a complete building.

HTML represents the blocks, concrete, and irons that make up the walls. It's the foundation that makes the building strong. CSS represents the interior and exterior design that makes the house look beautiful. JavaScript represents the electrical and water system that ensures uninterrupted access to water and electricity.

## Part-2

An attribute is a value placed inside the opening tag of an HTML element. Attributes provide additional information about the element or specify how the element should behave. Here is the basic syntax for an attribute:

> `<element attribute="value"></element>`  
The attribute name is followed by an equal sign (`=`) and a value in quotes. The value can be a string or a number, depending on the attribute.

This first example uses the `href` and `target` attributes. The `href` attribute specifies the URL of a link and the `target` attribute specifies where to open the link.


> `<a href="https://www.freecodecamp.org/news/" target="_blank">Visit freeCodeCamp</a>`  

Without the `href` attribute, the link would not work because there would be no destination URL. So you must include this `href` attribute to make the link functional. The `target="_blank"` enables the link to open in a new browser tab. You will learn more about the `target` attribute in future lessons.

Other common attributes are the `src`, and `alt`, or alternative, attribute - which is used to specify the source of an image and provide alternative descriptive text for the image, respectively.


> `<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch." />`

Similar to the `href` attribute, the `src` attribute is required because it specifies the image file to be displayed. The `alt` attribute is not required, but it is recommended for accessibility purposes. Accessibility means making sure that everyone, including those with disabilities, can use and understand things like websites, apps, and physical spaces. You will learn more about accessibility in the upcoming lessons.

Some attributes are a little unique with their syntax like the `checked` attribute.

Enable the interactive editor and try clicking on the checkbox in the preview window to see it alternate between a checked and unchecked state.

> `<input type="checkbox" checked />`

In the following example, we have an `input` element with the `type` attribute set to `checkbox`. Inputs are used to collect data from users, and the `type` attribute specifies the type of input. In this case, this input is a checkbox. You will learn more about how inputs work in the upcoming lessons.

The `checked` attribute is used to specify that the checkbox should be checked by default. The `checked` attribute does not require a value. If it is present, the checkbox will be checked by default. If the attribute is not present, the checkbox will be unchecked. This is known as a boolean attribute. You will learn more about booleans in general when you get to the JavaScript section.

Enable the interactive editor and try remove the `checked` attribute from the `input`. You will see that the checkbox is no longer checked by default.

> `<input type="checkbox" checked />`

There are several common boolean attributes you will encounter in HTML, such as `disabled`, `readonly`, and `required`. These attributes are used to specify the state of an element, such as whether it is disabled, read-only, or required.

Here is an example of a text`input` element that is disabled by default. Enable the interactive editor and try clicking on the `input` element in the preview window. Now remove the `disabled` attribute from the`input` element and you will see that the `input` is no longer disabled by default. You should now be able to click on it and type inside the field.

> `<input type="text" disabled>`

HTML has many attributes that can be used to customize the behavior and appearance of elements on a webpage. Understanding how to use attributes is essential for creating interactive and accessible web content. Over the next few lessons, you will learn about more HTML attributes and how to use them effectively in your web development projects.

## Part-3

What Is the Role of the Link Element in HTML, and How Can It Be Used to Link to External Stylesheets?

Let's learn about the `link` element, and how to use it to link to external stylesheets.

The `link` element is used to link to external resources like stylesheets and site icons. Here is the basic syntax for using the `link` element for an external CSS file:

> `<link rel="stylesheet" href="./styles.css" />`

The `rel` attribute is used to specify the relationship between the linked resource and the HTML document. In this situation, we need to specify that this linked resource is a `stylesheet`.

It is considered best practice to separate your HTML and CSS in different files. Developers will use the `link` element for their external CSS file instead of writing everything in the HTML document.

The `href` attribute is used to specify the location of the URL for the external resource.

The `dot` followed by a forward slash in the example tells the computer to look in the current folder, or directory, for the `styles.css` file.

The `link` element should be placed inside the `head` element as seen in the following example:

> ```
> <head>
>  <meta charset="UTF-8" />
>  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
>  <title>Examples of the link element</title>
>  <link rel="stylesheet" href="./styles.css" />
> </head>
> ```
Often times you will see multiple `link` elements inside a professional codebase that link to different stylesheets, fonts, and icons. Here is an example of using the link element to `link` to an external Google Font called Playwright Cuba:

> ```
> <link rel="preconnect" href="https://fonts.googleapis.com" />
> <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
> <link
>  href="https://fonts.googleapis.com/css2?family=Playwrite+CU:wght@100..400&display=swap"
>  rel="stylesheet"
> />
> ```

Google Fonts are a set of free and open source custom fonts that you can use inside any project. You can choose which fonts you would like to use and Google will provide you with the necessary HTML and CSS code. In this example, the `preconnect` value for the `rel` attribute tells the browser to create an early connection to the value specified in the `href` attribute. This is done to speed up loading times for these external resources.

Another common use case for the `link` element is to link to icons. Here is an example of linking to a favicon:

> `<link rel="icon" href="favicon.ico" />`

A favicon, which is short for favorite icon, is a small icon typically displayed in the browser tab next to the site title. A lot of websites will use a favicon to display their brand icon.

## Part-4

What Is an HTML Boilerplate, and Why Is It Important?
Let's learn about the HTML boilerplate.

What is the HTML boilerplate, you ask? It's like a ready-made template for your webpages. Think of it as the foundation of a house. A boilerplate includes the basic structure and essential elements every HTML document needs. It saves you time and helps ensure your pages are set up properly. Here is an example:

> ```
> <!DOCTYPE html>
> <html lang="en">
>  <head>
>    <meta charset="utf-8" />
>    <meta
>       name="viewport"
>       content="width=device-width, initial-scale=1.0" />
>    <title>freeCodeCamp</title>
>    <link rel="stylesheet" href="./styles.css" />
>  </head>
>  <body>
>  </body>
> </html>
> ```
Let's break down the key parts of this boilerplate. First, there is the `DOCTYPE` declaration:

> `<!DOCTYPE html>`

It tells browsers which version of HTML you're using. Next, comes the html tag:

> ``` 
> <!DOCTYPE html>
> <html lang="en">
>   <!--All other elements go inside here-->
> </html>
> ```
This wraps around all your content, and can specify the language of your page. Inside the `html` tag, you'll find two main sections - a `head`, and a `body`:

> ```
> <!DOCTYPE html>
> <html lang="en">
>   <head>
>     <!--Important metadata goes here-->
>  </head>
>   <body>
>     <!--Headings, paragraphs, images, etc. go inside here-->
>   </body>
> </html>
> ```
The `head` section contains important behind-the-scenes information:

>```
> <head>
>   <meta charset="UTF-8" />
>   <meta name="viewport" content="width=device-width, initial-scale=1.0" />
>   <title>Document Title Goes Here</title>
>   <link rel="stylesheet" href="./styles.css" />
> </head>
> ```
Your site's metadata, contained in `meta` elements, has details about things like character encoding, and how websites like Twitter should preview your page's link. Your site's title, found in the `title` element, determines the text that appears in the browser tab or window. Finally, you'll typically link your page's external stylesheets in the `head` section using `link` elements.

The `body` section is where all your content goes:
> ```
> <body>
>  <h1>I am a main title</h1>
>   <p>Example paragraph text</p>
> </body>
> ```

Now, why is a boilerplate important? It ensures your pages are structured correctly and work well across different browsers. Using a boilerplate helps you avoid common mistakes and follow best practices. It's a great starting point for any web project. Remember, you can customize your own boilerplate to fit your needs. As you gain experience, you might add your own preferred elements or `meta` tags. As you continue to improve your personal boilerplate, you'll find that it saves you time when starting new projects.

## Part-5

What Is UTF-8 Character Encoding, and Why Is It Needed?
UTF-8, or UCS Transformation Format 8, is a standardized character encoding widely used on the web. Character encoding is the method computers use to store characters as data. Essentially, all text on a web page is a sequence of characters stored as one or more bytes. In computing, a byte is a unit of data consisting of 8 bits, or binary digits. UTF-8 supports every character in the Unicode character set - and this includes characters and symbols from all writing systems, languages, and technical symbols. Here is an example of using the `meta` element with the `charset` attribute to set the character encoding to `UTF-8`:

> `<meta charset="UTF-8" />`

By setting the character encoding to UTF-8, it will ensure that the accented `"e"` character (`é`) is displayed correctly on the page. Here is an extended code example of using the UTF-8 character encoding:

> ```
> <!DOCTYPE html>
> <html lang="en">
>   <head>
>     <meta charset="UTF-8" />
>     <meta name="viewport" content="width=device-width, initial-scale=1.0" />
>     <title>Examples of the UTF-8 encoding</title>
>   </head>
>   <body>
>     <p>Café</p>
>   </body>
> </html>
> ```
For each new project you create, you should include this `meta` element with the `charset` attribute set to `UTF-8`.

## Part-6

What are Div Elements and When Should You Use Them?

The `div` element is used as a container to group other elements.

Here is an example of a `div` element. Add another paragraph element inside of the `div` element and see the changes in the preview window. To see the previews, you will need to enable the interactive editor.
> ```
> <div>
>   <p>Example paragraph element.</p>
> </div>
> ```
You will mainly use the `div` element when you want to group HTML elements that will share a set of CSS styles. You will learn more about CSS in future lessons and workshops.

Even though the `div` element is commonly used in real world codebases, you should be careful not to overuse it. There are times when another element would be more appropriate.

For example, if you wanted to divide up your content into sections, then the `section` element would be more appropriate than a `div` element.

Add another `section` element below the first one. Then inside of the `section` element, a `h2` and `p` elements. You can use whatever text you like and you will see the changes in the preview window. To interact with the example, you will need to enable the interactive editor.

> ```
> <section>
>   <h2>Mammals</h2>
>   <p>
>     Mammals are warm-blooded animals with fur or hair. Most give birth to live
>     young.
>   </p>
>   <ul>
>     <li>Lion</li>
>     <li>Elephant</li>
>     <li>Dolphin</li>
>   </ul>
> </section>
> ```
The `section` element has semantic meaning over the `div` element which is not semantic. Semantics are the meaning of words or phrases in a language. In HTML, which is a language, elements have their own semantic meaning too. So, this means if you use a `section` element, the browser will pick up its semantic meaning and understand to treat this as a section - on desktops, mobiles, you name it.

## Part-7

What Are IDs and Classes, and When Should You Use Them?

The `id` attribute adds a unique identifier to an HTML element.

Here is an example of an `h1` element with an `id` of `title`.

Below the `h1` element, add an `h2` element with an `id` set to `"subtitle"`. You can write whatever text you like for the `h2` and you will see the changes in the preview window. To interact with the example, you will need to enable the interactive editor.


> `<h1 id="title">Movie Review Page</h1>`

You can reference the `id` name of `title` within your JavaScript or CSS. Here's a CSS example referencing the `id` of `title` to change the text `color` to `red`.

***NOTE:*** Some CSS has been provided for you in this interactive example. Don't worry about trying to understand the CSS code because you will learn more about that in future lessons. But if you want to see the text color change to blue, enable the interactive editor, click on the `styles.css` tab and change the `color: red;` to `color: blue;`.

> ```
> <!DOCTYPE html>
> <html lang="en">
>   <head>
>     <meta charset="utf-8" />
>     <meta
>        name="viewport"
>        content="width=device-width, initial-scale=1.0" />
>     <title>Review page Example</title>
>     <link rel="stylesheet" href="./styles.css" />
>   </head>
>   <body>
>     <h1 id="title">Movie Review Page</h1>
>   </body>
> </html>
> ```

> ```
> #title {
>   color: red;
> }
> ```
The hash symbol (`#`) in front of `title`, tells the computer you want to target an `id` with that value. `id` names should not be used more than once, and they should always be unique. Another thing to note about `id` values, is that they cannot have spaces in them. Here is an example of applying the words `main` and `heading` to an `id` attribute value:


> `<h1 id="main heading">Main heading</h1>`

Browsers will see this space as part of the `id` which will lead to unwanted issues when it comes to styling and scripting. `id` attribute values should only contain letters, digits, underscores, and dashes.

In contrast to the `id` attribute, the `class` attribute value does not need to be unique and can contain spaces.

Here is an example of applying a class called `box` to a `div` element.

> `<div class="box"></div>`

If you wanted to add multiple class names to an element, you can do so by separating the names by a space. Here is an updated example applying multiple classes to a `div` element.

> `<div class="box red-box"></div>`

Here is an another example of applying multiple classes to multiple `div` elements.

***NOTE:*** Some CSS has been provided for you in this interactive example. Don't worry about trying to understand the CSS code because you will learn more about that in future lessons. But if you wanted to change the color of the first and third boxes, enable the interactive editor and click on the `styles.css` tab and change the `background-color: red`; to `background-color: black;`.

> ```
> <!DOCTYPE html>
> <html lang="en">
>   <head>
>     <meta charset="utf-8" />
>     <meta
>        name="viewport"
>        content="width=device-width, initial-scale=1.0" />
>     <title>Colored boxes example</title>
>     <link rel="stylesheet" href="./styles.css" />
>   </head>
>   <body>
>     <div class="box red-box"></div>
>     <div class="box blue-box"></div>
>     <div class="box red-box"></div>
>     <div class="box blue-box"></div>
>   </body>
> </html>
> ```

> ```
> .box {
>   width: 100px;
>   height: 100px;
> }
> 
> .red-box {
>   background-color: red;
> }
> 
> .blue-box {
>   background-color: blue;
> }
> ```

## Part-8

What Are HTML Entities, and What Are Some Common Examples?

An HTML entity, or character reference, is a set of characters used to represent a reserved character in HTML.

Let's say you wanted to display the text `This is an <img/>` element on the screen. If you use the code currently in the editor, it won't display the desired result. Even if you added `src` and `alt` attributes to the example, it would show an image in the middle of the paragraph. Not the desired result. To interact with the example, you will need to enable the interactive editor.

> `<p>This is an <img /> element</p>`

When the HTML parser sees the less than (`<`) symbol followed by an HTML tag name, it interprets that as an HTML element. That is why you are not getting the desired result of `This is an <img/>` element on the screen.

To fix this issue, you can use HTML entities. Here is an updated example using the correct HTML entities for the less (`<`) than and greater than (`>`) symbols. Now you should see `This is an <img/> element` on the screen.

> `<p>This is an &lt;img /&gt; element</p>`

These types of character references are known as named character references. Named references start with an ampersand sign (`&`) and end with a semicolon (`;`). By using a named character reference, the HTML parser will not confuse this with an actual HTML element.

Another type of character reference would be the decimal numeric reference. This character reference starts with an ampersand sign and hash symbol (`#`), followed by one or more decimal digits, followed by a semicolon.

Here is an example of using the decimal numeric reference for the less than symbol.

> `&#60;`

The last type of character reference would be the hexadecimal numeric reference. This character reference starts with an ampersand sign, hash symbol, and the letter `x`. Then it is followed by one or more ASCII hex digits and ends with a semicolon.

> `&#x3C;`

## Part-9

What Is the Role of the Script Element in HTML, and How Can It Be Used to Link to External JavaScript Files?

The `script` element is used to embed executable code. Most developers will use this to execute JavaScript code. JavaScript is used to add interactivity to your web pages. Common examples of using JavaScript include interactive games, image sliders, and dynamic forms that validate user input in real-time.

Here is an example of using the `script` element in an HTML document. Remove the `//` from in front of the `alert("Welcome to freeCodeCamp");` and you should see an alert pop up. To see the previews, you will need to enable the interactive editor.
> ```
> <body>
>   <script>
>     // alert("Welcome to freeCodeCamp");
>   </script>
> </body>
> ```

While you can technically write all of your JavaScript code inside the `script` tags, it is considered best practice to link to an external JavaScript file instead. Here is an example of using the `script` element to link to an external JavaScript file:

> ```
> <script src="path-to-javascript-file.js"></script>
> ```

The `src` attribute is used here to specify the location for that external JavaScript file. `src` stands for "source". The reason why it is not encouraged to place all of your JavaScript inside the HTML document is because of separation of concerns. Separation of concerns is a design principle where you separate your programs into distinct sections and have each section address a separate concern. In this case, we want to separate our JavaScript code from our HTML code.

## Part-10

What Is the Role of the Meta Description, and How Does It Affect SEO?

SEO, or Search Engine Optimization, is a practice that optimizes web pages so they become more visible and rank higher on search engines. One way to improve your site's SEO, is to provide a short description for the web page using the `meta` element. Here is an example of using the meta element to set a page description for a gardening site:

> ```
> <meta
>   name="description"
>   content="Discover expert tips and techniques for gardening in small spaces, choosing the right plants, and maintaining a thriving garden."
> />
> ```

By setting the `name` attribute to `description`, it ensures that browsers, search engines, and other web tools correctly interpret this metadata. The `content` attribute is where you will place your description. It is recommended that you keep your descriptions short and concise. This is because search engines will often truncate the description based on the results page layout.

## Part-11

What Is the Role of Open Graph Tags, and How Do They Affect SEO?

The open graph protocol enables you to control how your website's content appears across various social media platforms, such as Facebook, LinkedIn, and many more. By setting these open graph properties, you can entice users to want to click and engage with your content. You can set these properties through a collection of `meta` elements inside your HTML `head` section.

The first important OG property to include would be the `title`. Here is an example of setting the OG `title` for the freeCodeCamp homepage:

> `<meta content="freeCodeCamp.org" property="og:title" />`
> 
For the `property` attribute, you will need to specify that it is `og:title`. The `content` attribute is where you will write the title you want displayed for social media sites.

The next important OG property would be the `type`. Here is an example of using the OG `type` for the freeCodeCamp homepage:

> `<meta property="og:type" content="website" />`

The `type` property is used to represent the type of content being shared on social media. Examples of this content include articles, websites, videos, or music.

The third important OG property would be the `image`. Here is an example of setting the OG `image` for the freeCodeCamp homepage:

> ```
> <meta
>   content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
>   property="og:image"
> />
> ```

In this example, the open graph image is pointing to the freeCodeCamp logo. All of these images should be high quality with good dimensions and ratios. Most social media platforms will include criteria for image requirements to help you ensure that your content displays well on their site. For example, the developers.facebook.com documentation page states:

"use images that are at least 1200 by 630 pixels for the best display on high resolution devices. At the minimum, you should use images that are 600 by 315 pixels to display link page posts with larger images."

The fourth important OG property would be the `url`. Here is an example of setting the OG `url` for the freeCodeCamp homepage:

> `<meta property="og:url" content="https://www.freecodecamp.org" />`


There are many more OG properties that you can set, like `description`, `audio`, `video` and `locale`. However, the open graph `url`, `image`, `type`, and `title` are the most important ones to include.

So how do these open graph properties affect Search Engine Optimization? When your content is shared on social media, well-crafted OG properties can enhance the appearance for your content in users' feeds. This can lead to higher click-through rates which could signal to search engines that your content is relevant and engaging.

## Part-12

What Are the Roles of the HTML Audio and Video Elements, and How Do They Work?

The `audio` and `video` elements allow you to add sound and video content to your HTML documents. The `audio` element supports popular audio formats like mp3, wav, and ogg. The `video` element supports mp4, ogg, and webm formats.

To include `audio` content on your web page, you can use the audio element with the `src` attribute pointing to the location of your audio file.

> ```
> <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/cruising-for-a-musing.mp3"></audio>
> ```

If you want to see the audio player on the page, then you can add the `audio` element with the `controls` attribute.

Press play in the preview window to hear one of Quincy Larson's songs. To hear a different song, change the `src` value to `"https://cdn.freecodecamp.org/curriculum/js-music-player/never-not-favored.mp3"`.

> ```
> <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/cruising-for-a-musing.mp3" controls></audio>
> ```

The `controls` attribute enables users to manage audio playback, including adjusting volume, and pausing, or resuming playback. The `controls` attribute is a boolean attribute that can be added to an element to enable built-in playback controls. If omitted, no controls will be shown.

Apart from the `src` and `controls` attributes, there are several other attributes that enhance the functionality of the `audio` element. The `loop` attribute is a boolean attribute that makes the audio replay continuously.

Here's an example of using the `loop` attribute to play one of Quincy Larson's songs titled "Can't stay down". To see the looping in action, enable the interactive editor, scrub the play head close the end of the song and it will restart again once it is finished.
> ```
> <audio
>   src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3"
>   loop
>   controls
> ></audio>
> ```

Another attribute you can use is the `muted` attribute. When present in the `audio` element, this boolean attribute will start the audio in a muted state. Here's an example of using the `muted` attribute.

To hear the music, enable the interactive editor and click on the volume icon in the audio player.

> ```
> <audio
>   src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3"
>   loop
>   controls
>   muted
> ></audio>
> ```

When it comes to audio file types, there are differences in which browsers support which type. To accommodate this, you can use `source` elements inside the `audio` element and the browser will select the first source that it understands. Here's an example of using multiple `source` elements for an `audio` element:

> ```
>  <audio controls>
>   <source src="audio.ogg" type="audio/ogg" />
>   <source src="audio.wav" type="audio/wav" />
>   <source src="audio.mp3" type="audio/mpeg" />
> </audio>
> ```

The browser will first start with the ogg type, and if it can't play the audio, then it'll move down to the next type in the list.

All the attributes we have learned so far are also supported in the `video` element. Here's an example of using a `video` element with the `loop`, `controls`, and `muted` attributes.

Add the `autoplay` attribute to the opening `video` tag so the video plays automatically. To interact with the example, you will need to enable the interactive editor.

NOTE: The `width` attribute is being used here to make the video smaller and fit better in the preview window. You will learn more about the `width` attribute in future lessons.

> ```
> <video
>   src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
>   loop
>   controls
>   muted
>   width="400"
> ></video>
> ```

For the `src`, or source attribute, we are using a video called "Big Buck Bunny" from archive.org. If you wanted to display an image while the video is downloading, you can use the `poster` attribute. This attribute is not available for `audio` elements and is unique to the `video` element. Here's an example of using the `poster` attribute with content provided by peach.blender.org.

> ```
> <video
>   src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
>   loop
>   controls
>   muted
>   poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
>   width="400"
> ></video>
> ```

You can also use the `source` element inside a `video` element, just like you did with the `audio` element. This lets you provide the same video in multiple formats, and the browser will choose the first one it can play.

> ```
> <video
>   controls
>   width="400"
>   poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
> >
>   <source
>     src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
>     type="video/mp4"
>   />
>   <source
>     src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.webm"
>     type="video/webm"
>   />
>   Your browser does not support the video tag.
> </video>
> ```