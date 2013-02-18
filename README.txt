How I made the Akkadian syntax highlighting addin:

1. Made the MonoDevelop.AkkadianSyntax.addin.xml file.
2. Made the AkkadianSyntaxMode.xml file.
3. Downloaded mautil.exe (from MonoTools - was hard to find).  This is used to build (pack up) the addin.
4. Put mautil.exe in the folder with the two xml files.
5. Opened a command prompt and ‘cd’ to that same folder.
6. Typed the command: mautil pack MonoDevelop.AkkadianSyntax.addin.xml.  This created an .mpak file which incorporated all files referenced in the addin.xml file.
7. In MonoDevelop’s add-in manager, installed the .mpak file.


Notes:

* If the addin doesn’t seem to function properly (such as by not recognizing .akk files), try uninstalling and reinstalling it via MonoDevelop's add-in manager.  Also try enabling/disabling the addin.  Also try closing and reopening MonoDevelop.
* MonoDevelop custom highlighting schemes (such as MidnightHammurabiStyle.xml) are stored here: C:\Users\<user>\AppData\Roaming\MonoDevelop-3.0\HighlightingSchemes


References:

* http://monodevelop.com/developers/articles/syntax_mode_definition


TODO:

* Block comments
* Tvar?, Stub(), temporal:, set: