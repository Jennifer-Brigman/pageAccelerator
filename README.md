# pageAccelerator
A very light solution to load web pages faster.

## Browser Support
![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png)
--- | --- | --- | --- | --- |
5.0+ ✔ | 4.0+ ✔ | 10+ ✔ | 11.5 ✔ | 5.0+ ✔ |

# How does it work?
pageAccelerator is an agnostic library that uses ajax and pushState to deliver a faster navigation experience. It is a very light version of [turbolinks](https://github.com/turbolinks/turbolinks) and [pjax](https://github.com/defunkt/jquery-pjax) (our minfied file is just 2.2KB!). Basically it follows every link in your application and  for each click it loads the page in background and replaces the content correctly, keeping the real data from the body and head while updating the title.

## Installation
To install pageAccelerator, execute:

```shell
  npm install page-accelerator
```

or

```shell
  bower install page-accelerator
```

You may also simply use the minified file from the `dist/` directory.

## How to use?
pageAccelerator doesn't depend on jQuery, Zepto or any other library to work. You need just to include it at the end of your HTML code:

```html
  <script src="page-accelerator.min.js"></script>
```

Then you will be able to call upon the `pageAccelerator` functions, such as the example below:

```js
  pageAccelerator();
```

`pageAccelerator` can also receive a callback as a parameter that will be called whenever a new page has loaded.

Just call it and pageAccelerator was already following the web application links.

For links that you don't want to be followed, you need simply add `data-pageAccelerator="false"`.
