# kd.js

a collection of ui widgets and other nice things.

```
npm i kd.js
```

# usage

```js
var main = new kd.View;
main.appendToDomBody();

var input = new kd.InputView;
var form = new kd.View;

form.addSubView(input);
form.addSubView(new kd.ButtonView({
  title: 'i\'m a button. type in your name and click on me',
  callback: function () {
    alert('sup ' + input.getValue())
  }
}));

var tabs = new kd.TabView({
  hideHandleCloseIcons: true,
  paneData: [
    {
      title: 'tab1',
      partial: 'that\'s me, tab1'
    },
    {
      title: 'form',
      view: form
    }
  ]
});

main.addSubView(tabs);
```

# example

Type `make example` and go to http://localhost:3000/example. This also starts a `watchify` process, so any changes you make in `example/index.js` will be recompiled on the spot.

# license

mit

