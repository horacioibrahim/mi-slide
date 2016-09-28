# &lt;mi-slide&gt;

> Custom element to drawing [and sharing] slide as Silvio Meira

## Demo

[Check it live!](http://horacioibrahim.github.io/mi-slide)

## Install

Install the component using [Bower](http://bower.io):

```sh
$ bower install mi-slide --save
```

Or [download a ZIP](https://github.com/horacioibrahim/mi-slide/archive/gh-pages.zip)

## Usage

1. Import Web Components polyfill:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/mi-slide/mi-slide.html">
    ```

3. Start using it!

    ```html
    <mi-slide></mi-slide>
    ```
  
### Options

Attribute   | Options   | Default   | Description
---         | ---       |---        |---  
`slides` | *array* | `[]` | slides pages formatted into JSON specs.
`canvas`   | *object*  | `undefined`|  canvas wrapper created by Fabric.. 
`backgroundColor`  | *string* | `rgba(255,255,255,1)` |  sets the background color of the canvas.
`colorBrush`   | *string*  | `rgba(220, 14, 61, 1)`| brush color can be any regular HTML color as string.
`widthBrush`   | *number*  | `3`| is width of the pencil (point).
`selected` | *number* | `0` | variable hold the seletec page. 


### Methods

Method  | Parameters    | Returns   | Description
---     |---            |---        |---
`initialize(refid)`| refid       | Nothing    | initialize setup of the fabric.js where controls and borders is disabled. The isDrawingMode is configured to true.
`locker(obj)`| fabric.Path        |Nothing    | locks horizontal and vertical move, rotation and scaling properties of a fabric.Path.
`noBorderAndControls(obj)`| fabric.Path      |Nothing    | hide bordes and controls of the object.

### Events
Event   | Description
---     | ---
`mi-slide:json`| fire events with JSON values from Fabric's canvas.

## Development

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

1. Install [Bower](http://bower.io/) & [polyserve](https://github.com/PolymerLabs/polyserve/):

    ```sh
    $ [sudo] npm install -g bower polyserve
    ```

2. Install local dependencies:

    ```sh
    $ bower install && npm install
    ```

3. Polyserve:
    ```sh
    $ polyserver
    Starting Polyserve on port 8080
    Files in this directory are available under http://localhost:8080/components/mi-slide/
    ```

## Contributing 
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature-or-fix`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature-or-fix`
5. Submit a pull request :P

## History

For detailed changelog, check [Releases](https://github.com/horacioibrahim/mi-slide/releases).


## License
[MIT License](http://horacioibrahim.mit-license.org)
