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

## 17-02-2020
1. `TypeWriter` component added for typing animation effect
2. Full `HTML` formatting supported
3. Customizable in terms of delaying between each line
4. `SimpleCard` allows customised `width` for ease or for bespoke situations
5. `makeStyles` moved inside `function` to allow dynamic value setting
6. Changed `routes`'s `route` property to `path`
7. Changed structure to allow more central control from `routes` component

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


