# The Idea

Nota is going to be an extension that pipes into the browsers' bookmarks and
browsing history. Sounds creepy, but it can all be self-hosted, which is why I
wanted to build it myself. The browser extenson would have a keyboard shortcut
that when pressed, will open a command-palette search of the user's history and
bookmarks.

## Why?

I am not personally a heavy user of bookmarks, but I've been in many
circumstances where I've been looking for a link _I Know I've Seen_, but either
can't find by googling or had seen it years ago.

## How?

Collect all browsing history via the [chrome.history](https://developer.chrome.com/docs/extensions/reference/history/)
API and upload it to the backend. This **wouldn't** upload the already-collected
history, only the new ones fired with events.

The backend would have some type of search indexing such as [MeiliSearch](https://github.com/meilisearch/MeiliSearch)
that exposes Lightning Fast search endpoints for the browser extension.

Under the options page for the extension the user can change the keyboard
shortcut needed to open the command palette.

## Goals

Nota has a couple of goals.

### For the MVP

- backend is self-hostable
- browser extension with fast search

### Later

- extension: custom history page
- extension: custom options page
- extension: actions with leading caret >
- website: same features as the extension
- app: react-native / flutter app?
