# Print Google Code Wiki

This project allows you to prepare a selected set of Google Code Wiki pages for printing.

# Usage

Copy the *printit.html* file into the directory in which your wiki files are located. For the subversion repositories, this typically is the wiki directory. For Mercurial and Git repositories, use the wiki branch. Now you can open the HTML file locally with a browser that allows file access from files (if you are using Chrome, you can enable this temporarily using the *--allow-file-access-from-files* command line argument). Should you have security concerns, you may also just commit the file and open it in the browser (remember to set the proper mime types).

# Hint

Should you need to export a larger number of similar documents, the following command may be useful for you. It searches for all files which contain the word *Decision* in a bold font face and formats the file names properly so that you only need to copy it into the input field.

    grep -H "*Decision*" /path/to/your/wiki/*.wiki | sed 's/^.*wiki\/\(.*\).wiki.*$/\1/g' | tr '\n' ','
