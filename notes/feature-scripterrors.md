# Script editor error handling has been improved

The behavior of the script editor has changed in the following ways:

* Previously when a user applied a script that did not compile the
script was set on the object anyway. This behavior has now changed to
*only* set the script if it successfully compiles. If the user tries
to close the script editor or save the script of an unset script a
warning dialog appears to allow setting the uncompilable script. This
change means that users working with preserveVariables true do not lose
the value of script local variables when editing scripts.

* Previously when opening a script that was not able to be compiled
a compilation error would not be shown until the script was modified and
then applied. The script editor will now attempt to compile scripts when
opened in order to present errors without user interaction.
