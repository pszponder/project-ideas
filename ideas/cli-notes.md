# CLI Notes / Code Snippet manager

## Project Name(s)

-   QuickNotes

## Idea(s)

-   CLI tool to take and manage notes / code snippets from the CLI
-   Would it be easier if CLI tool would open up Vim to take a note and then save it to a database on closing of vim? (As an alternative to typing notes into the terminal?) Maybe this can be an option?

## App requirements

-   Copy notes / code snippets into clipboard
-   Be able to save a string of text as a note
    -   Save a single-line string of text
    -   Save a multi-line string of text
    -   Tag a note with one or more tags during note creation
-   Be able to view a list of saved notes
    -   Retrieve last x notes
    -   Retrieve notes from today
    -   Retrieve notes from yesterday
    -   Retrieve notes from last x days
    -   Retrieve notes based on specific timestamp
    -   Retrieve notes older than specified timestamp (from beginning to timestamp)
    -   Retrieve notes newer than specified timestamp (from timestamp to end)
    -   Retrieve notes based on timestamp range
    -   Retrieve x random notes
    -   Retrieve a note based on note id
    -   Retrieve notes based on one or more tags
    -   Fuzzy search by note content
-   Be able to edit a note
    -   Edit note just retrieved from a search
    -   Select a note to edit from a list of notes returned from a retrieval (if retrieving multiple notes)
    -   Be able to update the text of a note
    -   Be able to add one or more tags to a note
    -   Be able to remove one or more tags from a note
    -   Be able to edit tags in a note
-   Be able to remove a note
    -   Remove note by id
    -   Remove note(s) based on tag(s)
    -   Remove note(s) based on timestamp range
    -   Remove note based on specific timestamp
    -   Select notes in a list to remove
-   Enable option to warn user before deleting note(s)
-   Be able to view list of tags

## Todos

-   [ ] Look up additional projects which may already provide code snippet / node managers to get ideas
    -   [ ] [pieces.app](https://pieces.app/)
    -   [ ] [pieces.app cli](https://code.pieces.app/updates/new-pieces-cli-for-macos)
-   [ ] Research how to deploy / install a cli tool so that it can be used globally from the command line
-   [ ] Research languages to use for CLI tool (Go or Python?)
-   [ ] Research how to enter multi-line strings and save them
-   [ ] Research a database to use (SQLite, PostgreSQL, or MongoDB?)
-   [ ] If using SQL, research how you could add multiple tags to an item but still be able to quickly search against multiple tags. (probably use a separate tags table which links via a one to many relationship to the notes table)
-   [ ] Start by writing to a file (.txt?) and then update to SQL?
-   [ ] Start simple, create a simple todo-like app by just giving capabilities for adding, viewing, updating and deleting lines from a text file.
-   [ ] Determine format of single-line and multi-line notes (ex. will notes have titles? will this be optional?)
-   [ ] Determine how will manage tags and notes (if a note is deleted, is the corresponding tag deleted?). Maybe there is a command which cleans up tags if they aren't being used by any notes?

## Resources

-   [nap - code snippet manager for your terminal](https://github.com/maaslalani/nap)
-   [Charm CLI - Nap: your new Leetcode BFF](https://www.youtube.com/watch?v=G1U4e1u-Sfc)
-   [SQLite](https://www.sqlite.org/index.html)
-   [Bubble Tea - Go framework for building TUI](https://github.com/charmbracelet/bubbletea)
