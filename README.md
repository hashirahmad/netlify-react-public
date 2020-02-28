# netlify-react-public
It simply contains the commit history of the private `netlify-react`<br> 
***This is a side project.*** <br>
***It is not production ready code***<br>

## Why?
To show the progress of private side project. <br> It help showcase what I am doing in my private time but without having to reveal the source code. <br>
I do not wish at the present moment to reveal the source code for personal reasons.

**🙏Github🙏**: Please add the ability to show `private repo` but not actual source code so that viewers can still see the progress of a developer regradless of whether they are working on `private` or `public repo`. Obviously letting developers choose because they equally may not want to.

# Commit history
## LATEST FIRST

 1. First task
 2. Second task
 3. Third task
 4. etc . . .

## 28-02-2020
1. Added linear `Bar` component. Previously `Linear` component was actually designed too heavily for the animation of the bottom progress bar. Basically it ended up being bespoke component.
2. Added `TextBar` component - basically when want to show progress of something with text on left and progress `Bar` on the right and additional tooltip for actual values. 
3. Added `Dashboard` screen leveraging the use of newly added components.
4. Fixed a bug in `Bar` component in regards to where setting 100 value would not work. Animations are now much faster and little more realistic.
5. Finalised the content of `Dashboard` screen.

## 27-02-2020
1. Added `animateForSecs` option to `Linear` progress bar for fake animations or when the to show "subtle" progress but the sort of progress which is not predictable or `callback` is not available or possible. 
2. Small bug fixed in `SimpleCard` component where having `paddingTop: 0` would result into sligh visual annoyance and `paddingTop: 1` fixes it.
3. Finally managed to virtualise `SimpleCardList` using `react-tiny-virtual-list` the way how I wanted to so that it appends the new content underneath the current content and not doing too much rendering without any duplication of initial set of data. The rerendering still happens but in managable way and is only noticable due to image being reloaded again. Overall it is a good effort.
4. A bug fixed which would initiate progress bar to open unintentionally.
5. `CustomTypography` now support aligning of text - before it would simply just stick to the left side.
6. Fixed a bug in `Linear` progress bar where `on` and `off` would utilize a `class` which would turn off other progress bars too.

## 26-02-2020

1. Tried to virtualize the `SimpleCardList` so that no matter how big the list
may be - performance is not impacted in any negative way.
2. Tried `react-virtualized`, `react-infinite-scroll-component` and `react-tiny-virtual-list`.
3. The main problem with them is that they constantly rerender and with `list` being very heavy
in terms of image urls, performance is hit quite hard. Most of these are generally aimed at
creating only long list of tabular or any other data but not anything which fetches images
for each child.
4. `react-infinite-scroll-component` is almost perfect except that it duplicates first set twice
and then loads the rest of data smoothly morealess.
5. Ideally `react-virtualized` is most complete package but would require significant customisation
to fit exactly my needs.
6. After a day of trying different solutions and ideas offered on stack overflow - what I want to do is apppend
the new content towards the bottom of the screen and I can think of ways but they require certain level of hacking
the packages in ways not intended or very much developing complete bespoke solution.

## 25-02-2020
1. Added image support for `SimpleCard`.
2. Padding at the top is now set to 0, previously it was `16px` which was far too unecessary.
3. `imageTitle` of `SimpleCard` by deafult will be whatever is `boldStatement`
4. Added support for picture heavy card by adjusting `padding` and `margin` at the bottom.
5. `Utils`'s `getCardActions` support `title` parameter which is useful for both `InAppBrowser` and `LongContentDialog`. 
6. Does not break it because if `title` is not provided, it falls back to `text` which is required anyway.
7. `getCardActions` of `Utils` now offically supports `title` as oppose to relying on the `text` property. 
8. `title` is directly injected into `getCardActions` which is whatever the `Card`'s title is.
9. This does mean that if a particular card has more than one `InAppBrowser` instances on a click - all of them will have the same `title` which is fine because it is all part of that `Card`'s title.
10. Added content to `MyNotebookOfLife` screen.
11. Added relevant `CMS` for easy updating of content.
12. Made changes to `SimpleCard` that would run specifed function of `Utils` for the image URL - this is at the moment only needed for.
13. Medium's content where I can easily enter uncomperessed image URL in `CMS` and the desired function of `utils` will return a URL whose image is compressed.
14. Added `mediumSmallUrl` to `Utils` which is the function that does literally adds some parameters for width and height to return a smaller image.
15. Added `SnackbarOne` component. It can be accessed from internal `API` as usual. 
16. It is a "one-off" component - this means it needs to be just defined in the main `app` once and can than be used pretty much across the entire app with easy to use internal `API`.
17. Added `copyTextToClipboard` to `Utils` for easu coping of links.
18. Added support for copying to `getCardActions` of `Utils`.
19. Updated `MyNotebookOfLife`'s `CMS` to benefit from `copyTextToClipboard` functionality by letting users share the article URL easily wherever they want to use it.
20. Added generic icon for articles for `MyNotebookOfLife` screen. Originally wanted customised icons for each article but there are not enough icons at the moment to describe icons so just using default icon.
 
