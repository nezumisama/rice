## Css files for stylish. 
They can also be used for userChrome.css/userStyle.css.
* `xul.css` themes the Firefox UI.
* `about:newtab.css` themes the "speed dial" page in Firefox.
* `forms.css` changes a few properties of form elements to make them look better.
* `view_image.css` themes background image on image view pages (this works together with the extension *pic style - checkerboard*.
* For other files the name should tell you what does that file theme.
## Updating
This directory contains an update script that will update the code in stylish database for each style. Note if a style with the same name as the file name (minus extension) doesn't exist, the script won't do anything. I don't know for sure how stylish adds new styles to that database so I can't make an install script. Therefore, to add styles, create ones with the stylish UI, with the same names as the relevant files and then use this script. 
The script takes no arguments. If you want to answer yes to all questions, which will make it try to update style from every css file in this directory, you can use the *NIX `yes` command, like so: `yes y | ./update`.
Note this script uses the python 2 script `stylish_import_style` from the `utils` directory.
## Notes:
* To make my life easier I use a Firefox theme called FT Deep Dark and use stylish to change some things. If you use the default theme or a different one, some stuff may not look as intended, because of different defaults.
* The xul style styles the interface but doesn't move stuff around. To do that, click with right mouse button on any toolbar and select "Customize". Then you can move stuff around. I have only the tabs toolbar enabled, I have tabs there and urlbar right of them.
