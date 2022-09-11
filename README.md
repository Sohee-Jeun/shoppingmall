# MiniGame Shoppingmall Game
This is the toy project for using JSON and PWA.
## JSON

### When you build JavaScript, you should think about those steps first

- Design from the skeleton to see what type of motion it will be! 
  - Item data call succeeds.
    1. output data.
    2. Set events related to data.
  - If the data call fails, an error is handled.
- As you create the function, check that the result is still output (check the function action and json output through the console)
- Convert json data so that it can be output to html.
  1. Create json data variable with document.querySelector (const container)
  2. Create a function that returns json in html format (function createHTMLString(item))
  3. Update as a single string in container.innerHTML with map and join
  
## Fetch the items from the JSON file
```
function loadItems(){
    return fetch('data/data.json')
    .then(response => response.json())
    .then(json => json.items);
}
```

The function loadItems retrieves data using fetch, and if the received data is successful, it converts it to JSON and returns the items in json. In short, it takes the resource of loadItems 'data.json', converts it to json, and returns the items contained in json.

fetch provides a fetch API, a way to asynchronously fetch resources from the network. Below is an example of setting up a basic import request.

```
function displayItems(items){
    const container = document.querySelector('.items');
    container.innerHTML = items.map(item=>createHTMLString(item)).join('');
}
```
<hr/>

## PWA
### What is PWA?
PWA, short for 'Progressive Web Apps', is a technology that provides a native app-like user experience on mobile sites.

Features that can be implemented in a PWA
- Add icon to home screen You can add an icon to the home screen of your smartphone.
- No installation required, like native apps PWAs are not apps, so users don't need to download and install them from the store. However, it can provide an app-like look and feel.
- Push Notifications You can send push notifications like normal apps.
https://www.pwabuilder.com/


