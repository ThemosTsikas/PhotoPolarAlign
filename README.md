# PhotoPolarAlign
A python utility to help align equatorial telescopes by imaging the Celestial Pole region.


Proposed new "Readme":

This script allows you to polar align an equatorial mount to the North Celestial Pole (NCP) using a camera or CCD (with camera lens) attached to the mount.

Briefly stated, one takes just two images of the North Celestial Pole (NCP) area and feeds these into the script which responds with the desired pixel positions of Polaris (Alpha UMi) and Lambda UMi. One then moves the mount so that Polaris is at those pixel positions (might take a few iterations and test shots to confirm).

To start off, you need to roughly align the RA axis with the celestial pole and set your camera pointing to declination +90 or as close as you can get it (so that Polaris and Lambda will be in the picture). Lock the declination at this stage and don't change it until PA is finished. The two images will be taken at different RA-axis positions, the first with the long side of the camera sensor vertical and the second with the long side of the sensor horizontal. That way, any recommended offsets in terms of image coordinates will translate naturally into left-right (azimuth) corrections and up-down (altitude) corrections for the RA axis. The script will also produce a plot for visual confirmation of where things stand and update plots after every repositioning of the RA axis (if a new image is taken after correction).

It is designed to run both under a Windows+cygwin environment and a Linux environment. It does not connect to or control your mount so it can be used with any Equatorial mount. All mount movement operations, whether in RA/DEC or Alt/Az, must be performed by the user, manually.
