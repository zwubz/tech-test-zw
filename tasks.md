# Build a game with CreateJS

# Module 01 - Main game loop

### 1.1 - Reference an external script

Open `index.html` and add a `script` tag that references the `CreateJS` on the `CreateJS` CDN. Also add a `script` tag for the `app.js` file.

### 1.2 - Listen for DOMContentLoaded

Open `app.js` and add an event lister to the `window`. Listen for the `DOMContentLoaded` event. The event handler should be an anonymous function.

### 1.3 - Key code constants

At the top of the event handler anonymous function. Declare four constants called `KEYCODE_LEFT`, `KEYCODE_UP`, `KEYCODE_RIGHT`, and `KEYCODE_DOWN`. Assign them the values `37`, `38`, `39`, and `40` respectively.

### 1.4 - Create a stage

Below the key code constants, assign to a constant called `stage` a `new createjs.Stage`. Make sure that you have the proper id.

### 1.5 - Create a shape

Below the `stage` constant, assign a  Assign a constant called `ship` a `new createjs.Shape`.

### 1.6 - Draw the ship shape

On the `graphics` layer of the `ship` shape, draw a white ship with the following list of points `(0, 0); (30, 15); (0, 30); (7.5, 15); (0, 0);`.

### 1.7 - Add a shape to the stage

Add the `ship` shape to the `stage`.

### 1.8 - Ticker event listener

Using the `createjs.Ticker` object and the on function, register a handler for the onTick event. The handler function should be and anonymous function that updates the `stage`.

### 1.9 - Ticker FPS

Use `createjs.Ticker` object and `setFPS()` to set the frame per second to `30`.

### 1.10 - Keyboard listener

Listen for when a user presses a key. The handler should be and anonymous function with an `event` parameter, and will need to use an `if` statement.

### 1.11 - Switch statement

Create a new switch statement and test the event.keyCode.

### 1.12 - Left key

Create a case for KEYCODE_LEFT that moves the ship left by `15` pixels. Break out of this case.

### 1.13 - Up key

Create a case for KEYCODE_UP that moves the ship up by `15` pixels. Break out of this case.

### 1.14 - Right key

Create a case for KEYCODE_RIGHT that moves the ship right by `15` pixels. Break out of this case.

### 1.15 - Down key

Create a case for KEYCODE_DOWN that moves the ship right by `15` pixels. Break out of this case.
