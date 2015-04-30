# Course-Notes

## Getting Started:

### Installing Git

1. Install git-bash: http://git-scm.com/downloads
2. You'll need a local version of the repo to work on, so open GitBash, navigate to your desired location for the repo, then run the following command to clone it:

```
git clone https://github.com/MaxOSmith/Course-Notes
```

### Setting up Sublime

1. Install Sublime Text (2 or 3): http://www.sublimetext.com/
2. Install Package Control (instructions on their website are very easy to follow): https://packagecontrol.io/installation
3. Install LaTeXTools plugin for Sublime
  1. Open Sublime text, then open it's command menu (CTRL + SHIFT + P)
  2. Select 'Package Control: Install Package,' if you start typing it will search for matches.
  3. Another menu that looks identical should replace it, but this time select 'LaTeXTools'
  4. It should download and install it for you.
  5. You need to migrate settings if this is the first time you've installed this package, so open the command menu again (CTRL + SHIFT + P) and then search for 'LaTeXTools: Reconfigure and migrate settings'
4. Install a TeX compiler based on operating system:
  1. Windows = MikTeX (http://miktex.org/)
  2. OSX = MacTeX (https://tug.org/mactex/)
  3. Linux = Read about it here: https://github.com/SublimeText/LaTeXTools
5. (Optional) In the Sublime's command menu (CTRL + SHIFT + P) select 'Package Control: Install Package,' then look for 'Non Text Files.' This will let you open any type of file from sublime using different software
  1. In Sublime: Preferences > Settings - User add 
  ```
  "open_externally_patterns":
  [
  	"*.pdf"
  ]
  ```
  this example will open all pdf files in your default pdf viewer, you can also do this with any other files you would like.
  2. Your settings should now look something like this:
  ```
	{
		"font_size": 8,
		"ignored_packages":
		[
			"Vintage"
		],
		"open_externally_patterns":
		[
			"*.pdf"
		],
		"update_check": false
	}

  ```
  If it's missing any of the other settnigs, that's completely fine, this is just an example.

### Sublime Workflow Tips

1. View > Sidebar > Show Side Bar, This sidebar shows all open files, and any folders you want to keep track of in your project 
  1. To add a folder simply drag the folder into the sidebar
  2. To remove a folder, WITHOUT DELETING IT, Right-Click > Remove Folder from Project

## Starting a New Course:

1. Copy and paste the Template folder 
2. Delete the section/lec-1Example folder, since it's just for examples
3. For each section make a new folder to hold all the relevant files
4. create a new file in the folder, I suggest 'page.tex,' but YMMV and put your notes in there, you don't need any fancy LaTeX document settings, use packages, just the content. You're welcome.
5. In the file 'Index.tex,' which is where we organize all of the pages, add under the 'Document Begins' comment 
```
\input{sections/<file-name>/page}
```