## 24-02-2020
1. `Linear` progress `API` now integrated with internal `API` for full control of turning it on and off easily from entire app.
2. `Linear` progress bar by default now invisible as before running openly.
3. Made internal changes to `Linear` progress bar - mainly when turning `on` or `off` and checking if the `DOM` actually exists. This problem happens around when page loading and `API` is turning it `on`.
4. Added `GitHubReadMe` component for showing `readme` of Github for side projects.
5. Added support for `GitHubReadMe` for `getCardActions` so that `card`'s read me button opens `LongContentDialog` opening up `Read Me` of the github.
6. Fixed a bug of setting `display: 'none'` to `Linear` component.
7. Added a `Side Projects` screen.
8. Added relevant `CMS` for it.
9. Updated `Routes` accordingly.
10. Fixed a bug for `Linear` progress bar component where it would hide very after `rendering` because there is no immediate need for it to be shown. This is a design flaw or not the right way. At this point I have not yet found a "right" approach hencing fall for what works as last resort.
11. Made minor fixes to `CMS` namely `ProjectsCMS` and `SideProjectsCMS`.
12. `LongContentDialog` now supports `icon` just like other dialogs. 
13. Removed `horizontal scroll bar`.
14. Decreased overall height of the `LongContentDialog` so that it does not takes 100% of the height or close to it. 
15. `Utils`'s `getCardActions` updated with the icon support so it can benefit from the new feature.

## 23-02-2020
1. Changed some structure of the `InAppBrowser` so it does not need to be wrapped around for everything. It is just now used very much like `LongContentDialog`.
2. Added a `RunOnEveryUrlChange` component. This is useful for change root level components from children and many more purposes. 
3. Changed `PageTitle` to benefit from `RunOnEveryUrlChange`.
4. Added a `CookieConscent` component that will ask for cookie conscent one-time. 
5. I know many websites which will ask for permission every single session.
6. This `CookieConscent` component will be one-off and until user resets browser or manually delete cookies - the conscent will never ask again.

## 22-02-2020
1. Added google analytics to site.
2. Changed Work Diary's pdf `Drive`'s link so it is embded.
3. Created internal `API` for internal use.
4. The main idea is to expose `React Hooks API` of components centrally to other components that may not be linked in any other way.
5. With the use of internal `API` - Indvidual components' `API` is no longer relient on `window` object.
6. This also means that it is no longer exposed using `Developer Tools` at least not easily. Furthermore the concept of validating for the `key` when using `window["function"]` is no longer required or neccessary.
7. `InAppBrowser` updated to use internal `API` and require no longer any reliance on `global` `window` object.
8. Also removed `bloated` code.
9. `Utils` also updated to benefit from internal `API` rather than relying on `window` object.
10. Added a `LongContentDialog` component which of course support easy programmatic use via internal `API` throughtout the entire app. 
11. No need of having to place `LongContentDialog` indvidually on each screen - it is placed centrally and can envoked easily using the internal `API`.
12. Added a custom ` React Hook` - still do not fully understand it yet. It is called `UseFunctionAsState`.
13. This allows setting functions for dynamic clicking of button. Usually `React.useState( () => { ... }` would work and it does work but not in the way I expect. This way function will run immediatley as the function is set however `React.useState( () => { ... }` returns the value of function not returning the actual function itself.
14. Custom hooks are meant for this sort of thing. I use it and it work but not quite fully understand the depth of technicality.
15. Added a `FullScreenDialog` that is responsive which also uses  `UseFunctionAsState` to fully work as planned. As `LongContentDialog` it can easily be envoked using internal `API`.

