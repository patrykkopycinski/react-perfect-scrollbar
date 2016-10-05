# React-Perfect-Scrollbar [![Travis][build-badge]][build] [![npm][npm-badge]][npm]

This is react component to allow use [perfect-scrollbar](https://github.com/noraesae/perfect-scrollbar) in React.

### Usage
1. `npm install react-perfect-scrollbar`
2. Import the module in the place you want to use:
    ```
    import PerfectScrollbar from 'react-perfect-scrollbar'
    ```
3. Wrap you content in this component:
    ```
    <PerfectScrollbar>
        ... SCROLLBAR CONTENT HERE ...
    </PerfectScrollbar>
    ```

### Props
The following props are accepted:
#### option
The optional parameters used to initialize [perfect-scrollbar](https://github.com/noraesae/perfect-scrollbar).
For more info, please refer to  https://github.com/noraesae/perfect-scrollbar#optional-parameters
#### onScrollY
Invoked when the y-axis is scrolled in either direction.
#### onScrollX
Invoked when the x-axis is scrolled in either direction.
#### onScrollUp
Invoked when scrolling upwards.
#### onScrollDown
Invoked when scrolling downwards.
#### onScrollLeft
Invoked when scrolling to the left.
#### onScrollRight
Invoked when scrolling to the right.
#### onYReachStart
Invoked when scrolling reaches the start of the y-axis.
#### onYReachEnd
Invoked when scrolling reaches the end of the y-axis (useful for infinite scroll).
#### onXReachStart
Invoked when scrolling reaches the start of the x-axis.
#### onXReachEnd
Invoked when scrolling reaches the end of the x-axis.

All the callback 'onXXXX' can accept a parameter: the ref to the scrollbar container. You can get the current `scrollTop` and `scrollLeft` from it:
```
    <PerfectScrollbar
        onScrollY={container => console.log(`scrolled to: ${container.scrollTop}.`)}>
        ... SCROLLBAR CONTENT HERE ...
    </PerfectScrollbar>
```

### Methods
There are some methods which can be called from the ref to this component:
#### setScrollTop(top: number)
set the scrollTop of the y-scrollbar
#### setScrollLeft(left: number)
set the scrollLeft of the x-scrollbar

### Example
A working example can be found in the `example` directory. Please run `npm run example` and open `http://localhost:8080/` in browser.

### License
MIT
