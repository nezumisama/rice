## Css files for [stylish](https://addons.mozilla.org/en-US/firefox/addon/stylish). 
They can also be used for userChrome.css/userStyle.css.
* `xul.css` themes the Firefox UI.
* `xul_big.css` is an additional style to be used with the above. Makes elements bigger.
* `about:newtab.css` themes the "speed dial" page in Firefox.
* `forms.css` changes a few properties of form elements to make them look better.
* `view_image.css` themes background image on image view pages (this works together with the extension *pic style - checkerboard*.
* `tabview.css` themes the tab groups view in Firefox.
* For other files the name should tell you what does that file theme.

## Updating
This directory contains an update script that will update the code in stylish database for each style. Note if a style with the same name as the file name (minus extension) doesn't exist, the script won't do anything. I don't know for sure how stylish adds new styles to that database so I can't make an install script. Therefore, to add styles, create ones with the stylish UI, with the same names as the relevant files and then use this script. 
The script takes no arguments. If you want to answer yes to all questions, which will make it try to update style from every css file in this directory, you can use the *NIX `yes` command, like so: `yes y | ./update`.
Note this script uses the python 2 script `stylish_import_style` from the `utils` directory.

## Notes:
* All these files are created, tested and used by me on Firefox's current stable version. I suggest using Firefox (or Gecko in general), though you can use these css files on other browsers. However, there could be problems with this. I'm trying to not use features limited to gecko, but it's not always the case. Another source of problems could be prerelease versions of FF.
* The xul style styles the interface but doesn't move stuff around. To do that, click with right mouse button on any toolbar and select *Customize*. Then you can move stuff around. I have only the tabs toolbar enabled, I have the menu button there, then tabs and urlbar right of them.
* If you want to hide something, like the menu button, edit the relevant css, find the rule for the element you want to hide (the css files have comments for most rules telling what this rule styles) and add this on a new line between `{` and `}`: `display: none !important;`. 
