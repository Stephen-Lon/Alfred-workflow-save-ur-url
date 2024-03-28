# Important note
*Version 4.5 (and later) of this workflow requires Alfred 5.5 (and above).* It uses Alfred 5.5's Text View action. If you are not using Alfred 5.5 (or later) please install [version 4.1](https://github.com/Stephen-Lon/Alfred-workflow-save-ur-url/releases/tag/v4.1) of this workflow.

# Introduction

Sometimes when browsing you want to save a URL quickly for future reference without creating a bookmark in your browser. That is what this workflow does. It uses a simple plain text or markdown file (which will be created for you when you first run the workflow if the file doesn't already exist) to which saved URLs will be appended. You select the location folder for that file in the workflow configuration opposite.

# Setup

In the workflow configuration choose:
- the folder where you want to keep your `Links` file;
- the keyword you want to use to *open* the `Links` file;
- the keyword you want to use to *search* the `Links` file;
- whether you want to use markdown (check the relevant box) or plain text;
- whether you want the workflow to attempt automatically to extract the web page title for the description field (see separate note below);
- whether you wish to mute the sound effect when adding a new link (uncheck the relevant box);
- whether you want to open a found link in a Firefox private window (check the relevant box).

# Usage

## Saving URLs

Using your Universal Action hotkey on a selected URL, select `Save URL to links file` from the list and press <kbd>⏎</kbd>:

<img width="764" alt="SaveURL" src="https://github.com/Stephen-Lon/Alfred-workflow-save-ur-url/assets/111967061/c2c1849a-451e-4ee1-8cb4-f2f9d9912416">

You will then be prompted for a description of the URL (which may be a useful reminder). Type the description (or accept or amend the description if you have checked the configuration for the workflow to attempt to complete the description from the web page title) and press <kbd>⏎</kbd>. If you are using a plain text `Links` file you can leave the description blank by simply pressing <kbd>⏎</kbd>. If you are using a markdown `Links` file you must complete the description:

<img width="764" alt="MDTitlePrompt" src="https://github.com/Stephen-Lon/Alfred-workflow-save-ur-url/assets/111967061/a1f1854c-70aa-4209-a5f5-e9240af82c1c">

The result will be a file which you can open in Alfred's Text View (see below for examples).

## Viewing, editing and clearing the `Links` file

Type the keyword (selected in the workflow configuration) to open the `Links` file then:
- press <kbd>⏎</kbd> to open the Links file in Alfred's Text View from where it may be viewed or edited; or
- press <kbd>⌘</kbd><kbd>⏎</kbd> to create a *new* links file in your chosen format (effectively deleting any URLs you have previously saved to the file).

If you choose to view the `Links` file this is what it looks like in plain text:

<img width="764" alt="ViewPlainLinks" src="https://github.com/Stephen-Lon/Alfred-workflow-save-ur-url/assets/111967061/400bcbf9-b5c6-4a74-9f59-dd942c5b2e80">

This is what it looks like if you choose to use markdown:

<img width="764" alt="ViewMDLinks" src="https://github.com/Stephen-Lon/Alfred-workflow-save-ur-url/assets/111967061/e75bccaf-e56c-4018-a983-82f2041f31bb">

In both cases the prompts at the bottom of the window are the same:
- press <kbd>⌘</kbd><kbd>⏎</kbd> to edit the Links file (see below);
- press <kbd>⌘</kbd><kbd>0</kbd> to toggle the size of the Text View window if necessary;
- press <kbd>esc</kbd> to end the workflow.

Selecting the option to edit the `Links` file will:
- if you have used markdown open the file in your default markdown editor;
- if you have used plain text open the file in Alfred's editable Text View window (from which you can choose to save changes or exit the workflow without saving changes—see the prompts at the bottom of the Text View window when in edit mode).

## Searching URLs in a `Links` file
The search is a case insensitive search for a word which occurs in a saved *URL*—*not* for a word in any *description* of a URL that you have saved. Simply type your search keyword and the relevant URLs will display in Alfred's window. (If you want to display all of your saved URLs type `ht`.) Press <kbd>⏎</kbd> to display the first or any selected URL in your chosen browser (or press Alfred's shortcut key—<kbd>⌘</kbd><kbd>2</kbd>, <kbd>⌘</kbd><kbd>3</kbd>, etc.—to display the relevant URL in your chosen browser). Here is an example of a search result:

<img width="764" alt="SearchLinks" src="https://github.com/Stephen-Lon/Alfred-workflow-save-ur-url/assets/111967061/c38767a0-5ee1-4514-a76d-5f4cb105c88a">

You will be warned if:
- the `Links` file does not exist; or
- your search term is not found.

# Configuration options
As mentioned above you can choose (among others):
- The keyword you wish to use to trigger a search of the `Links` file (the default is `flinks`—for "find links").
- Whether you wish the selected URL to open in your default browser or (if you use Firefox) in a Firefox private window.

**Warning**  
There is no error trapping if in the configuration you set the option to view URLs in a Firefox private window when you don't have the Firefox app...but then you wouldn't do that, would you? 😀

## Extracting web page titles for description field

**Note**: Be aware this feature can on occasion, and with some websites, lead to strange results. However if and when it does you can easily overwrite the description field with your own text.

If you check the relevant box in the user configuration the workflow will attempt to extract the title of the web page for which you are saving the URL and put that title in the description field. *If the workflow is unable for any reason to retrieve the title the description field will simply be left blank for you to complete*.

If you prefer to complete the description field yourself simply leave unchecked the relevant check box.

# Acknowledgements
I am indebted to @vitor on the Alfred forum for huge help with the script filter and to @Acidham on the forum for the contribution that enabled extraction of the web page title.
