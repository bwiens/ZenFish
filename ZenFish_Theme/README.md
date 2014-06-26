ZenFish Drupal Theme, built on Zen (the most downloaded Drupal theme) with a customized Superfish Menu.

Sources:

https://drupal.org/project/superfish

https://drupal.org/project/zen


Installation

1. git clone https://github.com/bwiens/ZenFish.git

2. copy folder ZenFish_Theme into themes folder in sites/all/themes/

3. cp -R ZenFish/ZenFish_Theme/* /var/www/html/sites/all/themes/

4. Install Modules and Libraries: Libraries, Superfish, JQeasing, JQuery_update, Nice Menus (?)

5. Sites > All > Appearence > Set as needed

6. Structure > Blocks: Superfish: Navigation Bar

7. Configure: Menu Type: Navbar, Style: White (that's were all the modifications are, other minor things: see composer), Region zenfish Drupal Theme Navigation Bar

8. Remove Structure > Blocks > Footer, Add Block > Custom Footer, zenfish Footer: Powered by the <a href="https://zenfishpa.org"  target="_blank">Keystone Library Network<a>

9. Right-click Superfish Menu and Configure Block: Block Title: <none>. For the Menu Interface to work properly, you need at least 2 items since one of them is defined as .first. Keep Home as .first to activate the -9999px replacement for the House-Icon (copy over icon in appropriate directory)*.

* If the menu stays auto expanded on sub-itmes, play with the weight settings.

Most Menu Costumizations are in white.css in the superfish library.
