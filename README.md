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

## 13-01-2010

1. Added material design `icon` support for `SimpleCard` component
2. Added "outline" `variance` to `card` button
3. Benefiting from `icon` support and setting icons dynmaically
4. Added a material design `ComplexCard` component with fully dynamic anatomy
5. `ComplexCard`'s `avatarInitials` removed - it is now automatically generted from `title`
6. Some refinments added
7. `CSS` added for custom styling and easy to change in regards to Chrome `Developer Tools`

## 12-01-2010

1. Added linear progress bar and its `API` for easy control of `on` and `off`
2. Fixed `gradient animation` <br>
   Was previously broken but was not noticed

## 11-01-2010

1. Added the ability to show `labels` for `BottomNavigation` for internal purposes
2. Fixed some potential spelling `bugs` or misleading `variables`
3. Added initial progress bar for `AJAX` progress and anything else it may be useful for
4. Added `safeColor` function that will return safe random color which will not be innappropriate for the `set` theme

## 10-01-2010

1. Fixed a bug that broken `live` production

## 09-01-2010

1. Changing theme `on the fly` works! - no need to `reload` page
2. Theme saving also works - once saved always saved until changed
3. `Nested routing` is working as expected - not in the way I thought but outcome is still the same
4. `Bottom App Bar` is more like translucent in line with the overall theme
5. Added `Utils` for simplified development
6. Added `CMS` via `JSON` for easy changes to actual content
    6.1. This is also to keept content strictly separate from `logic`
7. Theme changing is simplified or the apprach is

## 05-01-2020

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


