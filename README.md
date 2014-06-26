ZenFish Drupal Theme, built on Zen (the most downloaded Drupal theme) with a customized Superfish Menu.

Sources:

https://drupal.org/project/superfish

https://drupal.org/project/zen


Installation

First, clone the theme onto your Drupal instance
```
git clone https://github.com/bwiens/ZenFish.git
```

Then, copy the theme folders and superfish libraries (which contain css customization).
```
cp -r zen/ and kln_theme/ into /var/www/html/sites/all/themes/
cp -r superfish/ into /var/www/html/sites/all/libraries/
```

Install Modules and Libraries:
These wget addresses are current as of this writing.
You can find updated addresses from the following pages:
https://www.drupal.org/project/libraries
https://www.drupal.org/project/superfish
https://www.drupal.org/project/jqeasing
https://www.drupal.org/project/jquery_update
```
# Move into the modules folder
cd sites/all/modules

# wget the drupal modules
wget http://ftp.drupal.org/files/projects/libraries-7.x-2.2.tar.gz
wget http://ftp.drupal.org/files/projects/superfish-7.x-1.9.tar.gz
wget http://ftp.drupal.org/files/projects/jqeasing-7.x-1.0.tar.gz
wget http://ftp.drupal.org/files/projects/jquery_update-7.x-2.4.tar.gz

# Unzip them in the modules folder
cat *.tar.gz | tar -xzvf - -i

# Remove the unzipped tar files
rm -rf *.tar.gz
```

In order to install superfish, you need to include the superfish library.
You can get an updated wget address from the above superfish drupal link.
```
cd /var/www/html/sites/all/
mkdir libraries
cp -r superfish /var/www/html/sites/all/libraries/
```

After putting the modules into /sites/all/modules, you need to enable them.
The modules you need to enable are: Libraries, Superfish JQuery Easing, and JQuery Update
In the admin toolbar: Modules > List tab > check the modules > Save Configuration

Then download and install the Zen theme
```
cd sites/all/themes/
wget http://ftp.drupal.org/files/projects/zen-7.x-5.5.tar.gz
tar -xzvf zen*
rm -rf *.tar.gz
```

You can now enable the zenfish Drupal Theme.
Go to the administrator toolbar > Appearence > Click enable on the zenfish Drupal Theme and set as default

In order to add Superfish as a block do the following:
In the admin toolbar: Structure > Blocks > Superfish > set to Navigation bar
Set Search form to None in blocks or accomodate your css to include it.

Click on configure next to Superfish
Under Superfish settings, Select NavBar as Menu type and white as the Style


Menu Type: Navbar, Style: White (that's were all the modifications are, other minor things: see composer), Region zenfish Drupal Theme Navigation Bar

8. Remove Structure > Blocks > Footer, Add Block > Custom Footer, zenfish Footer: Powered by the <a href="https://zenfishpa.org"  target="_blank">Keystone Library Network<a>

9. Right-click Superfish Menu and Configure Block: Block Title: <none>. For the Menu Interface to work properly, you need at least 2 items since one of them is defined as .first. Keep Home as .first to activate the -9999px replacement for the House-Icon (copy over icon in appropriate directory)*.

* If the menu stays auto expanded on sub-itmes, play with the weight settings.

Most Menu Costumizations are in white.css in the superfish library.
