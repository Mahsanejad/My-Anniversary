<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HAPPY 2 ANNIVERSARY</title>
  <style>
    body {
      font-family: "Times New Roman", sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: c<svg xmlns="http://www.w3.org/2000/svg" xml:space="preserve" viewBox="0 0 192 192"><path fill="#e08524" d="M75.3 73.4H18.4l45.3 34.3L48.3 163l46.1-32.3 48.2 34.6-16.9-58.3 44.9-33.6H115l-20.5-55-19.2 55z"/><path d="m96.7 18.8 18.2 8.2 16.5 44.3h-15.1L96.7 18.8zm-47 146 18.7 9.9 42.6-29.9-16.5-11.4-44.8 31.4zm79.1-56.8 17.4 9.4 18.6 60.1-19.7-11.3-16.3-58.2z"/><path d="m173.1 74.3 17.8 9.2-44.7 34-17.4-9.4 44.3-33.8z"/></svg>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HAPPY 2 ANNIVERSARY</title>
  <style>
    body {
      font-family: "Times New Roman", sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background: url('czNmcy1wcml2YXRlL3Jhd3BpeGVsX2ltYWdlcy93ZWJzaXRlX2NvbnRlbnQvbHIvdjExMTctZnJhbWVzLTMyLmpwZw.webp') no-repeat center center fixed;
      /* background-size: cover; */

      background-size: 400% 400%;
      animation: gradientAnimation 15s ease infinite;
      color: bisque;
      text-align: center;

    }

    .container {
      background: rgba(0, 0, 0, 0.5); /* Optional: Add a dark overlay for better text readability */
      padding: 20px;
      border-radius: 10px;
      text-align: center;
    }
    .video {
      width: 80%;
      max-width: 325px;
      margin-bottom: 30px;
      margin-top: 20px;
      margin-left:220px ;

    }
    .text {
      font-size: 1.2em;




    }
  </style>
</head>
<body>
<div class="container">
  <div class="video">
    <video width="100%" controls>
      <source src="video-output-DC1EC769-9ADE-4C8E-AF40-9CD7307A668E.MP4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
  <div class="text">
    I can not believe it's been 2 years that we have been together.
    <br>
    Since the first time I saw you, I know that I will love you more and more till forever.
    <br>
    Thanks for being there for me all the time, I'll be there for you always and forever.
    <br><br>
    can't take my eyes off you, I always want to see you, touch you, feel you and love you over and over again.
  </div>
</div>
</body>
</html>

Copyright (c) HTML5 Boilerplate

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

{
  "name": " ",
  "version": "0.0.1",
  "description": "",
  "private": true,
  "keywords": [
    ""
  ],
  "license": "",
  "author": "",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "webpack serve --open --config webpack.config.dev.js",
    "build": "webpack --config webpack.config.prod.js"
  },
  "devDependencies": {
    "copy-webpack-plugin": "^11.0.0",
    "html-webpack-plugin": "^5.6.0",
    "webpack": "^5.91.0",
    "webpack-cli": "^5.1.4",
    "webpack-dev-server": "^5.0.4",
    "webpack-merge": "^5.10.0"
  }
}

# www.robotstxt.org/

# Allow crawling of all content
User-agent: *
Disallow:

{
  "short_name": "",
  "name": "",
  "icons": [{
    "src": "icon.png",
    "type": "image/png",
    "sizes": "192x192"
  }],
  "start_url": "/?utm_source=homescreen",
  "background_color": "#fafafa",
  "theme_color": "#fafafa"
}

const path = require('path');

module.exports = {
  entry: {
    app: './js/app.js',
  },
  output: {
    path: path.resolve(__dirname, 'dist'),
    clean: true,
    filename: './js/app.js',
  },
};

const { merge } = require('webpack-merge');
const common = require('./webpack.common.js');

module.exports = merge(common, {
  mode: 'development',
  devtool: 'inline-source-map',
  devServer: {
    liveReload: true,
    hot: true,
    open: true,
    static: ['./'],
  },
});

const { merge } = require('webpack-merge');
const common = require('./webpack.common.js');
const HtmlWebpackPlugin = require('html-webpack-plugin');
const CopyPlugin = require('copy-webpack-plugin');

module.exports = merge(common, {
  mode: 'production',
  plugins: [
    new HtmlWebpackPlugin({
      template: './index.html',
    }),
    new CopyPlugin({
      patterns: [
        { from: 'img', to: 'img' },
        { from: 'css', to: 'css' },
        { from: 'js/vendor', to: 'js/vendor' },
        { from: 'icon.svg', to: 'icon.svg' },
        { from: 'favicon.ico', to: 'favicon.ico' },
        { from: 'robots.txt', to: 'robots.txt' },
        { from: 'icon.png', to: 'icon.png' },
        { from: '404.html', to: '404.html' },
        { from: 'site.webmanifest', to: 'site.webmanifest' },
      ],
    }),
  ],
});
enter;
      height: 100vh;
      margin: 0;
      background: url('czNmcy1wcml2YXRlL3Jhd3BpeGVsX2ltYWdlcy93ZWJzaXRlX2NvbnRlbnQvbHIvdjExMTctZnJhbWVzLTMyLmpwZw.webp') no-repeat center center fixed;
      /* background-size: cover; */

      background-size: 400% 400%;
      animation: gradientAnimation 15s ease infinite;
      color: bisque;
      text-align: center;

    }

    .container {
      background: rgba(0, 0, 0, 0.5); /* Optional: Add a dark overlay for better text readability */
      padding: 20px;
      border-radius: 10px;
      text-align: center;
    }
    .video {
      width: 80%;
      max-width: 325px;
      margin-bottom: 30px;
      margin-top: 20px;
      margin-left:220px ;

    }
    .text {
      font-size: 1.2em;




    }
  </style>
</head>
<body>
<div class="container">
  <div class="video">
    <video width="100%" controls>
      <source src="video-output-DC1EC769-9ADE-4C8E-AF40-9CD7307A668E.MP4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
  <div class="text">
    I can not believe it's been 2 years that we have been together.
    <br>
    Since the first time I saw you, I know that I will love you more and more till forever.
    <br>
    Thanks for being there for me all the time, I'll be there for you always and forever.
    <br><br>
    can't take my eyes off you, I always want to see you, touch you, feel you and love you over and over again.
  </div>
</div>
</body>
</html>
