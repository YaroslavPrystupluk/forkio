# Make a layout

Teamwork.
In this project, all students are divided into groups of two. Each team member is given a list of tasks to complete. The team members can decide who will perform task #1 and who will perform task #2.

Technical requirements for the layout
You are given a website layout in three versions - 320 pixels, 768 pixels, and 1200 pixels.
The layout should be made taking into account the principles of adaptive layout, i.e. all blocks/columns should change their relative position when the screen resolution becomes too small for them to be located on the same line.
The 320 pixel wide layout shows how the content will look when the screen width is from 320 to 480 (!) pixels (320 pixels is the minimum width of the content, it should not be narrower).
The 768 pixel layout shows how the content will look when the screen size is from 481 to 992 (!) pixels.
The 1200 pixel layout shows how the content will look when the screen width is 993-1200 pixels. That is, where in the 768 layout there were two columns somewhere, and in the 1200 layout there are four, the change from two to four should occur when the screen width reaches 993 pixels.
If the screen is wider than 1200 pixels, the content should occupy exactly 1200 pixels and be centered.
The content container should have side padding - 10 pixels on both sides, on all screen variants.
The layout should look good both at the specified boundary points and at any screen width between them.
There are two additional layouts - Hover and 320 drop down crop. Hover shows how all elements should look when you hover the mouse cursor. drop down crop - shows how the top menu should look like on mobile devices (with a width of up to 480 pixels inclusive).It should open when you click on the menu burger icon. It should be closed by clicking on the cross icon or by clicking outside the drop-down box.
All styles must be written in SCSS files
All classes on the page must be defined using the BEM methodology
Task for the student #1
Design the header of the site with the top menu (including the drop-down menu at low screen resolution.
Design the People Are Talking About Fork section.
Task for student #2
Design the Revolutionary Editor block. The buttons should be made to look like the one on the top right (you can also use the inspector to take all the SVG icons and download the styles used on the github).
Make the Here is what you get section.
Build the Fork Subscription Pricing section. In the block with prices, the third element will always be "highlighted" and will be larger than the others (i.e. not by click/hover, but statically).
General task for the team:
Create a README.MD file in the root of the project:
List of technologies used
The composition of the project participants
What tasks did each member perform
The code of both team members should be in the same repository.
Set up a project build using Gulp (see requirements below).
Post the project on the Internet using Github pages or Gitlab pages (don't forget to add a link to your resume later).
Build the project:
The project should be built using Gulp
There should be two folders in the project root - src and dist, as well as the index.html file
The styles and script in index.html should be included from the dist folder
The src folder should contain all the working files in which you will write the code (scss, js, img folders)
The contents of the dist folder should be generated automatically by converting and copying the files in the src folder
You need to set up two main work tasks for Gulp:
dev
build
The build job should include the following tasks:
cleaning the dist folder;
compile scss files into css;
Adding vendor prefixes to CSS properties to support the latest several versions of each browser;
removing unused CSS code;
concatenating all js files into one scripts.min.js and minifying it;
copying the minified final styles.min.css and scripts.min.js files to the dist folder;
optimizing images and copying them to the dist/img folder;
The dev work task should include the following tasks:
Launching the server and further tracking changes to *.js and *.scss files in the src folder;
When you change it, you need to rebuild and copy the combined and minified styles.min.css and scripts.min.js files to the dist folder, and reload your html page.
You can use any package to build your project, but most of the necessary functionality can be found in the following ones:
gulp
gulp-sass
browser-sync
gulp-js-minify
gulp-uglify
gulp-clean-css
gulp-clean
gulp-concat
gulp-imagemin
gulp-autoprefixer
