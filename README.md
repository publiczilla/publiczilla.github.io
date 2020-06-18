# Carmazon

AMP-html template. Used by Pug, Sass, Gulp.

- [AMP documentation](https://amp.dev/)

## Recommendations

### Common

- The most important thing about AMP layout is to monitor the validity of the page. if the page does not meet the AMP standard, google will exclude it from the search results. To verify the validity of the page in different ways, there is even a extension in Chrome, [more detailed](https://amp.dev/documentation/guides-and-tutorials/learn/validation-workflow/validate_amp/). When developing, I like to just add `#development=1` to the address bar and then look in the browser console, [for example](https://alexkazakov.info/layout/carmazon/home-video-infographics.html#development=1).
- It is important to check the performance of AMP pages not only during development, but also after google has already started to output pages in search from its cache. It may be that after [Google AMP Cache](https://developers.google.com/amp/cache/?hl=ru) the pages will not work as planned, although they will be valid.

### CSS

- There are a number of restrictions in writing styles, all of them do not make sense to describe here, I will give a link to the [documentation](https://amp.dev/documentation/guides-and-tutorials/develop/style_and_layout/). Somewhere the validator will tell you, but here I will note an important feature - this is the limit on the size of CSS, namely: 75 KB. Therefore, we can't write as many styles as we want right now, because this could lead to a serious problem in the future. If possible, we make up independent blocks and use universal classes, which we set for different blocks.

### Connection

- It is quite easy to link AMP pages with regular pages, [more detailed](https://amp.dev/documentation/guides-and-tutorials/optimize-and-measure/discovery/?format=websites). On the finished AMP page, I have already specified a link to the normal one, and the other link is commented out there, so it remains to insert it on the normal page and specify the correct path to the AMP page. Google-bot will see a link to the AMP page on a normal page, check that it is valid, and add it to the search results. That's it, you don't need to do anything else.

### SЕО

- AMP is friendly with markup [Schema.org](https://amp.dev/documentation/guides-and-tutorials/optimize-and-measure/discovery#use-schema.org-for-most-search-engines), some possible bonuses are also promised in the output results, [more detailed](https://developers.google.com/search/docs/guides/about-amp).

## About building a project

- The build files are located in the build folder, and the finished production files are located in the dist folder.
- For HTML, Pug is used, and for CSS, SCSS is used. The project is built using Gulp.
- The project code has a commented section with reviews: [link](https://bit.ly/39ymSP5)

### Launch of the project

Enter in the terminal:

```
npm install
gulp watch
```
