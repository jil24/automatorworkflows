# automatorworkflows
A few Mac OS Automator services & Applications

## Services:
* **Create SMB inetloc from selection**  
  While browsing a remote SMB share in the finder, this serivce creates a inetloc file directed to the selected item. This is a double-clickable or dock-clickable file which will connect to the same location. This kind of launcher tends to behave more relibly than aliases or placing network shares in the finder sidebar. They can't be easily created from the finder directly, but this service takes care of it.

*  	**Create symbolic link**  
    It's not rocket science. Make one or many symlinks at once.

*	**Move selected files to "Sorted"**  
    Creates a subfolder called "Sorted" in the folder you are working in, and moves the selected file(s) into it. [Assign this to a hotkey](http://apple.stackexchange.com/questions/43998/how-do-i-assign-a-keyboard-shortcut-to-a-service-in-os-x) to quickly sort files. (I use it to quickly sort the good photos.) If the folder already exists it just adds the files, and when you're done with one category you can rename or move the folder and start over again with the next category.


Since these are bundles, you should download a .zipped copy of the repository and move the bundles you would like to your `~/Library/Services/` directory.


----------
## Applications

*	**Make permissive ACLs:**
	Removes all ACLs from the selected folder, then applies a very permissive inherited ACL for the specified group (default is "staff"). Good for shared folders that you want contents put in by one user to definitely be readable by other users. Otherwise permissions have to be set manually by every user who puts files in the share, which is ridiculous.
	the actual ACL applied is: `allow list,add_file,search,delete,add_subdirectory,delete_child, readattr,writeattr,readextattr,writeextattr,readsecurity,file_inherit,directory_inherit`