## 21-02-2020
1. Added `InAppBrowser` component.
2. The main motivation for it's creation is to serve external links or media inside the app. 
3. This is useful so that vistors stay inside the app even if viewing external content - basic idea is so keep them inside the app plus gives a little more control.
4. `Wrapping` the entire app inside the `InAppBrowser` to benefit from its functionality inside the entire app using its `API` or rather one function more easily rather than having to place `InAppBrowser` on individual screens manually.
5. The merits of this approach is debatable, whether a good idea or terrible idea.
6. Added `Keys` component - this is very much a `JSON` file containing reference keys used for `LocalStorage`. NOT TO BE CONFUSED WITH SECURITY/API keys
7. `Themes` now internally uses `Keys` component. Allows very much central one place control. 
8. `InAppBrowser`'s `API` is technically public in terms of calling `window["functionName"]( ...data )`. While all it can do is close or open a link - that is all it can do. Despite this, `API` now requires a certain `key` to be passed in to `window["functionName"]( ...data )` function so that using `Developer Tools` it cannot be envoked as whoever envokes it will have to require the internal key just for using the function.
9. While this measure is not perfect, it still prevents the envoking of `InAppBrowser`'s `API` from `Developer Tools`.
10. Made changes to `getCardActions` of `Utils` to benefit from `InAppBrowser`'s `API` so that it opens external links in the `InAppBrowser` component.
11. `allowExternally` property supported to allow it externally of course! - This is useful particularly when URL does not allow/support `iframes`.
12. Made changes to `ProjectsCMS` to benefit from `allowExternally` property where GitHub's link would be opened in a new tab as oppose to `InAppBrowser`.
13. `CorporateExperiencesCMS` updated with `link` icons to be replaced with `open_in_browser` icons as it excactly the icon for `InAppBrowser`.

## 20-02-2020
1. Changes made to `standardizeText` function of `Utils` to add a space character at the end of each line so that `CMS` `array` of `text` does not have to conatain an extra ` ` space at the end of each line in an `array`.
2. `SimpleCard`'s `text` now `aligned` to left as oppose to center.
3. Added icon support for `SimpleCard` using `mainIcon`.
4. `CMS` changed for various screens to benefit from icon support available in `SimpleCard`. Following screeens have benefited from ^ above ^ feature: 
<br>`MyStoryCMS`, <br>`ChangeTheme`, <br>`MoreCMS`, <br>`ProjectsCMS`
5. `getCardActions` of `Utils` now supports `open in new tab` feature where any external link is opened in a new tab.
6. Subtle changes to `ProjectsCMS`
7. Updated `Routes` inline with the new content added to `ProjectCMS`
8. Added `CorporateExperiences` screen, bare skeleton
9. Added releveant `CorporateExperiencesCMS` for use later on today
10. Refined or rather added some comments to main `App.js` and renamed some variable names for cleaner code.
11. Added `ComplexCardList` component to be used in `CorporateExperiences` screen or rather useful in that respect.
12. `ComplexCard`'s `action` buttons now wrap around in a fluid way and pleasant to eyes. This is useful when there are more than 2 buttons when it would previously try to compact everything and hold it in one row.
13. Added `min-width` equal to `max-width` to `ComplexCard` so it looks evened out in terms of `width`.
14. `CorporateExperiences` screen updated with real content.
15. `CMS` content added.
16. Added pictures related to content too.
17. Updated some `CorporateExperiencesCMS` content.
18. Added projects screen to `Work Experience` screen.

