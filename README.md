What is it?
===========

This is a tap file to add support for LXQt Archiver to the thunar-archive-plugin 
in the Thunar File Manager, which adds archive operations to the file context menus.


Installation
==========================

Ensure that you have a .desktop file for LXQt Archiver installed in
the $(datadir)/applications/ folder. This is usually either /usr/share/applications
or /usr/local/share/applications.

Add the tap file to your $(libexecdir)/thunar-archive-plugin/ folder. This is most
likely found in /usr/lib/xfce4/thunar-archive-plugin/.

Ensure that the .tap file is named identically to your .desktop file so that Thunar
is able to confirm that the application is installed.

Note that the thunar-archive-plugin takes the applications from the desktop
database, so after installing new archive managers in $prefix (i.e. /usr or
/usr/local), make sure to run

 update-desktop-database $prefix/share/applications

Most modern packagement systems will do this for you automatically, but if
you are installing archive managers manually, you may need to run the above
command first, otherwise you will get an error message telling you that no
support archive managers were found on your system.
