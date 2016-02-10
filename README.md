# Flickity React
Flickity component for React

### Installation
```bash
  npm install react-flickity
```

### Example
```js
var React = require('react')
var Flickity = require('react-flickity')

var flickityOptions = {
    initialIndex: 2
}

var Carousel = React.createClass({
    render: function () {
    return (
      <Flickity
        className={'carousel'} // default ''
        elementType={'span'} // default 'div'
        options={ flickityOptions } // takes flickity options {}
        disableImagesLoaded={false} // default false
      >
        <div className="box1"></div>
        <div className="box2"></div>
        <div className="box3"></div>
      </Flickity>
    );
  }
});

module.exports = Carousel;
});
```