## 19-02-2020
1. `SimpleCard`'s `text` typography component changed from `p` to `div` which allows `text` to be more roubust component as `p` is more limiting.
2. Backspace speed animation in `TypeWriter` increased to 3 from -1 being the default speed.
3. `CMS` added for `MyStory` screen to show "real" and "actual" story with full typing animation and effects. 
4. `ReRender` component added
5. Basically it is a safer way to `rerender` without having to use `forceRender` functionality
6. Added `ReRender` as `reRender` in `Utils` library
7. Added internal `random key` to `TypeWriter` as required by React
8. Disabling rereading story feature as `react-typing-animation` needs to support `reset` functionality internally.
9. Developing custom solution is not a high priority myself nor something of recommendation.
10. Fixed a bug in `getBottomAppBarPath` in `Routes.js` where if a `route` is in "home" than return home icon
11. Added `key={ Math.random() }` to a `list` as React complains too much when an `element` in a list does not have unique `key`.
12. The merit of using `key={ Math.random() }` is debatable because it makes impossible to identify the react `element` using unique key for any purposes.
13. Added `key={ Math.random() }` to `More.js` screen as I forgot to add.
14. Changed `Projects` screen to `Work Experience` screen
15. Added `SimpleCardList` which is built on top of `SimpleCard` for listing an array of cards from `CMS`
16. `More` screen now using `SimpleCardList` and debloating some of the code as a result of it.
17. Added `standardizeText` function to `Utils` which simply parses the HTML if `text` contains marked up `HTML` and also `text` can be simple string or `array` of text
18. This functionality was being duplicated at more than 3 different components hence the call to `standardize` it all in one place
19. `SimpleCard`, `ComplexCard`, `CustomTypography` all now rely on `standardizeText` of `Utils` so that central functionality can be changed easily from one central place.
20. `SimpleCard` now requires new property `noStandardizeText` which will not `standardize` it's `text` property. Main use case for this is if `text` is a `CustomTypography` component or other custom component in which case the `standardizing` will take place inside the component.
21. `MyStory` benefiting from `noStandardizeText` property as previous update would have broken it.
22. `Work Experience` screen updated with cards
23. Added neccessary `CMS` to it.

## 18-02-2020
1. `safeColor` functionality removed from `Colors` due to `circular reference` 
2. `safeColor` functionality added to `Themes` - it makes sense for it to be there
3. App's font sizes are now responsive
4. `PageTitle` component added to main App which can effectively show each screen's page title based on the screen automatically without having to place  `PageTitle` on each screen.
5. `Routes` screen name change to Welcome as oppose to boring "Home"
6. Change to Home `CMS` - slight variation of words
7. `ComplexCard`'s `actions` property now automatically enables navigating using `CMS`
8. Initial `MyStory` screen added
9. Initial navigation working
10. Home `CMS` updated to all work
11. Much improvements to `TypeWriter` component
12. `CMS` `line` data can now be an `array` of simple text
13. Backspacing had a bug  - it would calculate the number of backspaces based on HTML text which meant `<span>Hi</span>` would result into `15` backspaces as oppose to `2` 

## 17-02-2020
1. `TypeWriter` component added for typing animation effect
2. Full `HTML` formatting supported
3. Customizable in terms of delaying between each line
4. `SimpleCard` allows customised `width` for ease or for bespoke situations
5. `makeStyles` moved inside `function` to allow dynamic value setting
6. Changed `routes`'s `route` property to `path`
7. Changed structure to allow more central control from `routes` component
8. Getting rid of `bull` • `variable` of `SimpleCard`
9. Renaming of `routes`'s function `routing` to `getBottomAppBarPath` to avoid any confusion or as to what the function does
10. Added `getPageTitle` to `routes` for getting screen's title based on the URL route

## 16-02-2020
1. Fixed a bug in `ComplexCard` and `CustomTypography` where if text is
   not in array it would not be `parsed` for HTML.
2. CSS classes `highlight` improved
3. `border` new `class` added.
4. `underline` now uses `border-bottom` for superior style than `font-style: underline`
5. `italics` removed
6. Home `CMS` now benefits from new changes built for formatting of content

## 15-02-2020

1. `ComplexCard` now support `HTML` formatting for easy styling of content
2. `ComplexCard` now supports line breaks based on fullstop `.` for easier reading style 
3. `CMS` text can be set as simple text or in an array. `ComplexCard` deals with it appropriatley
4. `CustomTypography` also supports `HTML` formatting just as `ComplexCard` 
5. Line breaks are also supported for `CustomTypography` and `CMS` content for easy as array or text either way
6. 5 new `classes` added for formatting of text and ease of convinience!<br>
       `highlight`<br>
       `quote`<br>
       `bold`<br>
       `italics`<br>
       `underline`<br>
7. 

## 14-02-2020

1. Added `Beth Ellen` and `Reem Kufi` fonts and removed `Mr Dafoe`
2. Added `Bismillah` component<br>
   Basic philosophy of putting God first!
3. `Petit Formal Script` font removed
4. `Beth Ellan` font removed
5. 2 new fonts added: `Amatic SC`, `Bungee Shade` - both these are `display` fonts for drawing special attention
6. `ComplexCard` component now support custom `typography` for main text content
7. `Bismillah` now no longer `bold`
8. `Utils`'s `getCardActions` now expects an array rather than entire `card`<br>
   This means `getCardActions` can be envoked from `SimpleCard` internally for simplification purposes
