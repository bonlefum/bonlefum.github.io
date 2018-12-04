* Interesting collection: https://hackernoon.com/12-cool-things-you-can-do-with-github-f3e0424cf2f0
* apparently diretoy listing is possible
   https://stackoverflow.com/questions/21395159/shell-script-to-create-a-static-html-directory-listing

* gotcha: every md doc in the gh pages needs to have the header information -- seems to be a yaml document. The section itself can be empty, but must be present. (It is called "Front matter")
    * with an excepion... inside the _posts directory.
    * and a quirk.  If the header is absent, we can see the raw page and the formatted one.
    (the former is `file.md`, the latter is `file.html`); however if the header is included
    then the raw file is gone and only `file.html` exists on the site. 

