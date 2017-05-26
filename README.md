# Ghostly

A theme for [Ghost](http://github.com/tryghost/ghost/) based on the default Ghost theme, [Casper](https://github.com/TryGhost/Casper).

[Demo here](https://ghostly.dexa-dev.com/)

## What does it provide

As it's based on Casper, the general look and feel is the same you would get with it, but we added some features that will enhance your experience using it:

* **Code syntax highlight**: when writing fenced code blocks (those surrounded by backticks (`` ``` ``) ), you can add the language after the opening quotes, and the HTML output will be highlighted according to the language.
  * If no language is specified, the engine will try to guess it
  * Provided by [Highlight.js](https://highlightjs.org/)
* **Disqus** as a comment system: if you use Disqus as a comment system, you will only need to define your Disqus shortname and it will be all set.
  * The comments will be lazy-loaded only when the user clicks the "Load comments" button, so no unnecessary requests are made
* **Revamped side menu**: the standard side menu felt old and incomplete. The new menu has a flat, simple style.
* **'Reading Time' header on posts:** added a simple 'reading time' header based on post length.
* **Default Home icon** in case you didn't add a Blog icon.
* **Social profiles**: On the lower part of the new side menu, you will be able to show links to your social profiles. Currently, the ones supported are:
  * Twitter
  * Facebook
  * Github
  * Linkedin
  * Telegram
* **Post description** The description of the post is taken from the meta description (If it is).
* **Link on repositories** On the footer link to the repository (GitHub, e.t.c.) "Fork this theme"

## Screenshots

<details>
<summary>Side menu</summary>

![Side Menu](assets/screenshots/side_menu_screen.png?raw=true "Side menu")

</details>
<details>
<summary>Reading time</summary>

![Reading time](assets/screenshots/read_time_screen.png?raw=true "Reading time")

</details>
<details>
<summary>Syntax Highlight</summary>

![Syntax Highlight](assets/screenshots/syntax_highlight_screen.png?raw=true "Syntax Highlight")

</details>
<details>
<summary>Comments</summary>

![Comments](assets/screenshots/comment_screen.png?raw=true "Comment")

</details>




## Why

We liked the Ghost default theme, but we thought it lacked some things, such as Syntax Highlighting or easy integration with a comment system.

## How

1. Download the latest version from [here](https://github.com/Arasthel/Ghostly/archive/master.zip).
1. Upload the theme folder to `{GHOST_FOLDER}/content/themes/`.
1. Restart the Ghost service.
1. Go to your Ghost admin panel, and under the **General** section, select the Theme.
1. Customize it as you like.

## Customization

For customizing the different options that this theme provides, you will need to go to your Ghost admin panel, open the **Code Injection** section, and on the **Blog Header** add this:

```html
<script type="text/javascript">
  // Your variables go here
</script>
```

Any further modification should be made by direct editing of the source code. Feel free to do it!

### Disqus

If you want to use the Disqus comment system, you will need to tell the theme which one is your Disqus shortname.

For doing so, between the script tags you put on the **Blog Header** section, you will need to add the following code:

```javascript
var disqus_shortname = 'YOUR_SHORTNAME';
```

### Social profiles

Those are the variables you will need to define in order to show your social profile links on the side menu:

```javascript
// Github
var github_user = 'YOUR_GITHUB_USERNAME';

// Linkedin
var linkedin_url = 'YOUR_LINKEDIN_USER_LINK';

// Telegram
var telegram_channel = 'YOUR_CHANNEL_NAME'
```

### Fork this page link

To have a link to the theme repository, use the variable `forked_url`.

```javascript
// Link on Github page
var forked_url = 'https://github.com/your_username/Ghostly'
```

> ### Twitter and Facebook
> Twitter and Facebook profiles will be taken from the blog defaults, defined under the *General* section

### Example

```html
<script type="text/javascript">
  var ga_ua = 'UA-123456-1';
  var disqus_shortname = 'MYSHORTNAME';
  var github_user = 'MYGITHUBUSER';
  var telegram_channel = 'mychannel'
</script>
```

### ToDo

- [x] Update highlight.js 9.6.0 to 9.11.0
- [x] Change description of the post from meta description by default
- [x] Update jquery 1.12.0 to 1.12.4
- [ ] Add a variable that specifies how to take a description of the post (or meta description or from the beginning of the post)
- [x] Add link "Fork This Theme" to footer on main page.
- [ ] Update Casper theme from base repositary.

## Copyright & License

Copyright (c) 2013-2017 Ghost Foundation - Released under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