9. `BottomAppBar`'s gradient transparency is increased to 70% from 60%
10. `SimpleCard` expects now an array of plain `actions` as oppose to returning a JSON object of actions, this is now done from inside       `SimpleCard`. This way the main control can be changed from within `SimpleCard` in near future
11. `CMS` inside `More` component has been renamed to `MoreCMS` for easiser searching from within `vscode`
    Simplification of syntax to `SimpleCard` according to recent changes made to `SimpleCard`
12. Added `expandButton` property to  `ComplexCard` component so that it can be easily used to expand card but using some button text -       This effectively means expand button is duplicated but one with a text as not everyone may be used to expanding it or may not know       what expansion content contains. In that situation having a button text is very useful.
13. `ComplexCard`'s `imageURL` now expects only the file name, no longer a `path` as this is centrally done from within `ComplexCard` for     simplification and centralised purposes.
14. Added `margin` 10 to `ComplexCard` so that when used in list - they have some border and distance  between each other
    Same behaviour as `SimpleCard`
15. Changed `text-align` to left side for expansion text for `ComplexCard` component 
16. Added `CMS` for Home screen
17. Added initial profile card for main home screen


## 13-02-2020

1. Added material design `icon` support for `SimpleCard` component
2. Added "outline" `variance` to `card` button
3. Benefiting from `icon` support and setting icons dynmaically
4. Added a material design `ComplexCard` component with fully dynamic anatomy
5. `ComplexCard`'s `avatarInitials` removed - it is now automatically generted from `title`
6. Some refinments added
7. `CSS` added for custom styling and easy to change in regards to Chrome `Developer Tools`
8. Enhanced `Card`'s `CSS` so it does not get stretched up depending on the one of the children taking more.
   <br>It is still not fully Google Images like but a little better. Far from it.
9. Made card more `rounded` for an elegant look and feel
10. `ComplexCard`'s image is now `rounded` too which is debatable whether it looks pleasant or just to me
11. Added `margin-right` to `card`'s action buttons so that it does not look squished when there is more than 1 button. 
12. Added custom `Typography` components
13. Added `CustomTypography` component for easy change of fonts for certain type of components
14. Changed `Signature` component with different `Charmonman` font


## 12-02-2020

1. Added linear progress bar and its `API` for easy control of `on` and `off`
2. Fixed `gradient animation` <br>
   Was previously broken but was not noticed

## 11-02-2020

1. Added the ability to show `labels` for `BottomNavigation` for internal purposes
2. Fixed some potential spelling `bugs` or misleading `variables`
3. Added initial progress bar for `AJAX` progress and anything else it may be useful for
4. Added `safeColor` function that will return safe random color which will not be innappropriate for the `set` theme

## 10-02-2020

1. Fixed a bug that broken `live` production

## 09-02-2020

1. Changing theme `on the fly` works! - no need to `reload` page
2. Theme saving also works - once saved always saved until changed
3. `Nested routing` is working as expected - not in the way I thought but outcome is still the same
4. `Bottom App Bar` is more like translucent in line with the overall theme
5. Added `Utils` for simplified development
6. Added `CMS` via `JSON` for easy changes to actual content
    6.1. This is also to keept content strictly separate from `logic`
7. Theme changing is simplified or the apprach is

## 05-02-2020

1. Integrated Material-UI `BottomNavigation` with `reach-router` using custom hybrid solution
2. Fixed Material-UI `BottomNavigation` back button not changing Material-UI `BottomNavigation` buttons
3. Added `routes.js` file for all the routes for the main control
4. Added function in `routes.js` `routes.routing()` function which deals with routing
5. Added 28 different gradient themes
6. Integrated Material-UI `BottomNavigation` with gradient themes
7. Added `default` route component for common 404 error pages etc
8. Changed overall structure for cleaner and simple structure
9. Changed `location` to `window.location` as it causes build error on netlify deploy <br>
        Still do not understand how it works on `localhost` but not when `deployed`
10. Accidentally disabled `history` which disabled going back so now re-enabling it to allow user going back using `back` button

## 31-01-2020

 1. Material-UI integration<br>
    Basically working - just checking it 
 2. Added basic routing using `Reach Router`<br>
    Setup the `router`

## 29-01-2020

 1. Created `components` folder<br>
    Cleaning up so that `lambda` functions are located seperateley<br>
    Cleaning up of `App.js`<br>
 2. Added basic routing using `Reach Router`<br>
    Setup the `router`


