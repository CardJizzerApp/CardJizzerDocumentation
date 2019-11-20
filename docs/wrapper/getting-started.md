---
title: Installation
permalink: /docs/wrapper/getting-started
---

# Getting started with the NodeJs CardJizzer wrapper

## Installation
NOTE: Due to the WIP theres a high chance features that you currently implement in the Frontend may be a thing of the past in a version released a bit later. Please run the following command to install the package:
```
$ npm install cardjizzerwrapper
```


## Including in Typescript projects like Angular [WIP]
{% include alert.html type="warning" title="WIP!" content="This feature may or may be not implemented at the moment. It will be included in feature versions."%}

## Basic usage
```js
// Pass the backend url to the WebsocketWrapper options
const ws = new WebsocketWrapper({ url: 'ws://ENTER.YOUR.URL:HERE/' });
// Call the initialize function needed for establishing a connection to the backend
ws.initialize().then(() => {
    // Create a new object of the type wrapper taking the WebsocketWrapper-object as parameter.
    const wrapper = new Wrapper(ws);
    // Call the wrapper.Games.fetchGames() function returning a Games-array
    wrapper.Games.fetchGames().then((games) => {
        console.log(games);
    });
});
```