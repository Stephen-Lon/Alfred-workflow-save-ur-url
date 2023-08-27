# Alfred-workflow-save-ur-url
Save a selected URL to a text file (appending if the file exists). Updated for version 3.2.

# Introduction

Sometimes when browsing you want to save a URL quickly for future reference without creating a bookmark in your browser. That is what this workflow does. It uses a simple plain text or markdown file (which will be created for you when you first run the workflow if the file doesn't already exist) to which saved URLs will be appended. You select the location folder for that file in the workflow configuration opposite.

# Setup

In the workflow configuration choose:
- the folder where you want to keep your `Links` file;
- whether you want to use markdown (check the relevant box) or plain text;
- the keyword you want to use to open the `Links` file;
- whether you wish to mute the sound effect when adding a new link (uncheck the relevant box);
- the keyword you want to use to search the `Links` file;
- whether you want to open a found link in a Firefox private window (check the relevant box).

# Usage—saving URLs

Using your Universal Action hotkey on a selected URL, select `Save URL to links file` from the list and press ⏎.

You will then be prompted for a description of the URL (which may be a useful reminder). Type the description and press ⏎. If you are using a plain text `Links` file you can leave the description blank by simply pressing ⏎. If you are using a markdown `Links` file you must complete the description.

The result will be a file which you can open in your default file editor.

# Usage—opening and clearing the Links file

If you type the keyword (selected in the workflow configuration) to open the Links file:
- the Links file will open in your default file editor (and the editor selected may depend, of course, on whether you have chosen to save in markdown or plain text);
- you can hold down ⌘ while pressing ⏎ to create a *new* links file in your chosen format (effectively deleting any URLs you have previously saved to the file).

# Usage—viewing and opening saved links
## Warning
There is no error trapping if in this configuration you set the option to view URLs in a Firefox private window when you don't have the Firefox app...but then you wouldn't do that, would you? 😀

## Configuration options
As mentioned above you can choose:
- The keyword you wish to use to trigger a search of the `Links` file (the default is `flinks`—for "find links").
- Whether you wish the selected URL to open in your default browser or (if you use Firefox) in a Firefox private window.

## Searching URLs in a Links file
The search is a case insensitive search for a word which occurs in a saved *URL*—*not* for a word in any *description* of a URL that you have saved. Simply type your search keyword and the relevant URLs will display in Alfred's window. (If you want to display all of your saved URLs type `ht`.) Press ⏎ to display the first or any selected URL in your chosen browser (or press Alfred's shortcut key to display the relevant URL in your chosen browser).

You will be warned if:
- the `Links` file does not exist; or
- your search term is not found.

# Acknowledgement
I am indebted to @vitor on the Alfred forum for huge help with the script filter.
