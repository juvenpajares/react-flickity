# Flickity React
Flickity component for React

### Installation
```bash
  npm install flickity --save
  npm install react-flickity --save
```

### Example
```js
var React = require('react')
var Flickity = require('react-flickity')

var flickityOptions = {
    initialIndex: 0,
    cellSelector: '.sliderBoxes',
    accessibility: true,
    pageDots: true,
    wrapAround: true
}

var Carousel = React.createClass({
    render: function () {
    return (
      <Flickity
        className={ 'carousel' } // default ''
        elementType={ 'div' } // default 'div'
        options={ flickityOptions } // takes flickity options {}
        disableImagesLoaded={ false } // default false
      >
        <div className="sliderBoxes"></div>
        <div className="sliderBoxes"></div>
        <div className="sliderBoxes"></div>
      </Flickity>
    );
  }
});

module.exports = Carousel;
});
```