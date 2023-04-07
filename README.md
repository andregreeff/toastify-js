
# Toastify

![Built with JavaScript](https://img.shields.io/badge/Built%20with-JavaScript-red?style=for-the-badge&logo=javascript)

[![toastify-js](https://img.shields.io/badge/toastify--js-1.12.0-brightgreen.svg)](https://www.npmjs.com/package/toastify-js)
![MIT License](https://img.shields.io/npm/l/toastify-js)

Toastify is a lightweight, vanilla JS toast notification library.

## Demo

[Click here](https://apvarun.github.io/toastify-js/)

## Features

* Multiple stacked notifications
* No blocking of execution thread

### Customization options

* Notification Text
* Duration
* Close icon display
* Display position
* Offset position

## Installation

#### Toastify now supports installation via NPM

* Run the below command to add toastify-js to your existing or new project.

```
npm install --save toastify-js
```

or

```
yarn add toastify-js -S
```

* Import toastify-js into your module to start using it.

```
import Toastify from 'toastify-js'
```

You can use the default CSS from Toastify as below and later override it or choose to write your own CSS.

```
import "toastify-js/src/toastify.css"
```

#### Adding Toastify to HTML page using the traditional method

To start using **Toastify**, add the following CSS on to your page.

```html
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/toastify-js/src/toastify.min.css">
```

And the script at the bottom of the page

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/toastify-js"></script>
```

> Files are delivered via the CDN service provided by [jsdeliver](https://www.jsdelivr.com/)

## Documentation

New toasts are created by calling the core `Toastify` function, and then shown to the user by calling it's `showToast` function.

```javascript
Toastify({
  text: "This is a simple toast using default values.."
}).showToast();
```

Toast are configured by means of specific keys in the configuration object passed in at the time of creation.

> Toast messages will be centered on devices with screen width less than 360px.

* See the [changelog](https://github.com/apvarun/toastify-js/blob/master/CHANGELOG.md)

## API

### `text` string (required)

Message to be displayed in the toast

* default: `undefined`
* notes:
  * toast will fail to render if a message is not provided.

### `node` ELEMENT_NODE

Provide a node to be mounted inside the toast. `node` takes higher precedence over `text`

* default: `undefined`

### `duration` number

Duration for which the toast should be displayed.

* default: `3000`
* options:
  * any positive integer in milliseconds
  * `-1` for a persistent toast that must be explicitly dismissed
* notes:
  * this implicitly enables `close` unless `onClick` is defined

### `selector` string | ELEMENT_NODE | ShadowRoot

CSS Selector or Element Node on which the toast should be added

* default: `body`

### `destination` URL string

URL to which the browser should be navigated on click of the toast

* default: `undefined`

### `newWindow` boolean

Decides whether the `destination` should be opened in a new window or not

* default: `false`

### `close` boolean

To show the close icon or not

* default: `false`

### `gravity` "top" or "bottom"

To show the toast from top or bottom

* default: `"top"`
* options:
  * `"top"` to start lining up toasts from the top viewport edge
  * `"bottom"` to start lining up toasts from the bottom viewport edge

### `position` "left" or "right"

To show the toast on left or right

* default: `"right"`
* options:
  * `"left"` to position toast along the left viewport edge
  * `"right"` to position toast along the right viewport edge

### `avatar` URL string

Image/icon to be shown before text

* default: `undefined`

### `className` string

Ability to provide custom class name for further customization

* default: `undefined`

### `stopOnFocus` boolean

To stop timer when hovered over the toast (Only if duration is set)

* default: `true`

### `callback` Function

Invoked when the toast is dismissed

* default: `undefined`

### `onClick` Function

Invoked when the toast is clicked

* default: `undefined`

### `offset` Object

Ability to add some offset to axis

* default: `undefined`
* options:
  * `{ x: number }` to set the horizontal offset
  * `{ y: number }` to set the vertical offset
  * `{ x: number, y: number }` to set the both offsets
* notes:
  * if `position` or `gravity` are used, this offset will push the toast inwards from the relevant edge.

### `escapeMarkup` boolean

Toggle the default behavior of escaping HTML markup

* default: `true`

### `ariaLive` string

Announce the toast to screen readers, see https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Live_Regions for options

* default: `"polite"`
* options:
  * `"off"` will prevent screen readers from reading the notification
  * `"polite"` will cause screen readers to read the notification when the user is next idle
  * `"assertive"` will cause screen readers to read the notification as soon as it is shown

### `oldestFirst` boolean

Set the order in which toasts are stacked in page

* default: `true`

## Browsers support

| ![][ie]<br />IE / Edge | ![][firefox]<br />Firefox | ![][chrome]<br />Chrome | ![][safari]<br />Safari | ![][opera]<br />Opera |
| ---------------------- | ------------------------- | ----------------------- | ----------------------- | --------------------- |
| IE10, IE11, Edge       | last 10 versions          | last 10 versions        | last 10 versions        | last 10 versions      |

## Contributors

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->

<!-- prettier-ignore -->
<table>
  <tr>
    <td align="center">
      <a href="https://github.com/AStoker">
        <img
          alt="AStoker"
          src="https://avatars.githubusercontent.com/u/2907279?v=4"
          width="117"
        />
        <br />
        AStoker
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/caiomoura1994">
        <img
          alt="caiomoura1994"
          src="https://avatars.githubusercontent.com/u/9389139?v=4"
          width="117"
        />
        <br />
        caiomoura1994
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/rndevfx">
        <img
          alt="rndevfx"
          src="https://avatars.githubusercontent.com/u/5052076?v=4"
          width="117"
        />
        <br />
        rndevfx
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/1ess">
        <img
          alt="1ess"
          src="https://avatars.githubusercontent.com/u/36092926?v=4"
          width="117"
        />
        <br />
        1ess
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/d4rn0k">
        <img
          alt="d4rn0k"
          src="https://avatars.githubusercontent.com/u/2183269?v=4"
          width="117"
        />
        <br />
        d4rn0k
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/danielkaiser80">
        <img
          alt="danielkaiser80"
          src="https://avatars.githubusercontent.com/u/33827555?v=4"
          width="117"
        />
        <br />
        danielkaiser80
      </a>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/skjnldsv">
        <img
          alt="skjnldsv"
          src="https://avatars.githubusercontent.com/u/14975046?v=4"
          width="117"
        />
        <br />
        skjnldsv
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/chasedeanda">
        <img
          alt="chasedeanda"
          src="https://avatars.githubusercontent.com/u/8203134?v=4"
          width="117"
        />
        <br />
        chasedeanda
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/chrisgraham">
        <img
          alt="chrisgraham"
          src="https://avatars.githubusercontent.com/u/195389?v=4"
          width="117"
        />
        <br />
        chrisgraham
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/Wachiwi">
        <img
          alt="Wachiwi"
          src="https://avatars.githubusercontent.com/u/4199845?v=4"
          width="117"
        />
        <br />
        Wachiwi
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/FeixuRuins">
        <img
          alt="FeixuRuins"
          src="https://avatars.githubusercontent.com/u/66232834?v=4"
          width="117"
        />
        <br />
        FeixuRuins
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/gavinhungry">
        <img
          alt="gavinhungry"
          src="https://avatars.githubusercontent.com/u/744538?v=4"
          width="117"
        />
        <br />
        gavinhungry
      </a>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/haydster7">
        <img
          alt="haydster7"
          src="https://avatars.githubusercontent.com/u/4540595?v=4"
          width="117"
        />
        <br />
        haydster7
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/joaquinwojcik">
        <img
          alt="joaquinwojcik"
          src="https://avatars.githubusercontent.com/u/3205737?v=4"
          width="117"
        />
        <br />
        joaquinwojcik
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/juliushaertl">
        <img
          alt="juliushaertl"
          src="https://avatars.githubusercontent.com/u/3404133?v=4"
          width="117"
        />
        <br />
        juliushaertl
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/mort3za">
        <img
          alt="mort3za"
          src="https://avatars.githubusercontent.com/u/510242?v=4"
          width="117"
        />
        <br />
        mort3za
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/Sandip124">
        <img
          alt="Sandip124"
          src="https://avatars.githubusercontent.com/u/37034590?v=4"
          width="117"
        />
        <br />
        Sandip124
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/Tadaz">
        <img
          alt="Tadaz"
          src="https://avatars.githubusercontent.com/u/10881931?v=4"
          width="117"
        />
        <br />
        Tadaz
      </a>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/t12ung">
        <img
          alt="t12ung"
          src="https://avatars.githubusercontent.com/u/9781423?v=4"
          width="117"
        />
        <br />
        t12ung
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/victorfeijo">
        <img
          alt="victorfeijo"
          src="https://avatars.githubusercontent.com/u/8865899?v=4"
          width="117"
        />
        <br />
        victorfeijo
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/fiatjaf">
        <img
          alt="fiatjaf"
          src="https://avatars.githubusercontent.com/u/1653275?v=4"
          width="117"
        />
        <br />
        fiatjaf
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/prousseau-korem">
        <img
          alt="prousseau-korem"
          src="https://avatars.githubusercontent.com/u/59747802?v=4"
          width="117"
        />
        <br />
        prousseau-korem
      </a>
    </td>
  </tr>
</table>


<!-- ALL-CONTRIBUTORS-LIST:END -->

## License

MIT © [Varun A P](https://github.com/apvarun)

<a href="https://www.buymeacoffee.com/apvarun" target="_blank" rel="noopener"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="40" width="145" alt="Buy Me A Coffee"></a>

[ie]: https://raw.githubusercontent.com/godban/browsers-support-badges/master/src/images/edge.png
[firefox]: https://raw.githubusercontent.com/godban/browsers-support-badges/master/src/images/firefox.png
[chrome]: https://raw.githubusercontent.com/godban/browsers-support-badges/master/src/images/chrome.png
[safari]: https://raw.githubusercontent.com/godban/browsers-support-badges/master/src/images/safari.png
[opera]: https://raw.githubusercontent.com/godban/browsers-support-badges/master/src/images/opera.png

