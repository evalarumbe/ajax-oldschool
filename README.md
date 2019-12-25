# Intro to AJAX

## What is AJAX anyway?

AJAX stands for Asynchronous JavaScript And XML, (but these days JSON is more popular than XML). The term 'AJAX' describes a pattern, so you won't usually see the term 'AJAX'  written in the code.

AJAX is a technique for accessing web resources asynchronously. This improves UX, because users can immediately see fast-loading content, while heavier files load in the background and appear when they are ready, without refreshing the page.

## Client-server relationship

AJAX handles requests made from a client (e.g. a browser) to a server (software whose purpose in life is to provide files upon request).

For this reason, you will need a server (like the Live Server extension for VS Code) to run this code. To check this is working properly:
**Your url should look something like this...** http://127.0.0.1:5500/path/to/file (accessing the file via server software)
**Not this...** file:///path/to/file (accessing the file directly from your file system)

Live Server is an example of a server that runs locally on your own machine. When you 'Go Live', your browser is making requests to your server. Even if they share hardware, keep this logical separation of client and server in mind. The script in index.html is running on the client, and making a request to the server.

## Traditional vs modern AJAX techniques

Async JS used to be done with the XMLHttpRequest object (XHR for short) and callbacks. This was very common for many years, and there’s still lots of code that looks like this in the wild. The example in index.html uses XHR and callbacks.

Modern JS would instead use the fetch method with promises, but it’s good to understand history first.

## Traditional vs modern event handlers

This example uses the inline `onclick` attribute because historical code is worth getting familiar with, but the `addEventListener` method is preferred in modern code.
