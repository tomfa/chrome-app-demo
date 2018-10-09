# Chrome app example

A chrome extension is just a simple website with a `manifest.json` giving Chrome
some metadata about your app. Here's a simple chrome app example that replaces
the new tab page with a dummy trello todo-list.

## Awesome chrome extension list

Below is a few related links/guides for creating a Chrome extension of different
types that were helpful to me.

- [developer.google.com: Getting started](https://developer.chrome.com/extensions/getstarted)
- [thoughtbot.com: How to Make a Chrome Extension](https://robots.thoughtbot.com/how-to-make-a-chrome-extension)
- [freecodecamp.org: How to create and publish a chrome extension in 20 minutes](https://medium.freecodecamp.org/how-to-create-and-publish-a-chrome-extension-in-20-minutes-6dc8395d7153)

## Setup

### Trello

#### Required

- [A Trello account](https://www.trello.com)
- [Application key](https://trello.com/app-key)

The application key should be set in `globals.js`.

#### Optional

- [Application token](https://developers.trello.com/page/sandbox): Create a sandbox application
- Link to a Trello board you wish to connect to the app, e.g. [https://trello.com/b/lVGeY28u](https://trello.com/b/lVGeY28u)

With the last, you can find the id of the board, a todo list and a done list by adding `/report.json` to the url, e.g. [https://trello.com/b/lVGeY28u/report.json](https://trello.com/b/lVGeY28u/report.json).

Here you'll find the keys `id` (board id), and `lists[x].id` (list ids).

Set these in `globals.js` as well.

### Chrome

To load your extension in Chrome:
- Open up `chrome://extensions/` in your browser
- Click `Developer mode` in the top right.
- Click `Load unpacked` and select the repo directory on your machine.

You should now see your extension in the list, and if you open a new tab,
the background should be green. If you've set the application key in `globals.js`,
you should also see a list of Trello items from the Todo list in [https://trello.com/b/lVGeY28u](https://trello.com/b/lVGeY28u)
