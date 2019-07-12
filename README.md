# Template assumptions

Reference: https://stmorse.github.io/journal/Thesis-writeup.html

* All images are contained in one folder, "img/"
* each chapter is a separate TEX file, found under "chapters/"
* there is a MASTER bibliography that each chapter references
* each chapter includes references at the end, specific to that chapter only

# Setup instructions

* Install Sublime 3
* Open this folder as a project
    * from scratch:
    	* Project > Open Project (will be empty)
    	* Project > Save Project As... > save to folder
    	* Project > Add Folder to Project
* Set custom build command
	* Find out where "Sublime Text 3/Packages" is located using Preferences > Browse Packages
	* Navigate to "Sublime Text 3\Packages\User\LaTeXTools-Builders"
	* copy/paste thesisBuilder.py into this folder
	* Open project settings using Project > Edit Project
	* copy/paste the following into the project settings (see thesis-template.sublime-project for concrete example)

'''
	"settings" : {
        "TEXroot": "dissertation.tex",
        "tex_file_exts": [".tex"],
        "builder": "thesisBuilder",
        "builder_path": "User/LaTeXTools-Builders",
        "builder_settings": {
            "options": "--shell-escape"
        }
    }

'''

Now you should be able to build "dissertation.tex" by selecting it in Sublime and then building, using 'ctrl+B'
You may need to edit certain file paths...

# Thesis to-dos:

1. Edit preliminary pages for specific author
2. Fill out chapter files, adjusting content to match ucsd.cls (e.g. drop JNE/IOP formatting in tables)
3. Add shorttitle captions to figures and tables for their respective List of X
4. Consolidate all references into single bibliography, 'bib.bib'