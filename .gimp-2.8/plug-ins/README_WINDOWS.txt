
resynthesizer and associated plugins for Windows
------------------------------------------------


Source may be found at  https://github.com/bootchk/resynthesizer

Compiled for Gimp 32 bit version for Windows on 17 April 2011.  Tested with Gimp 2.6.11 32 bits running on Windows 7.  This is compatible with many Gimp versions (all that use libgimp v2.0), with many Windows versions, and with many Python versions.

(This is v1.0 of the resynthesizer.  A later version, v2.0, does the same things, only faster, if you have a multicore processor.)


Installation for Windows
------------------------

These plugins require Gimp and Python.  (If you don't have Python installed, you can still install the two .exe plugins, and use Filters>Map>Resynthesize.  However, that plugin is not so easy to use.  The easy and most commonly used plugin is Filters>Enhance>Heal Selection, and that requires Python, or a Scheme version of the Heal Selection plugin, found in another package.)

Remove obsolete version 0.16 executable and scripts-fu :
 - resynth.exe
 - smart-enlarge.scm
 - smart-remove.scm
(For more information about other older plugins, see the README.txt file.)

Place the following ten files in the standard place for plugins for Gimp, typically ....\lib\gimp\2.0\plug-ins or C:\Users\[user]\.gimp-2.6\plug-ins.

 - plugin-heal-selection.py
 - plugin-heal-transparency.py
 - plugin-map-style.py
 - plugin-render-texture.py
 - plugin-resynth-enlarge.py
 - plugin-resynth-fill-pattern.py
 - plugin-resynth-sharpen.py
 - plugin-uncrop.py
 - resynthesizer-gui.exe
 - resynthesizer.exe



Using the different plugins:
----------------------------

The full power of the resynthesizer plugin appears in the Gimp menus as:  Filters>Map>Resynthesize. However, many users will prefer the other plugins, which have a simplified interface.  (Also note: with version 1.0, Filters>Map>Resynthesize will NOT synthesize a selection from the inverted selection in the same layer, as the previous version 0.16 did.  Instead, you must explicitly pass another layer having its own selection, to synthesize from.  Some old tutorials that use Filters>Map>Resynthesize will no longer work with version 1.0.)

For healing a selection from nearby pixels :  Filters>Enhance>Heal selection...  (Most users will use this.)

For healing transparent areas (for example that you have cut) from nearby pixels: Filters>Enhance>Heal transparency...

For transferring the style (color and texture) from one image to another:  Filters>Map>Style.
 
For rendering a seamless texture from one image into a new image : Filters>Render>Texture...

For enlarging an image using the resynthesizer to retain sharpness:  Filter>Enhance>Enlarge & sharpen...

For filling seamlessly with a pattern:  Edit>Seamlessly fill with a pattern using synthesis.

For sharpening an image using the resynthesizer :  Filters>Enhance>Sharpen by synthesis...

For enlarging an image while retaining the point of view of the existing image by synthesizing an enlarging border :  Filter>Enhance>Uncrop...




















