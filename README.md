## Responsive header (and footer)  

This is a front-end conversion (excepting Javascript!) of the existing Vuforia header and footer to enable responsive viewing from the smallest device to full desktop viewing. Javascript is not my speciality so I am relying on your or your team's expertise to hook up where necessary.  

All code has been "scraped" from the exising structure and pains have been taken to keep things as close as possible to that.  

Although I've gone into details to point out things here, please study the structure closely and feel free to ping me with questions.

##### It is important to point out a few differences that will be unique to this conversion:  
*  Login & Register text rests now on the "bottom" of the green bar  
*  Font call is new, it is to OpenSans and the folder structure will need to be set up so the CSS file paths will work  
*  Clicking on Downloads, Develop, Support and Admin will now display a sub-menu, these are also used for the responsive view  
*  In the responsive menu dropdown > User (Currently "JohnDoe"), there is the ability to list number of messages. This feature wuould need to be connected, leave it up to the team to decide whether it's within scope  
*  There may be some slight visual changes but I have taken pains to match the existing look and feel as closely as possible. If you see something that you feel needs attention please ping me.  

#### Login and Logged in menus (right side)  
Both login states (lines `124` and `144`) are toggled on and off by adding removing `logged-state` class to the parent div. The `collapse` class stays. On responsive view these menus dissapear. The responsive user logged-in menu starts on line `45` and login / register is shifted to the icon of the user. Touch the icon will take the user to the login / register page.  The user icon is enabled through FontAwesome, link line `15`.

#### Highlight states (desktop view)  

The highlighted state (currently set for Downloads), is from the `active` class, refer to line `63`. This will need to be toggled as the user clicks the various options, and removed after another option is selected.  
*  for home add class to the `li` line `61`  
*  Pricing: same as above, line `62`  
*  Library: same, line `75`  
*  Develop: same, line `76`
*  Support: same, line `85`  
*  Admin: same, line `95`

#### Gray submenu bars (desktop)  

As I've sent to you, the Downloads submenu is showing (with corresponding highlight state on Downloads) to give you visual example. Each bar has been assigned an `ID` if needed (they can be removed if you wish). These bars visibility are toggled by adding/removing the `collapse` class.  
*  Downloads menu: starts line `156`  
*  Develop menu: line `166`  
*  Support menu: line `175`
*  Admin menu: line `185`

#### Footer  

The footer has a separate CSS stylesheet for it. Do pay attention to the path in the `social-media` class to ensure the icons are displayed. Beyond this it's pretty straight-forward. I added a spacing div line `216` to separate the footer, do not include this in production code.

The menu can also be [viewed on my sandbox here](http://pchapman-sandbox.dev.vuforia.com/).
