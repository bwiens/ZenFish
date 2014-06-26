zenfish Drupal Theme, built on Zen (the most downloaded Drupal theme). Responsive and based on SASS.

Sources:

zenfish_Theme.zip

https://drupal.org/project/superfish

https://drupal.org/project/zen
Step-by-step guide

 

    Install Drupal

    cp -R zenfish_theme/ /var/www/html/kutztown/sites/all/themes/

    cp -R zen/ /var/www/html/kutztown/sites/all/themes/

    Install Modules and Libraries: Libraries, Superfish, JQeasing, JQuery_update, Nice Menus (?)

    Sites > All > Appearence > Set as needed

    Structure > Blocks: Superfish: Navigation Bar

    Configure: Menu Type: Navbar, Style: White (that's were all the modifications are, other minor things: see composer), Region zenfish Drupal Theme Navigation Bar

    Remove Structure > Blocks > Footer, Add Block > Custom Footer, zenfish Footer: Powered by the <a href="https://zenfishpa.org"  target="_blank">Keystone Library Network<a>

    Right-click Superfish Menu and Configure Block: Block Title: <none>. For the Menu Interface to work properly, you need at least 2 items since one of them is defined as .first. Keep Home as .first to activate the -9999px replacement for the House-Icon (copy over icon in appropriate directory)*.

    * If the menu stays auto expanded on sub-itmes, play with the weight settings.

 

As seen on http://sandbox.ship.edu/kutztown/
Most Menu Costumizations are in white.css in the superfish library
All zenfish Zen Theme Costumizations are in zenfish.css in zenfish_theme folder

Below is a sample of what the theme will look like, minus the Kutztown branding.